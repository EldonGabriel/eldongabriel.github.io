---
title: "SUMMARY – pfSense IDS Traffic Monitoring and EternalBlue Detection – v1.0.0"
date: 2026-01-13
author: Eldon Gabriel
categories: [Security Operations]
tags: [pfSense, IDS, Snort, EternalBlue, Network Security, Vulnerability Management]
excerpt: "Deployment of a pfSense firewall with Snort IDS to detect and analyze EternalBlue (MS17-010) exploitation in a lab environment."
image:
  path: /assets/images/posts/pfsense-ids.png
  thumbnail: /assets/images/posts/pfsense-ids.png
---

# 0.0 Executive Summary

This report documents the deployment and hardening of network monitoring using a pfSense firewall and Snort Intrusion Detection System (IDS). The objective was to reduce the risk of remote code execution and lateral movement by monitoring traffic for known vulnerabilities, including EternalBlue (MS17-010).

The result is an improved security posture achieved by replacing unmonitored network segments with a controlled detection system. This was validated by triggering IDS alerts and capturing evidence during a simulated attack on a vulnerable Windows 7 system.

 

# 1.0 pfSense IDS Traffic Monitoring and EternalBlue Detection

## 1.1 Project Description

The goal of this task was to deploy an Intrusion Detection System (IDS) to detect exploitation attempts targeting legacy services.

pfSense and Snort were used to:
- Monitor SMB traffic for known malicious signatures  
- Detect and log exploitation attempts in real time  
- Improve visibility by documenting network monitoring and response steps  

This helps protect systems from worms and ransomware that exploit protocol-level weaknesses.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on improving network visibility and applying detection rules to identify active threats.

**Key Actions & Observations**

* Identified limited visibility into inter-VLAN traffic and exploit attempts.  

* Configured pfSense firewall rules to allow controlled lab traffic.  

* Enabled Snort on selected interfaces and loaded MS17-010 (EternalBlue) signature rules.  

* Applied monitoring to network segments containing legacy Windows 7 systems.  

* Identified exposed SMB services during vulnerability scanning.  

* Verified Snort service status and rule updates.  

* Checked IP addressing to prevent conflicts across network segments.  

* Documented all configurations for repeatable IDS deployment.  

**Root Cause:** Legacy systems and unmonitored SMB traffic created a high-risk environment for exploitation. This was resolved by deploying signature-based detection using Snort.

---

## 1.3 Resolution and Validation

The IDS setup was validated by testing detection and alert generation.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | pfSense / Snort IDS |
| **Control State** | Enforced / Active |
| **Security Mode** | Signature-Based Detection |
| **Scope** | Internal Lab Network Segments |

**Validation Steps**

1. Launched an EternalBlue exploit against a Windows 7 target system.  

2. Verified that Snort generated high-priority alerts for MS17-010 activity.  

3. Confirmed that normal traffic was not disrupted while attack traffic was logged.  

 
# 2.0: CONCLUSION

## 2.1 Key Takeaways

* IDS provides visibility into exploit activity that would otherwise go undetected.  
* Signature-based detection is effective for identifying known threats like EternalBlue.  
* Proper placement of IDS sensors is critical for accurate monitoring.  
* Security controls must detect threats without interrupting normal operations.  

---

## 2.2 Security Implications & Recommendations

**Risk: Remote Code Execution (RCE)**  
Legacy services like SMBv1 allow attackers to fully compromise systems.  
**Mitigation:** Remove legacy systems where possible or apply MS17-010 patches. Restrict SMB access to required hosts only.

**Risk: Lack of Network Visibility**  
Without monitoring, attacks can spread undetected across the network.  
**Mitigation:** Deploy IDS across key network segments and keep signatures updated.

**Best Practices**

* Apply least privilege to firewall and IDS management interfaces  
* Use centralized rule management for consistent segmentation  
* Revalidate configurations after network changes  
* Maintain documentation for audits and incident response  

**Framework Alignment**

* Aligns with NIST SP 800-53 for vulnerability management and monitoring  
* Supports ISO 27001 requirements for system hardening and logging  
* Reinforces NIST CSF Detect and Protect functions through active monitoring  
