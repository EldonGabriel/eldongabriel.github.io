---
title: "REPORT – GPO Hardening for Windows Application Control – v1.0.0"
date: 2025-09-07
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Windows, GPO, Application Control, Endpoint Security, Compliance]
excerpt: "Implementation of Group Policy restrictions to prevent unauthorized software installation and harden Windows endpoints against malicious downloads."
image:
  path: /assets/images/posts/cpanel.png
  thumbnail: /assets/images/posts/cpanel.png
  caption: "Security Implementation Overview"
---

# 0.0 Executive Summary

This report explains how application control was set up and hardened on a Windows 10 workstation. The goal was to reduce the risk of malware and unauthorized software by applying stronger security controls using Local Group Policy.

The result is a more secure system where users cannot easily install unapproved software. Administrative control is required for changes, which helps follow the principle of least privilege.

 
# 1.0 GPO Hardening for Windows Application Control

## 1.1 Project Description

The goal of this task was to restrict software installation and prevent users from installing unsafe programs.

Local Group Policy was used to:

- Block standard users from running Windows Installer packages
- Stop unauthorized software installations
- Ensure only administrators can make system-level changes
- Improve tracking and control over system modifications

These controls help protect the system from untrusted or malicious software.

 
## 1.2 Technical Task / Troubleshooting Process

This task involved reviewing default settings and applying security policies to limit software execution.

**Key Actions & Observations**

- Checked default system behavior and identified weak installation controls  
- Configured policies under:
  - Computer Configuration → Administrative Templates → Windows Components → Windows Installer  
  - Computer Configuration → Administrative Templates → Windows Components → File Explorer  
- Applied restrictions to:
  - Disable Windows Installer for standard users  
  - Enforce stricter execution rules using Windows Defender SmartScreen  
- Verified required services:
  - Windows Installer Service  
  - Windows Defender Antivirus  
- Recorded configuration steps for repeat use in lab environments  

**Root Cause:**  
Default Windows settings allow standard users more freedom than is secure. This creates a risk where users can install unsafe software. This was fixed by applying stricter Group Policy controls that block unauthorized installations.

 

## 1.3 Resolution and Validation

The system was secured by applying and testing the new policies.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | gpedit.msc |
| **Control State** | Enabled |
| **Security Mode** | Block Unauthorized Installations |
| **Scope** | Standard User Accounts |

**Validation Steps**

1. Attempted to run a software installer as a standard user  

2. Confirmed the system blocked the installation and requested administrator credentials  

3. Verified that approved software still worked normally  

 

# 2.0 CONCLUSION

## 2.1 Key Takeaways

- Default system settings are not secure enough on their own  
- Group Policy helps enforce consistent security across users  
- Testing is important to confirm controls work as expected  
- Security controls should protect the system without breaking normal use  

 

## 2.2 Security Implications & Recommendations

**Risk: Malware Execution**  
Users may accidentally install malicious software that can damage the system or steal data.  

**Mitigation:** Enable Windows Installer restrictions and SmartScreen protections through GPO.

**Risk: Privilege Escalation**  
Unauthorized software may attempt to gain higher system access.  

**Mitigation:** Limit admin rights and enforce application control policies.

**Best Practices**

- Use least privilege for all user accounts  
- Apply centralized policy controls where possible  
- Test configurations after changes  
- Document all settings for audits and repeatability  

**Framework Alignment**

- Supports system hardening and access control practices  
- Aligns with NIST standards (800-53 / CSF) for secure configuration and least privilege  
- Supports ISO 27001 and PCI-DSS requirements for controlled system environments  
