---
layout: home
title: Security Systems Specialist
permalink: /test/
image:
  path: /assets/images/banner.png
---

---
title: "Operational Philosophy & Troubleshooting Framework"
layout: collection-item
slug: operational-philosophy
collection: certifications
collection_item: true
order: 1
image:
  path: /assets/images/headers/ops-phi.png
  thumbnail: /assets/images/headers/ops-phi.png
  caption: "Logic-Driven Troubleshooting & Security Baselines"
---

<p style="text-align:center; font-size: 1.1em; color: #fff; background: rgba(255,255,255,0.05); padding: 15px; border-radius: 8px;">
  <strong>Core Pillars:</strong> Structured Troubleshooting · NIST/CIS Alignment · Negative Testing · Root Cause Analysis
</p>

### **Operational Philosophy**
My approach to IT Support and System Administration is built on the principle that **stability is a product of security.** I don't just resolve tickets; I harden systems to prevent the next incident.

> **On Automation:** "I believe security shouldn't be optional for the user; it should be an enforced technical baseline."
> 
> **On Compliance:** "I don't just change settings; I align my configurations with industry standards like NIST 800-53 and CIS Benchmarks."
> 
> **On Troubleshooting:** "My process always includes a validation phase—I use negative testing to prove the security controls actually hold."

---

### **Technical Troubleshooting Scenarios (The Hero Labs)**
The following scenarios represent my "Anchor Labs"—complex problems solved using a structured, multi-layer diagnostic approach.

#### **1. AD Disaster Recovery & Identity Restoration**
* **The Scenario:** Complete loss of a Domain Controller resulting in an identity blackout for 100+ users.
* **The Resolution:** Rebuilt the server and performed a system state restore using **Directory Services Restore Mode (DSRM)**. 
* **Validation:** Verified environment health using `dcdiag` and `repadmin` to ensure zero data loss and full replication.
* **Framework:** Business Continuity Planning (BCP).

#### **2. System Hardening: Windows Defender GPO**
* **The Scenario:** Default AV settings vulnerable to being disabled by local users or ransomware.
* **The Resolution:** Implemented an **Immutable Baseline** via Group Policy to enforce real-time protection and cloud-based scanning.
* **Validation:** Performed command-line checks to confirm settings remained enforced even against local administrative overrides.
* **Framework:** CIS Microsoft Windows Desktop Benchmark.

#### **3. RDP Troubleshooting (AWS Hybrid Cloud)**
* **The Scenario:** Persistent RDP connection failures for AWS-hosted virtual machines.
* **The Resolution:** Conducted a multi-layer audit of **AWS Security Groups**, **Network ACLs**, and OS-level Remote Desktop Services.
* **Validation:** Identified and corrected misconfigured ingress rules, restoring stable cross-platform connectivity.
* **Framework:** ITIL Incident Management / NIST CSF (RS.AN).

#### **4. Access Control & NIST Alignment (Least Privilege)**
* **The Scenario:** Confidential data leak caused by "permission creep" and lack of technical controls.
* **The Resolution:** Mapped the environment to **NIST 800-53 (AC-6)**. Restructured NTFS permissions to a Role-Based Access Control (RBAC) model.
* **Validation:** Conducted "Negative Testing" with different user roles to confirm data isolation and restricted PowerShell execution.
* **Framework:** Principle of Least Privilege (POLP).

---

### **My Technical Stack for Support Adventure**
* **Virtualization:** VMware, VirtualBox, AWS EC2, GCP.
* **Defensive Tools:** pfSense, OpenVPN, Windows Defender, GPO Baselines.
* **Diagnostics:** Procmon (Process Monitor), SAR (Linux), SAR, Wireshark, Event Viewer.
* **Documentation:** 100+ Structured Reports using the **Layer → Device → Root Cause** framework.

<p align="center" style="margin-top: 40px;">
  <a href="/experience/" class="btn" style="padding: 10px 20px; background: #fff; color: #000; text-decoration: none; border-radius: 5px; font-weight: bold;">
    View Full Lab Reports
  </a>
</p>
