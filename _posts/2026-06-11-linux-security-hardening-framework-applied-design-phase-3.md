---
title: "REPORT – Linux Security Hardening Framework: Applied Design Scenario (Phase 3) – v1.0.0"
date: 2026-06-11
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Linux, Hardening, Security Architecture, Access Control, Framework Design, System Administration]
excerpt: "Phase 3 of a Linux security hardening framework showing how a structured design reduces risk and strengthens system baselines."
image:
  path: /assets/images/posts/hardening-design.png
  thumbnail: /assets/images/posts/hardening-design.png
---

# 1.0 Executive Summary

This report explains the design of a Linux Security Hardening Framework. It shows how the framework secures a test environment and builds a hardened system baseline. The design removes legacy protocols, enforces access control, strengthens authentication, and enables system monitoring. 
It addresses common security gaps found in default Linux systems and improves overall system security.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 2.0 Scope of Assessment

The framework applies to a Linux virtual machine. It covers:

* Network services and legacy protocols  
* Passwords and account lockout rules  
* Access control and system integrity  
* System updates and patching  
* File permissions and hardware access  
* Intrusion detection and log monitoring  

# 3.0 Methodology

This design follows the Linux Security Hardening Assessment Framework and its workbook.

It uses three steps:

1. **Baseline check:** Compare the system to the framework rules  
2. **Control design:** Define security rules for users, network, and system files  
3. **Validation plan:** Define how to test if controls work without breaking the system  

# 4.0 Pre-Hardening Security Findings 

The baseline shows common risks in default Linux systems:

**Legacy Protocol Exposure (High)** 
Services like Telnet, FTP, and Rlogin may be enabled. These send data in plain text and can expose passwords.

**Authentication Weaknesses (High)**
Root login may be allowed. Password rules and lockouts are often weak or missing.

**Visibility Gaps (Medium)**
Systems may lack IDS tools and centralized log monitoring, making attacks harder to detect.

# 5.0 Security Improvements

The framework defines these controls:

**Identity and Access Control (Critical)**
* Block direct root login  
* Enforce strong passwords using PAM  
* Require password changes and prevent reuse  
* Lock accounts after 3 failed login attempts  

**Network and Service Hardening (Critical)**
* Disable Telnet, FTP, and Rlogin  
* Remove unused services at boot  

**System Integrity (High)**
* Update kernel and system packages  
* Enable SELinux in Enforcing mode  
* Remove unowned files  
* Disable USB and Thunderbolt ports  

**Monitoring and Detection (High)**
* Use Logwatch or Logcheck for log review  
* Deploy a host-based IDS  

## 5.1 Validation Design

The framework uses these checks:

* Test authentication and lockout rules  
* Scan for open ports and disabled services  
* Confirm SELinux is enforcing  
* Check for unowned files  
* Test log alerts and IDS detection  

# 6.0 Business Impact

* This framework turns a default Linux system into a locked-down environment. 
* It reduces risk from brute-force attacks, exposed services, and data theft. 
* Logging and IDS tools improve detection and response speed.

# 7.0 Framework Alignment

* **CIS Controls:** Secure configuration and logging  
* **NIST SP 800-53:** Access control and system integrity  
* **ISO/IEC 27001:2022:** Identity management and monitoring  

# 8.0 Conclusion

This framework defines a secure baseline for Linux systems. It reduces attack surface before deployment and improves system security from the start. 
Regular updates and monitoring are required to maintain this security level.
