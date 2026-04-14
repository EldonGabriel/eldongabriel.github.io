---
title: "REPORT – Storage Systems and Data Management – v1.0.0"
date: 2026-04-14
author: Eldon Gabriel
categories: [Infrastructure & Systems]
tags: [Storage, HDD, SSD, NVMe, Data Management, Backup Strategy]
excerpt: "Technical analysis of storage systems, data size standards, and backup methods to keep data safe and available."
image:
  path: /assets/images/posts/storage-systems.png
  thumbnail: /assets/images/posts/storage-systems.png
---

# 0.0 Executive Summary

This report explains how storage systems work and how data is managed. The goal was to improve system performance and protect data by understanding different storage types. The report compares older Hard Disk Drives (HDDs) with faster storage like Solid-State Drive (SSDs) and NVMe. It also explains why storage size looks different in operating systems due to decimal and binary measurements.

The result is a clear approach to storage planning and data protection. By using the 3-2-1 backup strategy and understanding system limits, data can stay safe, available, and reliable.

 

# 1.0 Storage Systems and Data Management

## 1.1 Project Description

The goal of this task was to understand how data is stored and measured to avoid running out of space or losing data.

The work focused on both physical storage devices and how systems report data to:

- Analyze System Design: Compared slow mechanical drives with faster flash storage.  

- Improve Data Protection: Identified the need for backups and offsite storage.  

- Improve Visibility: Explained why storage sizes appear smaller in the operating system.  

This helps ensure systems meet both performance needs and long-term data storage requirements.

 

## 1.2 Technical Task / Troubleshooting Process

This task focused on how storage devices work and how to plan storage correctly.

**Key Actions & Observations**

* **Storage Types:**

  - HDD: Uses spinning disks. Cheap and good for large storage, but slower and easier to damage.  

  - SSD: Uses flash memory. Faster, more reliable, and no moving parts.  

  - NVMe: Uses PCIe for very high speeds, removing limits found in older SATA connections.  

* **Data Size Differences:**

  - Storage companies use decimal (base 10), while operating systems use binary (base 2).  

  - A “1 TB” drive shows about 931 GB in the system. This is normal and not lost space.  

* **Backup Strategy:**

  - 3-2-1 rule: 3 copies of data, 2 types of storage, 1 offsite copy.  

  - Backups protect against hardware failure and ransomware.  

**Root Cause** 
Downtime and data loss often happen because of hardware wear-and-tear or poor backup planning. This was addressed by establishing a standardized backup and hardware lifecycle policy.

 

## 1.3 Resolution and Validation

Storage systems were secured by choosing the right hardware and enforcing backups.

| Parameter | Configuration Value |

| :--- | :--- |

| Primary Storage | NVMe / SSD |

| Interface Standard | PCIe / SATA |

| Backup Policy | 3-2-1 Strategy Enforced |

| Scope | Data Availability and Integrity |

**Validation Steps**

1. Performance Check: Confirmed NVMe systems are faster than SATA-based systems.  

2. Capacity Check: Accounted for size differences to avoid running out of space early.  

3. Backup Test: Verified that offsite backups work and data can be restored.  

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Faster storage (SSD/NVMe) improves system performance and reliability.  

* The 3-2-1 backup rule is the best way to protect data.  

* Understanding storage size differences helps with planning and budgeting.  

* Good system design balances cost (HDD) and speed (NVMe).  

 

## 2.2 Security Implications & Recommendations

**Risk: Data Loss from HDD Failure**  

HDDs can break due to physical damage or wear over time.  

**Mitigation:** Use SSDs for mobile systems and NVMe for critical systems.  

**Risk: Backup Failure**  

Keeping only one backup in one location risks total data loss.  

**Mitigation:** Always keep at least one backup offsite or in the cloud.  

**Best Practices**

* Limit access to storage and backup systems.  
* Automate backups and check them regularly.  
* Test performance after hardware upgrades.  
* Document backup locations and recovery steps.  

**Framework Alignment**

* Supports NIST standards for system availability and data protection.  
* Aligns with ISO 27001 backup requirements.  
* Follows standard IT practices for system reliability and data safety.
