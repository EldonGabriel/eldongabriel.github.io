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

### The Challenge: Too Many Resources via AWS Transform
AWS Transform created a large amount of extra supporting infrastructure across different regions. This led to cloud resource sprawl that needed to be reviewed and removed.

### Leftover Processes in Task Manager
After the migration, the replication agent processes remained active on the original systems. These processes continued running even after the migration was complete.

### Problem Removing Kernel Driver
The uninstaller could not remove the replication driver. The driver remained in memory, which prevented the Amazon installation files from being deleted.

---

### Key Technical Hurdles

**File Lock Problem**

The replication driver locked files inside the installation folder. Standard administrative tools could not remove the files while the driver was active.

**Safe Mode Solution**

Booting the system into Safe Mode prevented the driver from loading during startup. This made it possible to safely remove the installation folder and related registry entries.

---

### The Engineering Solution
The problem was resolved by isolating the kernel driver, removing the locked files, and stabilizing the migration environment. Additional troubleshooting steps fixed network performance and cloud configuration issues.  

After the fixes were applied, the environment was reviewed to confirm that the migrated systems were running correctly in the cloud.

---

### Full Technical Guide (PDF)
The full process is documented in the complete report. It includes:

* VMware to AWS migration setup  
* AWS replication agent troubleshooting  
* Kernel driver removal and Safe Mode remediation  
* Network performance troubleshooting and VPN interference  
* Cloud launch configuration and EC2 access restoration  
* Cost analysis and removal of unused cloud resources  

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Engineering Report: VMware to AWS EC2 Migration</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->
<div style="flex:0 1 500px; background:rgba(255,255,255,0.05); padding:20px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/reports/IR – AWS MGN Agent Removal & Environment Cleanup – v1.0.0.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:12px; color:#aaa;">
<strong>IR – AWS MGN Agent Removal & Environment Cleanup – v1.0.0.pdf</strong>
</p>

</div>

</div>

---

### Technical Skills Demonstrated
* **Cloud Migration:** VMware virtual machine migration to AWS EC2 using AWS MGN.
* **Operating Systems:** Windows Server and Windows 11 troubleshooting.
* **Kernel Troubleshooting:** Driver lock identification and Safe Mode remediation.
* **Cloud Infrastructure:** EC2 launch configuration and remote access management.
* **Cost Optimization:** Identification and removal of unused AWS resources.

---

### Conclusion
After resolving the driver lock and infrastructure issues, both systems successfully completed migration to AWS EC2. The environment is now stable, replication health checks passed, and unnecessary cloud resources were removed to control costs.
