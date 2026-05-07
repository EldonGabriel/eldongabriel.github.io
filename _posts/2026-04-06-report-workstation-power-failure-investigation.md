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

This report explains the investigation and resolution of a critical workstation power issue in a law firm. The goal was to reduce the risk of data loss and downtime by identifying the cause of sudden shutdowns that did not show software error messages (such as BSOD).

This issue was resolved by improving the hardware setup. The original 300 W Power Supply Unit (PSU) was replaced with a 650 W PSU. This ensured that the system had sufficient power to support all the connected hardware, especially after the installation of additional storage drives. Consequently, the system became stable again, and data integrity was protected.

 

# 1.0 Workstation Power Failure Investigation

## 1.1 Project Description

The goal of this task was to identify and fix unexpected system shutdowns that affected a law firm’s database workstation.

A structured physical layer analysis was used to:
- Ensure that the hardware can reliably handle power demands during peak usage.
- Prevent unexpected shutdowns that could lead to database corruption.
- Improve the tracking of hardware changes and their impact on system performance.

This approach ensures that the system remains reliable through proper hardware planning and capacity management.

 

## 1.2 Technical Task / Troubleshooting Process

The investigation focused on the power delivery system because the software logs did not show clear errors.

**Key Actions & Observations**

- Reviewed the system behavior and discovered that shutdowns occurred during heavy read and write operations on newly installed hard drives.

Tests were performed in a physical environment.
  - Estimated the total system power usage and compared it with the PSU capacity.
  - Ran stress tests using high disk activity to simulate the peak load.

The applied hardware improvements are as follows:
  - Replaced the 300 W PSU with a 650 W 80 Plus Gold PSU.
  - Ensured that the new PSU included protection features such as overcurrent protection (OCP).

The supporting hardware was checked.
  - Verified that the SATA power connections were secure.
  - Monitored system stability under continuous loads.


- Documented the setup to support future hardware planning and its repeatability.

**Root Cause:** The addition of multiple hard drives caused the system to exceed the capacity of the 300W PSU. This triggered a safety shutdown during high-power usage. This issue was resolved by upgrading to a higher-capacity power supply.

 

## 1.3 Resolution and Validation

This issue was resolved by upgrading the power supply and confirming the system stability under load.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | Physical Inspection / Load Stress Test |
| **Control State** | Enforced |
| **Security Mode** | Hardware Capacity Hardening |
| **Scope** | Database Workstation Physical Layer |

**Validation Steps**

1. Simulated real-world usage was performed by transferring large files across all storage drives.
2. The system remained operational without shutting down, indicating that the new PSU successfully handled the load.
3. The system was monitored for 72 h during normal operations to ensure long-term stability.

 

# 2.0 Conclusion

## 2.1 Key Takeaways

- Security and reliability depend on the physical layer, not only on software.
- Hardware changes must be reviewed to ensure that the system can handle increased power demands.
- Testing under high loads is necessary to confirm the effectiveness of the fix.
- Proper planning allows safe system growth and future upgrades.

 

## 2.2 Security Implications & Recommendations

**Risk: Data Corruption due to Sudden Power Loss**  
Unexpected shutdowns can interrupt write operations and damage database files.  

**Mitigation:** Use an Uninterruptible Power Supply (UPS) and ensure the PSU has enough capacity for the system load.

**Risk: Unplanned Downtime**  
Hardware failures can disrupt business operations and limit access to critical data.  

**Mitigation:** Implement regular hardware reviews and capacity planning to ensure systems remain within safe operating limits.

**Best Practices**

- Restrict physical access to hardware to authorized personnel.
- Maintain an inventory of hardware components and their power requirements.
- Test systems after hardware changes using stress tests to confirm their stability.
- Keep documentation updated to support audits and future upgrades (aligned with the NIST Cybersecurity Framework ID.AM-1).

**Framework Alignment**

- Supports the NIST Cybersecurity Framework (PR.DS-4) by maintaining system availability.
- Aligns with physical and environmental protection controls by securing the hardware layer.
- Reinforces the protection function by ensuring that infrastructure can reliably support business operations.
