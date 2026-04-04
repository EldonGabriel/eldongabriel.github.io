---
title: "REPORT – Monitoring Windows Processes with Procmon – v1.0.1"
date: 2025-09-01
author: Eldon Gabriel
categories: [Security Operations]
tags: [Windows, Sysinternals, Procmon, Incident Response, Monitoring]
excerpt: "Utilization of Process Monitor (Procmon) to capture, filter, and analyze real-time system events for security auditing and process behavior validation."
image:
  path: "/assets/images/procmon.png"
  thumbnail: "/assets/images/procmon.png"
---

# 0.0 Executive Summary

This report explains how system monitoring was set up on a Windows 10 workstation using Sysinternals Process Monitor (Procmon).

The main goal was to reduce the risk of unauthorized system changes and improve visibility into how processes behave. This was done by using stronger monitoring and filtering methods.

The final result improved security by moving from passive observation to active monitoring with filters. This allowed faster detection of unusual activity across the registry, file system, and network.

 

# 1.0 Monitoring Windows Processes with Procmon

## 1.1 Project Description

The goal of this task was to set up detailed system monitoring to detect hidden or suspicious activity and ensure process actions can be reviewed.

Procmon was used to:
- Identify processes that behave outside their expected function  
- Monitor access to sensitive files and registry keys  
- Record and export system events for later analysis  

This helps ensure that system activity is visible and can be reviewed for security or troubleshooting purposes.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on improving system visibility by filtering out unnecessary noise and focusing on important events.

### Key Actions & Observations

- Reviewed default Procmon output and observed a large number of low-value background events  

- Configured Procmon filters to:
  - Include specific process names  
  - Exclude repetitive or low-value operations such as common file reads  

- Applied monitoring to:
  - Registry activity, including key access and value changes  
  - File system activity in sensitive directories  

- Verified supporting requirements:
  - Administrative privileges for full system monitoring  
  - Ability to export logs in CSV and PML formats  

- Documented filter settings for reuse in future investigations  

**Root Cause:**  
Default system logging does not provide enough detail for real-time analysis. Important activity can be hidden among large amounts of normal system noise. This was resolved by using Procmon with filters to focus only on meaningful events.

---

## 1.3 Resolution and Validation

The monitoring setup was tested to confirm it captured and displayed the correct system activity.

| Parameter | Configuration Value |
| :--- | :--- |
| Management Tool | Procmon (v3.x) |
| Control State | Enforced (Admin Level) |
| Security Mode | Filtered Real-Time Capture |
| Scope | Process, Registry, and File System |

### Validation Steps

1. Ran a test process to generate system activity  

2. Verified that Procmon captured relevant events in real time  

3. Confirmed that filters removed unnecessary background noise  

4. Reviewed registry and file system activity for expected changes  

5. Exported the captured data to a CSV file for further analysis  

6. Confirmed the system remained stable during monitoring  

 

# 2.0 CONCLUSION

## 2.1 Key Takeaways

- Default system logs are not enough for detailed process analysis  
- Procmon provides real-time visibility into system activity  
- Filters are needed to focus on important events and reduce noise  
- Testing ensures that monitoring tools capture accurate and useful data  
- Proper setup helps detect unusual or suspicious behavior early  

---

## 2.2 Security Implications and Recommendations

**Risk: Unauthorized Access to Sensitive Data**  
Processes may attempt to access files they should not have permission to use.

**Mitigation:**  
Monitor file access patterns and review permissions regularly. Use Procmon to detect unusual activity.

**Risk: Registry Manipulation**  
Malware may use the registry to persist or disable security controls.

**Mitigation:**  
Monitor critical registry hives for unexpected changes such as new keys or modified values.

### Best Practices

- Apply least privilege so processes only access what they need  
- Use centralized monitoring tools such as Sysmon for larger environments  
- Review logs regularly to detect unusual patterns  
- Document monitoring configurations for consistency and audits  

### Framework Alignment

- Supports NIST SP 800-53 audit and accountability controls  
- Aligns with ISO 27001 logging and monitoring requirements  
- Supports the Detect function of the NIST Cybersecurity Framework by enabling identification of suspicious activity  
