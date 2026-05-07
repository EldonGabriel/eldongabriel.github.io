---
title: "REPORT – Storage Systems and Data Management – v1.0.0"
date: 2026-04-14
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Storage, HDD, SSD, NVMe, Data Management, Backup Strategy]
excerpt: "Technical analysis of storage systems, data size standards, and backup methods to keep data safe and available."
image:
  path: /assets/images/posts/storage-systems.png
  thumbnail: /assets/images/posts/storage-systems.png
---

# 0.0 Executive Summary

This report explains how storage systems work and how data are managed. The goal was to improve system performance and protect data by understanding the different storage types. The report compares older Hard Disk Drives (HDDs) with faster storage devices such as solid-state drives (SSDs) and NVMe. This also explains why the storage size appears different in operating systems owing to decimal and binary measurements.

The results provide a clear approach to storage planning and data protection. By using the 3-2-1 backup strategy and understanding system limits, data can remain safe, available, and reliable.

 

# 1.0 Storage Systems and Data Management

## 1.1 Project Description

The goal of this task was to understand how data are stored and measured to avoid running out of space or losing data.

This study focused on both physical storage devices and how systems report data to:

- **Analyze System Design:** Compared slow mechanical drives with faster flash storage.  

- ** Improved Data Protection:** Identified the need for backups and offsite storage.  

- **Improve Visibility:** Explained why storage sizes appear smaller in the operating system.  

This helps ensure that the systems meet both the performance needs and long-term data storage requirements.

 

## 1.2 Technical Task / Troubleshooting Process

This task focused on how storage devices work and how to plan storage.

**Key Actions & Observations**

* **Storage Types:**

  - HDD: Uses spinning disks. Cheap and good for large storage, but slower and easier to damage than HDDs.  

  - SSD: Uses flash memory. Faster, more reliable, and no moving parts are required.  

  - NVMe: Uses PCIe for very high speeds, removing the limits found in older SATA connections.  

* **Data Size Differences:**

  - Storage companies use decimal (base 10), whereas operating systems use binary (base 2).  

  - A “1 TB” drive showed approximately 931 GB in the system. This is normal and does not lose space.  

* **Backup Strategy:**

  - 3-2-1 rule: three copies of data, two types of storage, and one offsite copy.  

  - Backups protect against hardware failures and ransomware.  

**Root Cause** 
Downtime and data loss often occur because of hardware wear and tear or poor backup planning. This was addressed by establishing a standardized backup and hardware lifecycle policies.

 

## 1.3 Resolution and Validation

Storage systems are secured by choosing the appropriate hardware and enforcing backups.

| Parameter | Configuration Value |
| :--- | :--- |
| Primary Storage | NVMe / SSD |
| Interface Standard | PCIe / SATA |
| Backup Policy | 3-2-1 Strategy Enforced |
| Scope | Data Availability and Integrity |

**Validation Steps**

1. Performance Check: Confirmed NVMe systems are faster than SATA-based systems.  

2. Capacity Check: Size differences were considered to avoid running out of space early.  

3. Backup Test: Verified that offsite backups work and that data can be restored.  

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Faster storage (SSD/NVMe) improves the system performance and reliability.  

* The 3-2-1 backup rule is the best method for protecting data.  

* Understanding storage size differences aids in planning and budgeting.  

* A good system design balances cost (HDD) and speed (NVMe).  

 

## 2.2 Security Implications & Recommendations

**Risk: Data Loss from HDD Failure**  

HDDs can break due to physical damage or wear.  

**Mitigation:** Use SSDs for mobile systems and NVMe for critical systems.  

**Risk: Backup Failure**  

Keeping only one backup in one location risks the total loss of data.  

**Mitigation:** Always keep at least one backup offsite or in the cloud.  

**Best Practices**

* Limit access to storage and backup systems.  
* Automate backups and regularly check them.  
* Test performance after the hardware upgrades.  
* Document backup locations and the recovery steps.  

**Framework Alignment**

* Supports the NIST standards for system availability and data protection.  
* Aligns with the ISO 27001 backup requirements.  
* Follows standard IT practices for system reliability and data safety.
