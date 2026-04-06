---
title: "REPORT – Workstation Power Failure Investigation – v1.0.0"
date: 2026-04-06
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Hardware, Troubleshooting, Power Supply, Physical Security, Availability]
excerpt: "Investigation of sudden workstation shutdowns at a law firm, identifying and remediating a physical layer failure caused by insufficient power supply capacity."
image:
  path: /assets/images/posts/power-failure.png
  thumbnail: /assets/images/posts/power-failure.png
---

# 0.0 Executive Summary

This report explains the investigation and fix of a critical workstation power issue in a law firm. The goal was to reduce the risk of data loss and downtime by finding the cause of sudden shutdowns that did not show software error messages (such as BSOD).

The issue was resolved by improving the hardware setup. The original 300W Power Supply Unit (PSU) was replaced with a 650W PSU. This ensured the system had enough power to support all connected hardware, especially after additional storage drives were installed. As a result, the system became stable again and data integrity was protected.

 

# 1.0 Workstation Power Failure Investigation

## 1.1 Project Description

The goal of this task was to identify and fix unexpected system shutdowns affecting a law firm’s database workstation.

A structured physical layer analysis was used to:
- Ensure the hardware could reliably handle power demands during peak usage.
- Prevent unexpected shutdowns that could lead to database corruption.
- Improve tracking of hardware changes and their impact on system performance.

This approach ensures the system remains reliable through proper hardware planning and capacity management.

 

## 1.2 Technical Task / Troubleshooting Process

The investigation focused on the power delivery system since software logs did not show clear errors.

**Key Actions & Observations**

- Reviewed system behavior and found that shutdowns occurred during heavy read and write operations on newly installed hard drives.

- Performed tests in the physical environment:
  - Estimated total system power usage and compared it to the PSU capacity.
  - Ran stress tests using high disk activity to simulate peak load.

- Applied hardware improvements:
  - Replaced the 300W PSU with a 650W 80 Plus Gold PSU.
  - Ensured the new PSU included protection features such as Over-Current Protection (OCP).

- Checked supporting hardware:
  - Verified SATA power connections were secure.
  - Monitored system stability under continuous load.

- Documented the setup to support future hardware planning and repeatability.

**Root Cause:** The addition of multiple hard drives caused the system to exceed the capacity of the 300W PSU. This triggered a safety shutdown during high power usage. The issue was resolved by upgrading to a higher-capacity power supply.

 

## 1.3 Resolution and Validation

The issue was resolved by upgrading the power supply and confirming system stability under load.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | Physical Inspection / Load Stress Test |
| **Control State** | Enforced |
| **Security Mode** | Hardware Capacity Hardening |
| **Scope** | Database Workstation Physical Layer |

**Validation Steps**

1. Simulated real-world usage by performing large file transfers across all storage drives.

2. Confirmed the system stayed operational without shutting down, showing that the new PSU handled the load successfully.

3. Monitored the system for 72 hours during normal operations to ensure long-term stability.

 

# 2.0 CONCLUSION

## 2.1 Key Takeaways

- Security and reliability depend on the physical layer, not just software.
- Hardware changes must be reviewed to ensure the system can handle increased power demands.
- Testing under high load is necessary to confirm that a fix is effective.
- Proper planning allows for safe system growth and future upgrades.

 

## 2.2 Security Implications & Recommendations

**Risk: Data Corruption due to Sudden Power Loss**  
Unexpected shutdowns can interrupt write operations and damage database files.  

**Mitigation:** Use an Uninterruptible Power Supply (UPS) and ensure the PSU has enough capacity for the system load.

**Risk: Unplanned Downtime**  
Hardware failures can disrupt business operations and limit access to important data.  

**Mitigation:** Implement regular hardware reviews and capacity planning to ensure systems remain within safe operating limits.

**Best Practices**

- Restrict physical access to hardware to authorized personnel only.
- Maintain an inventory of hardware components and their power requirements.
- Test systems after hardware changes using stress tests to confirm stability.
- Keep documentation updated to support audits and future upgrades (aligned with NIST Cybersecurity Framework ID.AM-1).

**Framework Alignment**

- Supports NIST Cybersecurity Framework (PR.DS-4) by maintaining system availability.
- Aligns with physical and environmental protection controls by securing the hardware layer.
- Reinforces the Protect function by ensuring infrastructure can reliably support business operations.
