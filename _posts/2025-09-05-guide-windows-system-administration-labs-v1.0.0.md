---
title: "GUIDE – Windows System Administration Labs (11 Independent Labs) – v1.0.0"
date: 2025-09-05
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Windows, System Administration, Cybersecurity, Labs, AWS, Virtualization]
excerpt: "A collection of 11 hands-on labs designed to build Windows administration skills, covering maintenance, troubleshooting, security, and automation — all tested in an AWS-hosted Windows 10 VM."
image:
  path: "/assets/images/11labs.png"
  thumbnail: "/assets/images/11labs.png"
---
 
# 0.0 Executive Summary

This report shows how Windows 10 was set up and secured across 11 different admin tasks. The goal was to reduce system problems, stop unauthorized access, and prevent data loss. This was done by applying stronger security settings and better system maintenance in an AWS virtual machine.

As a result, the system became more secure and stable. Default settings were replaced with controlled and monitored configurations. Each task was tested to confirm that it worked as expected.

 
# 1.0 Windows System Administration Labs

## 1.1 Project Description

The goal of this project was to set up a standard and secure system across 11 key Windows features.

An AWS-hosted Windows 10 VM was used to:

* Improve security by setting up BitLocker, Firewall rules, and Credential Manager
* Block unauthorized actions by adjusting the Registry and reviewing system details
* Increase system visibility by using Event Viewer and Task Scheduler for monitoring

This approach helps protect the system from common errors and security risks by using regular maintenance and strong control settings.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on finding weak default settings in Windows and replacing them with stronger controls.

**Key Actions & Observations**

* **Storage & Performance:** Cleaned up disk space and ran defragmentation to improve speed
* **Automation & Logging:** Used Task Scheduler to automate tasks and Event Viewer to check system logs
* **Network & Security:** Reviewed Firewall rules and explored BitLocker to protect stored data
* **Configuration Management:** Made safe Registry changes and managed installed programs
* **Identity Management:** Used Credential Manager to secure saved login details

**Root Cause:** Default Windows settings focus on ease of use, not security. This was fixed by applying stronger admin controls based on best practices.

 
## 1.3 Resolution and Validation (Demonstrations)

The system was secured and improved across all 11 lab areas. Each task was tested and confirmed.

| Lab Module                 | Technical Objective      | Result       |
| :------------------------- | :----------------------- | :----------- |
| **1. Disk Cleanup**        | Remove junk files        | **Verified** |
| **2. Defragmentation**     | Improve disk performance | **Verified** |
| **3. Task Scheduler**      | Automate tasks           | **Verified** |
| **4. Defender Firewall**   | Control network access   | **Verified** |
| **5. Registry Editor**     | Make safe system changes | **Verified** |
| **6. Event Viewer**        | Review system logs       | **Verified** |
| **7. System Info**         | Collect system data      | **Verified** |
| **8. Programs/Features**   | Manage applications      | **Verified** |
| **9. Network Sharing**     | Fix connection issues    | **Verified** |
| **10. BitLocker**          | Encrypt data             | **Verified** |
| **11. Credential Manager** | Secure login data        | **Verified** |

 
# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Regular maintenance like disk cleanup and defrag helps keep systems running smoothly
* Event Viewer and Task Scheduler improve system monitoring and response
* Security features like Firewall, BitLocker, and Credential Manager must be set up manually
* Instructor feedback confirmed the work meets professional standards

 

## 2.2 Security Implications & Recommendations

**Risk: Unauthorized Data Access**
Unencrypted drives and saved credentials can expose sensitive data.

**Mitigation:**
Enable BitLocker and regularly review Credential Manager for unused or suspicious entries.

**Risk: Lateral Movement**
Weak firewall settings can allow attackers to move across systems.

**Mitigation:**
Set strict inbound and outbound rules in Windows Defender Firewall.


**Best Practices**

* Use least privilege when editing the Registry or removing programs
* Apply settings using Group Policy for better control at scale
* Check Event Viewer regularly for warnings and critical errors
* Document all changes for tracking and compliance

**Framework Alignment**

* Supports NIST CSF **PR.IP** by ensuring systems are maintained and documented
* Supports **PR.AC** by controlling user access and network traffic
* Supports **PR.MA** by improving system performance and reliability
