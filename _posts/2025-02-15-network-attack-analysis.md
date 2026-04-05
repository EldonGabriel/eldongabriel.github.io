---
title: "REPORT – Network Attack Analysis – v1.0.1"
date: 2025-02-15
author: Eldon Gabriel
categories: [Security Operations]
tags: [Network Security, Incident Response, DoS, TCP/IP, Firewall]
excerpt: "Analysis of a TCP SYN flood attack on a public web server, including identification and mitigation strategies."
image:
  path: /assets/images/posts/network-attack.png
  thumbnail: /assets/images/posts/network-attack.png
---

# 0.0 Executive Summary

This report documents the investigation and mitigation of a Denial of Service (DoS) attack targeting a public-facing web server. The goal was to reduce the risk of downtime and resource exhaustion by improving how the system handles network traffic and incomplete connections.

The issue was caused by a TCP SYN flood attack that overwhelmed the server with incomplete connection requests. This was addressed by applying controls such as SYN cookies, rate limiting, and firewall rules. These measures improved system stability and helped maintain availability for legitimate users.

 

# 1.0 Network Attack Analysis

## 1.1 Project Description

The goal of this task was to improve network defenses against traffic-based attacks that affect service availability.

Live traffic analysis was used to:
- Detect abnormal TCP handshake behavior  
- Identify malicious traffic patterns  
- Block or limit suspicious connection attempts  
- Document system behavior before and after mitigation  

This helps protect public services, such as a booking website, from being disrupted by external attacks.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on identifying weaknesses in the TCP connection process and applying controls to reduce the impact of flood-based attacks.

**Key Actions & Observations**

* Monitored network traffic and observed a large number of SYN requests without matching ACK responses.  

* Identified this as a TCP SYN flood attack creating many half-open connections.  

* Applied firewall rules to block known malicious IP addresses.  

* Configured rate limits to restrict the number of incoming connection attempts.  

* Implemented SYN cookies to better handle incomplete TCP handshakes.  

* Temporarily reduced service load by taking the affected system offline while applying mitigation controls.  

* Used packet analysis tools (Wireshark/Tcpdump) to confirm handshake failures and abnormal traffic patterns.  

* Verified firewall rules and system behavior after changes.  

* Documented all steps for future incident response and repeatability.  

**Root Cause:** The TCP stack allows the server to keep track of incomplete connection requests. Attackers can exploit this by sending many SYN packets without completing the handshake, consuming system resources. This was resolved by applying stricter connection handling and traffic filtering controls.

 

## 1.3 Resolution and Validation

The system’s availability was restored and verified after applying mitigation measures.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | Packet Sniffer / Firewall |
| **Control State** | Enforced |
| **Security Mode** | TCP Stack Hardening |
| **Scope** | Public Web Server Infrastructure |

**Validation Steps**

1. Monitored traffic after implementing firewall rules and rate limits.  

2. Confirmed that the number of incomplete connections decreased.  

3. Verified that legitimate users could successfully complete TCP handshakes.  

4. Confirmed that normal application performance was not affected by the changes.  

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Default TCP behavior can be exploited through SYN flood attacks.  
* Controls like SYN cookies and rate limiting help protect against resource exhaustion.  
* Packet analysis is useful for identifying abnormal network behavior.  
* Testing is required to confirm that mitigation does not impact legitimate users.  

 

## 2.2 Security Implications & Recommendations

**Risk: Service Unavailability (DoS)**  
Excessive SYN requests can overload a server and cause downtime.  

**Mitigation:** Use SYN cookies and rate limiting at both the firewall and system level.

**Risk: IP Spoofing**  
Attackers may use fake IP addresses, making IP-based blocking less effective.  

**Mitigation:** Use behavior-based detection tools such as a Web Application Firewall (WAF) and intrusion detection systems.

**Best Practices**

* Restrict access to network management interfaces using least privilege principles.  
* Use intrusion detection and prevention systems (IDS/IPS) to detect unusual traffic patterns.  
* Monitor system performance during and after mitigation to avoid unintended slowdowns.  
* Maintain documentation of all network changes for incident response and audits.  

**Framework Alignment**

* Aligns with NIST SP 800-94 for intrusion detection and prevention systems  
* Supports ISO 27001 (A.17.1) for maintaining service continuity during incidents  
* Supports the NIST CSF Respond function by applying mitigation actions during an active attack  
