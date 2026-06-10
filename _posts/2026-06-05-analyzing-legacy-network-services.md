---
title: "REPORT – Analyzing Legacy Network Services – v1.0.0"
date: 2026-06-05
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Linux, Hardening, Network Security, Access Control, Security Auditing, System Administration]
excerpt: "Technical implementation of a network service audit to demonstrate the risks of cleartext authentication protocols and network traffic interception."
image:
  path: /assets/images/posts/network-auditing.png
  thumbnail: /assets/images/posts/network-auditing.png
---

# 0.0 Executive Summary

This report documents an authorized security assessment on a Linux system. The goal was to demonstrate the risks of using outdated, unencrypted network services. The assessment focused on an Ubuntu Server 24.04 environment. 

The system was used to test network traffic and capture cleartext data. The process involved configuring legacy services, monitoring network traffic, and capturing remote authentication attempts. The results showed that passwords were easily captured in plain text. 

This demonstrates the critical need to disable outdated protocols and use secure encryption.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 Analyzing Legacy Network Services

## 1.1 Project Description

The purpose of this task was to develop Linux administration and network security skills.

The work included:

* Configuring a system to run legacy services like Telnet and Rlogin.
* Troubleshooting service configuration errors.
* Monitoring network traffic to intercept login attempts.
* Analyzing captured data to find exposed passwords.
* Removing the insecure services after testing.

This process helps administrators understand why legacy protocols are dangerous and how attackers can exploit them.

## 1.2 Technical Task / Troubleshooting Process

The assessment focused on reviewing network services and analyzing network traffic.

**Key Actions and Observations**

* Checked the Linux system for active network ports.
* Identified configuration errors preventing the legacy services from starting.
* Corrected file paths and service names to successfully launch Telnet and Rlogin.
* Used network monitoring tools to capture traffic during remote login attempts.
* Found that Telnet sends passwords one character at a time in plain text.
* Found that Rlogin buffers passwords but still sends them entirely in plain text.
* Extracted fully readable passwords directly from the captured network traffic.
* Stopped, disabled, and completely removed the vulnerable services after testing.

**Root Cause:** The legacy services failed to start initially because of outdated file paths and missing system name mappings. Updating the configurations to match the modern operating system allowed the services to start so the security assessment could proceed.

## 1.3 Resolution and Validation

The assessment results were reviewed through testing and verification of the network traffic.

| Parameter | Configuration Value |
|---|---|
| Assessment Tool | Network Traffic Analyzer |
| Target Assets | Active Network Ports |
| Assessment Type | Protocol Security Analysis |
| Operating System | Ubuntu Server 24.04 |
| Audited Services | Telnet, Rlogin |
| Data Protection | Traffic Interception |

**Validation Steps**

1. Verified that network ports were open and accepting connections.
2. Confirmed that remote login attempts were successfully intercepted.
3. Tested the captured traffic to find the unencrypted login prompts.
4. Extracted the cleartext passwords from the network capture file.
5. Verified that the insecure services were permanently disabled and completely removed from the system.

# 2.0 CONCLUSION

## 2.1 Key Takeaways

* Legacy network protocols expose severe system vulnerabilities.
* Outdated services transmit passwords and user data entirely in plain text.
* Network monitoring tools can easily capture and read unencrypted system traffic.
* Vulnerable services must be completely removed, not just stopped, to secure the system.

## 2.2 Security Implications and Recommendations

**Risk: Cleartext Data Exposure**

Insecure services like Telnet and Rlogin send passwords in plain text, allowing anyone on the network to intercept and read them.

**Recommendation:** Completely remove legacy services and replace them with secure, encrypted protocols like Secure Shell (SSH).

**Risk: Lack of Integrity Protection**

Unencrypted network sessions can be hijacked or modified by attackers without detection.

**Recommendation:** Enforce administrative policies to block cleartext authentication services at the network edge.

**Best Practices**

* Audit network ports regularly to identify unauthorized services.
* Purge unused or legacy software from the system to prevent accidental activation.
* Monitor network traffic for plain text credentials.
* Use secure encryption for all administrative network connections.

**Framework Alignment**

* Supports NIST SP 800-53 requirements for transmission confidentiality.
* Aligns with CIS Benchmark recommendations for using secure communication channels.
