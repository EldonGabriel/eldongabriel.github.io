---
layout: home
title: Security Systems Specialist
permalink: /test/
image:
  path: /assets/images/banner.png
---

---
title: "Applying Least Privilege in Risk Assessment (NIST SP 800-53 AC-6)"
date: 2026-03-17
author: Eldon Gabriel
tags: [Cybersecurity, Access Control, NIST, Governance, Risk Management]
excerpt: "Applying the principle of least privilege to reduce risk through controlled access, monitoring, and role-based security models."
image:
  path: "/assets/images/nist800-53.png"
  thumbnail: "/assets/images/nist800-53.png"
---

---
title: "Resolving AWS MGN Agent Removal Issues After VMware to EC2 Migration"
date: 2026-03-04
author: Eldon Gabriel
tags: [AWS, Cloud Migration, VMware, Troubleshooting, Infrastructure]
excerpt: "A hybrid-cloud migration case study covering VMware to AWS EC2 replication, DNS architecture, and post-migration driver failure recovery using AWS MGN."
image:
  path: /assets/images/posts/vmware-aws-migration.png
  thumbnail: /assets/images/posts/vmware-aws-migration.png
---

# Resolving AWS MGN Agent Removal Issues After VMware to EC2 Migration

## What I Studied

This project focused on an end-to-end hybrid-cloud migration from a VMware-based on-premises lab to AWS EC2 using the AWS Application Migration Service (MGN).

The environment was built under constrained resources (32 GB RAM) using nested virtualization. Core infrastructure included a Domain Controller (DC01) acting as DNS authority and NAT gateway, alongside ESXi and a vCenter Server Appliance (VCSA) to simulate enterprise architecture.

**Tools and Techniques:** VMware vSphere 8.0, AWS MGN, PowerShell (DNS automation), Windows Server (RRAS/NAT), and Safe Mode recovery techniques.

**Key Frameworks:** Hybrid-Cloud Interoperability, FinOps (cost control and resource hygiene), and Root Cause Analysis (RCA) through controlled failure injection.

---

## What I Learned

**Hands-on Skills:**  
Built a full DNS “source of truth” using forward (A) and reverse (PTR) records to support vCenter deployment and hybrid communication. Configured AWS MGN replication, staging environments, and Default Host Management Configuration (DHMC) for EC2 management via Systems Manager.

**Observations:**  
Migration success is not defined by instance launch alone. Test launch validation confirmed OS survivability, but underlying driver dependencies remained tied to the original VMware environment.

**Troubleshooting Lessons:**  
A controlled failure was introduced by manually removing AWS drivers post-migration. This caused a Hardware Abstraction Layer (HAL) failure due to mismatch between BIOS/EFI and GPT partitioning. Recovery required firmware correction (BIOS → EFI), Boot Configuration Data (BCD) reconstruction, and parallel OS installation to preserve data.

---

## Why It Matters

**Enterprise Security:**  
Over 300 orphaned AWS resources were identified and removed. Unused infrastructure increases both attack surface and operational cost.

**Operational Defense:**  
The ability to recover from a HAL failure ensures data persistence even when the operating system becomes unbootable.

**Real-World Analogy:**  
Migrating a system between hypervisors is like moving an engine into a different chassis. Without replacing the mounting components (drivers and firmware alignment), failure is inevitable.

---

## How It Maps to the Job / Framework

- **NIST NICE – Systems Architecture (SP-ARC)**
- **ASD Cyber Skills Framework – Systems Development (SDEV)**

This work aligns with real-world responsibilities in cloud engineering and system administration, including infrastructure design, migration validation, failure recovery, and cost governance.

---

## Key Takeaways

- DNS is a hard dependency. Missing A and PTR records will break vCenter deployment and hybrid communication  
- Migration validation must include test launches, not just replication completion  
- Driver and firmware alignment (BIOS vs EFI, MBR vs GPT) is critical post-migration  
- FinOps is part of security. Resource cleanup reduces both cost and exposure  
- Data preservation strategies must be in place before destructive recovery actions  

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->
<div style="max-width:500px; margin:0 auto; background:rgba(255,255,255,0.05); padding:12px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/reports/REPORT – Enterprise Hybrid-Cloud Migration – v1.2.0.pdf' | relative_url }}"
width="100%"
height="600"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:8px; color:#aaa; font-size:0.9em;">
<strong>REPORT – Enterprise Hybrid-Cloud Migration – v1.2.0.pdf</strong>
</p>

</div>

</div>

---

### Technical Skills Demonstrated
* **Cloud Migration:** VMware to AWS EC2 using AWS Application Migration Service (MGN)  
* **Infrastructure Design:** DNS architecture, NAT routing (RRAS), and vCenter deployment  
* **Operating Systems:** Windows Server recovery, HAL troubleshooting, and Safe Mode remediation  
* **Cloud Operations:** EC2 validation, Systems Manager (SSM), and launch configuration  
* **FinOps:** Identification and cleanup of orphaned AWS resources  

---

### Conclusion

This project validated a full hybrid-cloud migration workflow, from infrastructure setup to AWS replication and post-migration recovery. While initial test launches confirmed successful migration, the controlled removal of drivers exposed critical dependencies between firmware, partitioning, and operating system stability.

Through structured Root Cause Analysis, the system was recovered without data loss, and the environment was stabilized. Final cleanup ensured minimal resource waste, reinforcing the importance of combining technical execution with cost and security awareness.
