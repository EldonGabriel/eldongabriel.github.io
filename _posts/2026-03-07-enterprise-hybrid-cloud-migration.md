---
title: "REPORT – Enterprise Hybrid-Cloud Migration – v1.2.0"
date: 2026-03-07
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Cloud Security, Hybrid-Cloud, VMware, AWS, Migration]
excerpt: "Migration of enterprise workloads from VMware ESXi to AWS using AWS Application Migration Service."
image:
  path: /assets/images/posts/enterprise-migration.png
  thumbnail: /assets/images/posts/enterprise-migration.png
---

# 0.0 Executive Summary

This report describes the migration of enterprise systems from a local VMware ESXi environment to AWS.

The goal was to reduce risks related to hardware failure and single points of failure by moving workloads into a hybrid-cloud setup with better scalability, monitoring, and centralized identity control.

The result is a more reliable and flexible environment. On-premise infrastructure was replaced with a hybrid-cloud model that allows controlled, trackable, and secure workload migration. This was confirmed through successful testing of Windows Server and Active Directory systems after migration to AWS EC2.

 

# 1.0 Enterprise Hybrid-Cloud Migration

## 1.1 Project Description

The goal of this task was to build a secure migration process to move enterprise workloads to a hybrid-cloud environment without losing data or disrupting services.

A multi-phase approach was used to:
- Establish DNS as a central point of control and configure NAT for isolated network segments  
- Use VMware vCenter Server Appliance (VCSA) to manage ESXi hosts from a single interface  
- Integrate AWS Application Migration Service (MGN) to monitor replication and migration in real time  

These steps ensure that critical systems, such as domain controllers (DC01/DC2001) and workstations (WS01), remain available and protected during and after migration.

 

## 1.2 Technical Task / Troubleshooting Process

This process focused on identifying limitations in the local virtualization environment and applying structured migration methods to move workloads into AWS.

**Key Actions & Observations**

* Reviewed the VMware environment and identified limitations in scaling, licensing, and resource allocation.

* Configured Active Directory Domain Services (ADDS) for the `corp.internal` domain.

* Set up AWS MGN launch settings to handle hardware and driver differences during migration.

Applied network controls including:
  - NAT Gateway for controlled outbound traffic  
  - Forward and reverse DNS zones for name resolution  

* Reduced complexity and attack surface using standardized host management configurations.

Verified supporting services:
  - vCenter Single Sign-On (SSO) integration  
  - GPT partitioning and EFI boot support for migrated systems  

* Documented all steps to support repeatable migration for larger environments.

**Root Cause:** Traditional on-premise environments often lack built-in scaling and disaster recovery features. This was addressed by introducing cloud-based replication and structured migration policies to connect VMware and AWS environments.

 

## 1.3 Resolution and Validation

The migration was validated by testing replicated systems and confirming successful cutover behavior.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | VMware VCSA / AWS MGN |
| **Control State** | Enforced / Migrated |
| **Security Mode** | Agent-Based Continuous Replication |
| **Scope** | Enterprise Virtual Workloads |

**Validation Steps**

1. Performed a “Test Launch” in AWS MGN to confirm the migrated Windows Server 2019 instance functioned correctly.  

2. Verified that user data in `D:\Users` remained intact after migration to EC2.  

3. Confirmed that Active Directory authentication and DNS resolution worked correctly after cutover.  

4. Ensured system stability and application compatibility in the cloud environment.  

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Moving away from on-premise hardware reduces the risk of outages caused by hardware failure.  

* Using structured migration tools like AWS MGN helps maintain consistency across environments.  

* Testing is required to ensure migrated systems boot correctly and function as expected.  

* Hybrid-cloud setups provide flexibility while still maintaining control over critical systems.  

 

## 2.2 Security Implications & Recommendations

**Risk: Inconsistent Identity Management**  
If Active Directory is not properly synchronized, access control may become fragmented and accounts may become unmanaged.  

**Mitigation:** Use centralized identity management across both on-premise and cloud environments.

**Risk: Data Corruption During Migration**  
Replication issues can lead to corrupted systems or failed instances.  

**Mitigation:** Perform regular test migrations to confirm data integrity before final cutover.

**Best Practices**

* Limit access to both vCenter and AWS migration tools using least privilege principles.  
* Use centralized tools such as AWS Systems Manager (SSM) to manage EC2 instances.  
* Validate network configurations after changes to prevent connectivity issues.  
* Document all migration steps to support future operations and troubleshooting.  

**Framework Alignment**

* Aligns with NIST SP 800-144 for cloud security guidance  
* Supports ISO 27001 change management controls (A.12.1.2)  
* Supports NIST CSF Identify and Protect functions by improving asset visibility and securing data during migration  
