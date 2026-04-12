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

## Technical Support Fundamentals – Systems Analysis

These scenarios demonstrate how foundational computing concepts are applied to understand system behavior, data representation, and low-level processing in real-world environments.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>1. Binary Systems, Data Representation and Logic Gates</h5>
<p><strong>Scenario:</strong> Limited understanding of how computers process binary data, leading to gaps in troubleshooting, data interpretation, and low-level system analysis.</p>
<p><strong>Resolution:</strong> Analyzed binary-to-decimal conversion, character encoding (ASCII/UTF-8), and logic gate operations to establish a clear model of how data is processed and represented within computing systems.</p>
<p><strong>Validation:</strong> Verified accuracy through binary conversion exercises, ASCII mapping validation, and logic gate truth table analysis to confirm correct system behavior.</p>
<p><strong>Framework Alignment:</strong> Operational Approach · System Analysis · Data Representation · Foundational Computing</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-binary-systems-data-representation-logic-gates/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

</div>

---

## Applied Troubleshooting

These scenarios demonstrate how I apply structured troubleshooting, control enforcement, and validation to real-world security and infrastructure problems.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>1. Prompt & Rubric Evaluation</h5>
<p><strong>Scenario:</strong> Evaluation of technical prompts and rubrics suffering from ambiguity, inconsistent grading, and unclear success criteria.</p>
<p><strong>Resolution:</strong> Refined prompts and rubric structures by enforcing clear objectives, measurable criteria, and single-purpose instructions to improve consistency and reduce interpretation errors.</p>
<p><strong>Validation:</strong> Tested revised rubrics against sample technical reports to confirm consistent scoring, objective evaluation, and repeatability across different inputs.</p>
<p><strong>Framework Alignment:</strong> Operational Approach · Quality Assurance · Process Standardization · Evaluation Consistency</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-prompts-rubrics-evaluation-exercises/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>2. AD Disaster Recovery & Identity Restoration</h5>
<p><strong>Scenario:</strong> Complete loss of a Domain Controller resulting in an identity blackout for 100+ users.</p>
<p><strong>Resolution:</strong> Rebuilt the server and performed a system state restore using <strong>Directory Services Restore Mode (DSRM)</strong>.</p>
<p><strong>Validation:</strong> Verified system integrity using <code>dcdiag</code> and <code>repadmin</code> to confirm replication health and data consistency.</p>
<p><strong>Framework Alignment:</strong> Business Continuity Planning (BCP).</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-ad-disaster-recovery-identity-restoration-v1.0.2/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>3. Access Control & NIST Alignment (Least Privilege)</h5>
<p><strong>Scenario:</strong> Data exposure caused by permission creep and lack of enforced access controls.</p>
<p><strong>Resolution:</strong> Mapped controls to NIST 800-53 (AC-6) and implemented Role-Based Access Control (RBAC).</p>
<p><strong>Validation:</strong> Performed negative testing across user roles to confirm enforcement of access restrictions.</p>
<p><strong>Framework Alignment:</strong> Principle of Least Privilege (POLP).</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/sop-access-control-incident-nist-alignment/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>4. System Hardening: Windows Defender GPO</h5>
<p><strong>Scenario:</strong> Default AV configurations vulnerable to tampering and ransomware bypass.</p>
<p><strong>Resolution:</strong> Enforced a hardened baseline through Group Policy to maintain real-time protection and cloud-based scanning.</p>
<p><strong>Validation:</strong> Confirmed controls remained enforced against local administrative override attempts.</p>
<p><strong>Framework Alignment:</strong> CIS Microsoft Windows Desktop Benchmark.</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/sop-hardening-windows-defender-using-local-gpo/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255255255,0.1);">
<h5>5. RDP Troubleshooting (AWS Hybrid Cloud)</h5>
<p><strong>Scenario:</strong> Persistent RDP failures impacting access to AWS-hosted systems.</p>
<p><strong>Resolution:</strong> Audited AWS Security Groups, Network ACLs, and OS-level Remote Desktop configurations.</p>
<p><strong>Validation:</strong> Identified and corrected misconfigured ingress rules, restoring secure connectivity.</p>
<p><strong>Framework Alignment:</strong> ITIL Incident Management / NIST CSF (RS.AN).</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-rdp-troubleshooting-aws-users/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>6. Remote Access & Network Isolation (RDP + GPO + Dual-Homed)</h5>
<p><strong>Scenario:</strong> Connectivity and authentication failures between a macOS host and a Windows 11 virtual machine due to Group Policy conflicts and improper network segmentation.</p>
<p><strong>Resolution:</strong> Resolved conflicting Group Policy “Deny” rules, corrected Remote Desktop access permissions, and implemented a dual-homed network architecture separating management and internet traffic.</p>
<p><strong>Validation:</strong> Confirmed successful Remote Desktop authentication from the macOS host while maintaining simultaneous internet connectivity via a bridged adapter, ensuring both isolation and usability.</p>
<p><strong>Framework Alignment:</strong> NIST CSF (PR.AC, PR.IP) · ISO 27001 Remote Access Controls · Principle of Least Privilege</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/troubleshooting-remote-access-network-isolation/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>7. Physical Layer RCA: Workstation Power Failure</h5>
<p><strong>Scenario:</strong> Spontaneous "hard" shutdowns on a database workstation following a storage expansion, with no OS-level error logging.</p>
<p><strong>Resolution:</strong> Conducted a TDP (Thermal Design Power) audit and identified a wattage deficit. Replaced the legacy 300W PSU with a 600W unit to support increased SATA drive draw.</p>
<p><strong>Validation:</strong> Performed a 72-hour stress test under maximum I/O load to verify stability during peak power-draw windows.</p>
<p><strong>Framework Alignment:</strong> Physical Layer Diagnostics · Infrastructure Lifecycle Management · NIST CSF (PR.DS-4)</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-workstation-power-failure-investigation/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>8. USB Passthrough & Filesystem Recovery (Windows VM)</h5>
<p><strong>Scenario:</strong> USB device detected on the host but not accessible within a Windows 10 virtual machine, with additional “Cannot open volume for direct access” errors.</p>
<p><strong>Resolution:</strong> Configured VirtualBox USB filters to enforce consistent hardware passthrough and resolved volume lock issues by dismounting the drive and running <code>chkdsk E: /x /f /v</code>.</p>
<p><strong>Validation:</strong> Verified volume detection using <code>diskpart</code>, confirmed successful read/write operations, and exported <code>chkdsk</code> logs via <code>wevtutil</code> to validate filesystem integrity.</p>
<p><strong>Framework Alignment:</strong> Structured Troubleshooting · Root Cause Analysis · Filesystem Integrity Validation · NIST CSF (PR.DS-4)</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-restore-usb-access-windows-10-vm/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>9. USB Filesystem Corruption (Improper Removal)</h5>
<p><strong>Scenario:</strong> USB device became unreadable after use in a virtualized environment, with no visibility in File Explorer or disk tools.</p>
<p><strong>Resolution:</strong> Performed layered troubleshooting (Device Manager, Disk Management, diskpart) and isolated the issue to filesystem corruption caused by improper removal during an active <code>chkdsk</code> operation.</p>
<p><strong>Validation:</strong> Confirmed hardware functionality via port isolation and device detection. Verified corruption through forced format prompt and inability to mount the filesystem.</p>
<p><strong>Framework Alignment:</strong> Root Cause Analysis · Operational Troubleshooting · Data Integrity · NIST CSF (PR.DS-4)</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-usb-filesystem-corruption/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>10. USN Journal Forensics & Timeline Reconstruction</h5>
<p><strong>Scenario:</strong> Standard file timestamps could be manipulated (timestomping), creating gaps in forensic visibility during investigations.</p>
<p><strong>Resolution:</strong> Leveraged <code>fsutil</code> to analyze the NTFS USN Journal, extracting reason codes and sequential records to reconstruct file activity and detect potential tampering.</p>
<p><strong>Validation:</strong> Created, renamed, and deleted test files to confirm that the USN Journal recorded file activity and maintained sequential logging behavior.</p>
<p><strong>Framework Alignment:</strong> Incident Response · Forensic Analysis · File Integrity Monitoring · NIST CSF (DE.AE, RS.AN)</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-usn-journal-analysis/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>11. Windows Disk Management with CHKDSK and FSUTIL</h5>
<p><strong>Scenario:</strong> Risk of undetected filesystem corruption and unreliable storage due to lack of structured disk monitoring and validation processes.</p>
<p><strong>Resolution:</strong> Implemented a standardized disk management approach using <code>chkdsk</code> for repair operations and <code>fsutil</code> for deep filesystem analysis, including dirty bit checks, self-healing status, and NTFS metadata validation.</p>
<p><strong>Validation:</strong> Verified disk integrity through verbose <code>chkdsk</code> scans, confirmed clean volume states using <code>fsutil dirty query</code>, and validated file activity tracking through USN Journal analysis.</p>
<p><strong>Framework Alignment:</strong> Operational Troubleshooting · Filesystem Integrity · Preventive Maintenance · NIST CSF (PR.DS-4)</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-windows-disk-management-chkdsk-fsutil/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>12. USB Storage Failure Analysis and Disk Validation</h5>
<p><strong>Scenario:</strong> USB storage device appeared accessible but showed instability, repeated CHKDSK failures, and system unresponsiveness, creating risk of hidden hardware failure and data loss.</p>
<p><strong>Resolution:</strong> Performed structured troubleshooting across VM and host systems, including CHKDSK repair attempts, drive reassignment, and full (non-quick) format testing to validate sector-level integrity and isolate hardware failure.</p>
<p><strong>Validation:</strong> Confirmed persistent CHKDSK errors, full format failure at 0%, and system I/O lock condition. Verified failure across both virtual and physical environments, with system recovery only after physical device removal.</p>
<p><strong>Framework Alignment:</strong> Applied Troubleshooting · Hardware Failure Analysis · Storage Integrity · NIST CSF (PR.DS-4, ID.AM-1)</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-usb-storage-failure-analysis/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

</div>

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h2>Technical Stack</h2>

<p><strong>Virtualization:</strong> VMware, VirtualBox, AWS EC2, GCP</p>

<p><strong>Defensive Tools:</strong> pfSense, OpenVPN, Windows Defender, GPO Baselines, OpenVAS</p>

<p><strong>Diagnostics & Network Analysis:</strong> Procmon, SAR (Linux), Wireshark, Event Viewer, Nmap, sslscan, Fierce</p>

<p><strong>Penetration Testing:</strong> Burp Suite (Spider, Intruder)</p>

<p><strong>Recon & OSINT:</strong> dnsdumpster.com, shodan.io, dnstwist.py, urlscan.io, Google Dorking, Bing</p>

<p><strong>Threat Hunting & Forensics:</strong> YARA, Dumpzilla, PE Studio</p>

<p><strong>Research & Analysis:</strong> Elicit.org, MITRE ATT&CK, Cyber Kill Chain</p>

<p><strong>Documentation:</strong> 100+ structured reports using a Layer → Device → Root Cause framework.</p>

</div>

</div>

## Application Across Portfolio

This operational approach is applied across all technical investigations in my portfolio, ensuring that security controls are not only implemented, but tested, validated, and continuously improved through structured analysis.
