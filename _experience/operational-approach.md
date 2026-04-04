---
title: "Operational Approach"
layout: collection-item
slug: operational-approach
collection: certifications
collection_item: true
order: 1
image:
  path: /assets/images/headers/ops-app.png
  thumbnail: /assets/images/headers/ops-app.png
  caption: "Logic-Driven Troubleshooting & Security Baselines"
---

This section outlines the operational approach I use to implement, validate, and troubleshoot security controls across enterprise systems.

- Apply a structured troubleshooting framework (Layer → Device → Root Cause → Resolution)  
- Enforce security baselines aligned with NIST and CIS standards  
- Validate all fixes through testing, including negative testing  
- Prioritize long-term control effectiveness over temporary fixes  

<p style="text-align:center; font-size: 1.1em; color: #fff; background: rgba(255,255,255,0.05); padding: 15px; border-radius: 8px;">
  <strong>Core Pillars:</strong> Structured Troubleshooting · Security Control Enforcement · RCA · Validation Testing
</p>

---

## Applied Troubleshooting (Examples)

These scenarios demonstrate how I apply structured troubleshooting, control enforcement, and validation to real-world security and infrastructure problems.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>1. Prompt & Rubric Evaluation – Structured Assessment Design</h5>
<p><strong>Scenario:</strong> Evaluation of technical prompts and rubrics suffering from ambiguity, inconsistent grading, and unclear success criteria.</p>
<p><strong>Resolution:</strong> Refined prompts and rubric structures by enforcing clear objectives, measurable criteria, and single-purpose instructions to improve consistency and reduce interpretation errors.</p>
<p><strong>Validation:</strong> Tested revised rubrics against sample technical reports to confirm consistent scoring, objective evaluation, and repeatability across different inputs.</p>
<p><strong>Framework Alignment:</strong> Operational Approach · Quality Assurance · Process Standardization · Evaluation Consistency</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-prompt-rubric-evaluation-exercises-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>2. AD Disaster Recovery & Identity Restoration</h5>
<p><strong>Scenario:</strong> Complete loss of a Domain Controller resulting in an identity blackout for 100+ users.</p>
<p><strong>Resolution:</strong> Rebuilt the server and performed a system state restore using <strong>Directory Services Restore Mode (DSRM)</strong>.</p>
<p><strong>Validation:</strong> Verified system integrity using <code>dcdiag</code> and <code>repadmin</code> to confirm replication health and data consistency.</p>
<p><strong>Framework Alignment:</strong> Business Continuity Planning (BCP).</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-ad-disaster-recovery-identity-restoration-v1.0.2/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>3. System Hardening: Windows Defender GPO</h5>
<p><strong>Scenario:</strong> Default AV configurations vulnerable to tampering and ransomware bypass.</p>
<p><strong>Resolution:</strong> Enforced a hardened baseline through Group Policy to maintain real-time protection and cloud-based scanning.</p>
<p><strong>Validation:</strong> Confirmed controls remained enforced against local administrative override attempts.</p>
<p><strong>Framework Alignment:</strong> CIS Microsoft Windows Desktop Benchmark.</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/sop-hardening-windows-defender-using-local-gpo/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>4. Access Control & NIST Alignment (Least Privilege)</h5>
<p><strong>Scenario:</strong> Data exposure caused by permission creep and lack of enforced access controls.</p>
<p><strong>Resolution:</strong> Mapped controls to NIST 800-53 (AC-6) and implemented Role-Based Access Control (RBAC).</p>
<p><strong>Validation:</strong> Performed negative testing across user roles to confirm enforcement of access restrictions.</p>
<p><strong>Framework Alignment:</strong> Principle of Least Privilege (POLP).</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/access-control-incident-analysis/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>5. RDP Troubleshooting (AWS Hybrid Cloud)</h5>
<p><strong>Scenario:</strong> Persistent RDP failures impacting access to AWS-hosted systems.</p>
<p><strong>Resolution:</strong> Audited AWS Security Groups, Network ACLs, and OS-level Remote Desktop configurations.</p>
<p><strong>Validation:</strong> Identified and corrected misconfigured ingress rules, restoring secure connectivity.</p>
<p><strong>Framework Alignment:</strong> ITIL Incident Management / NIST CSF (RS.AN).</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/rdp-troubleshooting-aws/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a>
</p>
</div>

</div>

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h2>Technical Stack</h2>
<p><strong>Virtualization:</strong> VMware, VirtualBox, AWS EC2, GCP</p>
<p><strong>Defensive Tools:</strong> pfSense, OpenVPN, Windows Defender, GPO Baselines</p>
<p><strong>Diagnostics:</strong> Procmon, SAR (Linux), Wireshark, Event Viewer</p>
<p><strong>Documentation:</strong> 100+ structured reports using a Layer → Device → Root Cause framework.</p>
</div>

</div>

## Application Across Portfolio

This operational approach is applied across all technical investigations in my portfolio, ensuring that security controls are not only implemented, but tested, validated, and continuously improved through structured analysis.
