---
title: "REPORT – Troubleshooting pfSense DNS Resolution – v1.0.0"
date: 2026-04-27
author: Eldon Gabriel
categories: [Security Operations]
tags: [pfSense, DNS, Networking, Firewall, Troubleshooting]
excerpt: "Resolution of DNS failures in a hardened pfSense environment by implementing controlled, explicit DNS access under a default-deny policy."
image:
  path: /assets/images/posts/troubleshooting-pfsense.png
  thumbnail: /assets/images/posts/troubleshooting-pfsense.png
---

# 0.0 Executive Summary

This report outlines the identification and resolution of a DNS failure in a hardened pfSense network. This issue prevented systems from resolving external domain names, impacting normal Internet functionality despite active network connectivity.

The systems were able to reach external IP addresses but failed to resolve domain names, indicating a service-layer failure rather than a connectivity issue.

The objective was to restore the domain name resolution while maintaining a strict "Default Deny" security posture. The investigation followed a structured OSI-based approach, progressing from Layer 3 connectivity validation to Layer 7 service analyses.

The result is a stable and secure network configuration in which DNS traffic is explicitly permitted and monitored. By implementing targeted firewall rules for TCP/UDP Port 53 and enabling DNS Forwarding Mode in Unbound, the environment now enforces the least privilege while maintaining the required functionality.

 

# 1.0 Troubleshooting pfSense DNS Resolution

## 1.1 Project Description

The goal of this task was to diagnose and resolve DNS failures caused by the transition of a network to a hardened security state.

The approach focused on controlled outbound access through an explicit firewall policy by:

- **Enforcing Secure Behavior:** Transitioning from an open network to a default-deny model, where all traffic requires explicit authorization.
- **Controlled Outbound Access:** Only allowing the required DNS traffic to the internal resolver.
- **Improved Visibility:** Differentiating between connection timeouts (connectivity/firewall issues) and service failures (configuration issues).

This ensures that critical system operations, such as software updates and domain-based access, function correctly without exposing the network to unnecessary outbound risks.

 

## 1.2 Technical Task / Troubleshooting Process

The troubleshooting process followed the OSI model to isolate the failure point between the client system and the upstream DNS services.

**Key Actions & Observations**

* **Layer 3 Validation**
  - Verified external connectivity using IP-based testing (`ping 8.8.8.8`), and confirmed gateway routing and NAT functionality.
  - Failure observed when using domain names, isolating the issue to DNS resolution.

* **Service Analysis (Port 53)**
  - Identified that the default-deny firewall policy on the LAN interface blocked DNS traffic.
  - Confirmed DNS requires both UDP and TCP Port 53 for standard queries and larger responses.

* **Policy Remediation**
  - **Firewall Rules:** An explicit allow rule was implemented for TCP/UDP Port 53 from the LAN network to the pfSense resolver.
  - **Unbound Configuration:** DNS Forwarding Mode is enabled to ensure that queries are properly forwarded to upstream resolvers.

* **Rule Optimization**
  - Positioned the DNS allow rule at the top of the firewall rule set to prevent it from being overridden by broader deny rules.

**Root Cause:** The failure was caused by a correctly enforced default-deny firewall policy that lacked a required exception for DNS traffic (TCP/UDP Port 53), resulting in all name resolution requests being blocked.

 

## 1.3 Resolution and Validation

The DNS service was restored by applying targeted access controls and validating both the functionality and policy enforcement.

| Parameter | Implemented Configuration |
| :--- | :--- |
| **Management Tool** | pfSense / Unbound / dig |
| **Protocol** | TCP/UDP |
| **Service Port** | 53 |
| **Security Mode** | Explicit Allow (Default Deny) |

**Validation Steps**

1. **Query Validation:**  
   Executed `nslookup` and `dig google.com`, confirming successful responses and transition from timeout to non-authoritative answers.

2. **Functional Testing:**  
   Hostname-based connectivity tests were performed to verify the end-to-end resolution and routing.

3. **Log Verification:**  
   Reviewed pfSense firewall logs to confirm that DNS traffic was correctly permitted and matched the configured allow rule.

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Hardened environments require explicit allowance rules for all essential services, including DNS.
* Troubleshooting should follow a structured OSI-based approach to separate connectivity issues from service level failures.
* DNS validation must include both UDP and TCP to ensure compatibility with the modern network behavior.
* Secure configurations must balance restrictive policies and operational requirements.

 
## 2.2 Security Implications & Recommendations

**Risk: Unauthorized Outbound Communication**  
**Description:** Open DNS configurations can be abused for data exfiltration through DNS tunneling.  
**Mitigation:** Enforce centralized DNS through pfSense and monitor query logs for abnormal frequency or payload size.

**Risk: Firewall Rule Misconfiguration**  
**Description:** Incorrect rule ordering can result in allow rules being overridden by broader deny policies.  
**Mitigation:** Implement rule hierarchy validation to ensure critical service rules are evaluated before default deny rules.

**Best Practices**

* DNS over TLS (DoT) is implemented to protect query confidentiality.
* Restrict clients from using external DNS servers to enforce centralized control of the DNS service.
* Conduct periodic negative testing to confirm that only the required ports are permitted.
* Maintain documented firewall and DNS configurations as a source-of-truth.

**Framework Alignment**

* Aligns with NIST Cybersecurity Framework **PR.AC (Access Control)** through enforcement of least privilege network policies.
* Supports **DE.CM-1 (Network Monitoring)** by enabling visibility into DNS traffic patterns.
* Reinforces secure network design principles for both laboratory and production environments.
