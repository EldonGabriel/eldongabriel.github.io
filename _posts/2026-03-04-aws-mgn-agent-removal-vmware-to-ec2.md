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

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>

This project focused on moving virtual machines from a VMware lab to AWS EC2 using AWS Application Migration Service (MGN).

The lab was built using limited resources (32 GB RAM), so I used nested virtualization to simulate a real enterprise setup. A Domain Controller handled DNS and routing, while ESXi and vCenter managed the virtual machines.

**Tools and Techniques:** VMware vSphere 8.0, AWS MGN, PowerShell, Windows Server (RRAS/NAT), and Safe Mode troubleshooting.

**Key Frameworks:** Hybrid-Cloud, FinOps (cost control), and Root Cause Analysis (RCA).

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>

**Hands-on Skills:**  
I built a working DNS environment using both A and PTR records so systems could resolve names and IPs correctly. I also configured AWS MGN replication and used AWS Systems Manager (SSM) for managing the new EC2 instances.

**Observations:**  
A migration is not finished just because the system boots. Even after a successful test launch, the system can still depend on old drivers from VMware.

**Troubleshooting Lessons:**  
I forced a failure by removing AWS drivers after migration. This caused the system to crash due to a mismatch between BIOS/EFI and GPT settings. To fix it, I switched firmware modes, rebuilt boot settings (BCD), and installed a second OS to recover the data.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>

**Enterprise Security:**  
More than 300 unused AWS resources were left behind after testing. These increase both cost and security risk if not removed.

**Operational Defense:**  
Knowing how to recover from a system failure like this helps protect important data, even if the OS stops working.

**Real-World Analogy:**  
Moving a system between platforms is like moving an engine into a different car. If the parts don’t match, it won’t run properly.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job / Framework</h1>
</div>

- **NIST NICE – Systems Architecture (SP-ARC)**
- **ASD Cyber Skills Framework – Systems Development (SDEV)**

These skills apply directly to cloud migration, system recovery, and infrastructure management roles.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>

- DNS must be configured correctly. Both A and PTR records are required  
- A successful boot does not mean the migration is complete  
- Firmware and partition types (BIOS vs EFI, MBR vs GPT) must match  
- Cleaning up unused cloud resources reduces cost and risk  
- Always protect data before making major system changes  

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

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Technical Skills Demonstrated</h1>
</div>

* **Cloud Migration:** VMware to AWS EC2 using AWS MGN  
* **Infrastructure Setup:** DNS, NAT routing, and vCenter deployment  
* **Troubleshooting:** Windows recovery, Safe Mode fixes, and driver issues  
* **Cloud Operations:** EC2 setup and Systems Manager (SSM)  
* **Cost Control:** Cleanup of unused AWS resources  

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Conclusion</h1>
</div>

This project showed the full migration process from setup to recovery. The systems successfully moved to AWS, but testing also showed how easy it is to break things if drivers and settings are not aligned.

After fixing the failure and recovering the system, all data was preserved and the environment was cleaned up. This reinforced the importance of testing, troubleshooting, and cost control in cloud projects.

