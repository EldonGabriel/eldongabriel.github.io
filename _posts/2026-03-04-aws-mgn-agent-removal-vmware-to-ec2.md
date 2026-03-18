---
title: "Resolving AWS MGN Agent Removal Issues After VMware to EC2 Migration"
date: 2026-03-04
author: Eldon Gabriel
tags: [AWS, Cloud Migration, VMware, Troubleshooting, Infrastructure]
excerpt: "A practical troubleshooting case study on migrating VMware virtual machines to AWS EC2 and resolving kernel driver removal issues from the AWS Application Migration Service."
image:
  path: /assets/images/posts/vmware-aws-migration.png
  thumbnail: /assets/images/posts/vmware-aws-migration.png
---

# Resolving AWS MGN Agent Removal Issues After VMware to EC2 Migration

<!-- Project -->
<div style="flex:0 1 500px; background:rgba(255,255,255,0.05); padding:20px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<img
src="{{ '/assets/images/your-image.png' | relative_url }}"
style="width:100%; border-radius:8px; border:1px solid #333;" />

</div>

## What I Studied
This exercise involved a full-scale hybrid-cloud migration, in which on-premises VMware workloads (Windows Server 2019 and Windows 11) were moved into AWS EC2 using the AWS Application Migration Service (MGN).

**Tools and Techniques:** VMware vSphere 8.0, AWS MGN, PowerShell (DNS automation), and Windows Safe Mode for kernel-level troubleshooting.

**Key Frameworks:** Hybrid-Cloud Interoperability, FinOps (cloud cost optimization), and Root Cause Analysis (RCA).

---

## What I Learned
**Hands-on Skills:** Deployed the AWS Replication Agent and configured the Default Host Management Configuration (DHMC) in AWS Systems Manager (SSM) for centralized post-migration management.

**Observations:** Migration is not complete once the VM boots. If not properly removed, the driver stack remains tied to the source hypervisor, thereby creating stability risks.

**Troubleshooting Lessons:** Standard uninstall methods may fail against kernel-level drivers. Safe Mode was required to break file locks and allow manual cleanup, along with Boot Configuration Data (BCD) adjustments for BIOS to GPT/EFI transition.

---

## Why It Matters
**Enterprise Security:** Leftover migration agents and orphaned cloud resources (300+) increase the attack surface and cost.

**Operational Defense:** Handling a Hardware Abstraction Layer (HAL) failure ensures that critical data remains accessible even when the OS fails.

**Real-World Analogy:** Migrating systems is analogous to moving an engine between cars. If the mounting components (drivers) are not replaced, the system will not function correctly.

---

## How It Maps to the Job / Framework
- **NIST NICE – Systems Architecture (SP-ARC)**
- **ASD Cyber Skills Framework – Systems Development (SDEV)**

These skills directly apply to cloud migration and system administration roles responsible for lift-and-shift operations, system recovery, and cloud resource management.

---

## Key Takeaways
- DNS is foundational. A and PTR records are required for stable hybrid environments  
- FinOps is security. Removing unused resources reduces both cost and risk  
- Kernel-level awareness is critical for advanced troubleshooting  
- Data preservation must be prioritized during system recovery   

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Engineering Report: VMware to AWS EC2 Migration</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->
<div style="flex:0 1 500px; background:rgba(255,255,255,0.05); padding:20px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/reports/REPORT – Enterprise Hybrid-Cloud Migration – v1.2.0.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:12px; color:#aaa;">
<strong>REPORT – Enterprise Hybrid-Cloud Migration – v1.2.0.pdf</strong>
</p>

</div>

</div>

---

### Technical Skills Demonstrated
* **Cloud Migration:** VMware virtual machine migration to AWS EC2 using AWS MGN.
* **Operating Systems:** Windows Server and Windows 11 troubleshooting.
* **Cloud Infrastructure:** EC2 launch configuration and remote access management.
* **Cost Optimization:** Identification and removal of unused AWS resources.

---

### Conclusion
After resolving the driver lock and infrastructure issues, both systems successfully completed migration to AWS EC2. The environment is now stable, replication health checks passed, and unnecessary cloud resources were removed to control costs.
