---
title: "Operational Approach"
layout: home
title: Security Systems Specialist
permalink: /test/
image:
  path: /assets/images/banner.png
---

---
title: "Operational Approach"
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
  <strong>Core Pillars:</strong> Structured Troubleshooting · Security-First Thinking · Root Cause Analysis · Validation Testing
</p>

---

## Problem Solving Approach

My approach to IT support and system administration is based on structured troubleshooting and security-first thinking. I focus on identifying root causes, validating fixes, and applying controls that prevent repeat issues.

- Use a consistent troubleshooting framework (Layer → Device → Root Cause → Resolution)  
- Apply security baselines aligned with NIST and CIS standards  
- Validate fixes through testing, including negative testing  
- Focus on long-term stability, not just short-term fixes  

---

## Technical Troubleshooting Scenarios

These scenarios demonstrate how I approach real-world problems using structured troubleshooting and validation.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>1. AD Disaster Recovery & Identity Restoration</h5>
<ul>
<li><strong>The Scenario:</strong> Complete loss of a Domain Controller resulting in an identity blackout for 100+ users.</li>
<li><strong>The Resolution:</strong> Rebuilt the server and performed a system state restore using <strong>Directory Services Restore Mode (DSRM)</strong>.</li>
<li><strong>Validation:</strong> Verified environment health using <code>dcdiag</code> and <code>repadmin</code> to ensure full replication and no data loss.</li>
<li><strong>Framework:</strong> Business Continuity Planning (BCP).</li>
</ul>
<p align="center" style="margin-top:20px;"><a href="#" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>2. System Hardening: Windows Defender GPO</h5>
<ul>
<li><strong>The Scenario:</strong> Default AV settings vulnerable to user tampering and ransomware bypass.</li>
<li><strong>The Resolution:</strong> Implemented an enforced baseline via Group Policy to maintain real-time protection and cloud-based scanning.</li>
<li><strong>Validation:</strong> Confirmed settings remained enforced against local administrative changes.</li>
<li><strong>Framework:</strong> CIS Microsoft Windows Desktop Benchmark.</li>
</ul>
<p align="center" style="margin-top:20px;"><a href="#" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>3. RDP Troubleshooting (AWS Hybrid Cloud)</h5>
<ul>
<li><strong>The Scenario:</strong> Persistent RDP connection failures for AWS-hosted virtual machines.</li>
<li><strong>The Resolution:</strong> Audited AWS Security Groups, Network ACLs, and OS-level Remote Desktop Services.</li>
<li><strong>Validation:</strong> Identified and corrected misconfigured ingress rules, restoring connectivity.</li>
<li><strong>Framework:</strong> ITIL Incident Management / NIST CSF (RS.AN).</li>
</ul>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/rdp-troubleshooting-aws/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>4. Access Control & NIST Alignment (Least Privilege)</h5>
<ul>
<li><strong>The Scenario:</strong> Data exposure caused by permission creep and lack of access control enforcement.</li>
<li><strong>The Resolution:</strong> Mapped environment to NIST 800-53 (AC-6) and implemented Role-Based Access Control (RBAC).</li>
<li><strong>Validation:</strong> Performed negative testing across user roles to confirm access restrictions.</li>
<li><strong>Framework:</strong> Principle of Least Privilege (POLP).</li>
</ul>
<p align="center" style="margin-top:20px;"><a href="#" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a></p>
</div>

</div>

---

## Technical Stack

- **Virtualization:** VMware, VirtualBox, AWS EC2, GCP  
- **Defensive Tools:** pfSense, OpenVPN, Windows Defender, GPO Baselines  
- **Diagnostics:** Procmon, SAR (Linux), Wireshark, Event Viewer  
- **Documentation:** 100+ structured reports using a Layer → Device → Root Cause framework  

---

<p align="center" style="margin-top: 40px;">
  <a href="/experience/" class="btn" style="padding: 10px 20px; background: #fff; color: #000; text-decoration: none; border-radius: 5px; font-weight: bold;">
    View Full Lab Reports
  </a>
</p>
