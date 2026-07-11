---
title: "Security Operations"
layout: collection-item
slug: security-operations
collection: experience
collection_item: true
order: 5
permalink: /security-operations/
image:
  path: /assets/images/headers/section-header.png
  thumbnail: /assets/images/headers/section-header.png
  caption: "Security Operations, Hardening, and Monitoring Labs"
---

## Security Operations Laboratory Overview

<p style="line-height:1.6; font-size:1.05em;">
Security operations help organizations detect threats, protect critical systems, and maintain confidence in their technology environments. Effective security requires more than installing tools; it requires continuous monitoring, secure configuration, incident analysis, and validation that security controls operate as intended.
</p>

<p style="line-height:1.6; font-size:1.05em;">
This section demonstrates hands-on security operations practices across endpoint protection, network defense, vulnerability assessment, monitoring, incident response, and infrastructure recovery. Each lab focuses on identifying risks, applying security controls, investigating system behavior, and validating improvements through practical testing.
</p>

<p style="line-height:1.6; font-size:1.05em;">
The objective is to demonstrate how security operations reduce exposure, improve visibility, support faster incident response, and strengthen the reliability of IT environments through repeatable defensive practices.
</p>

### Lab Distribution Summary

| Category | Labs |
|--------|------|
| Perimeter Defense & Secure Connectivity | 4 |
| Endpoint Hardening & Access Control | 9 |  
| Infrastructure Protection & Recovery | 1 | 
| Threat Hunting & Malware Analysis | 1 |
| Incident Response & Monitoring | 2 |
| Lab Demonstrations |  8 |
| **Total Security Operations Labs Documented** | **25** |

<hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

### 🛡️ Perimeter Defense & Secure Connectivity

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Enterprise IPsec VPN Diagnostics – v1.0.0</h5>
<p>Demonstrates building and validating a site-to-site IPsec VPN between enterprise locations to secure data in transit over untrusted networks.</p>
<p><strong>Skills:</strong> IPsec VPN · IKE · ACLs </p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-enterprise-ipsec-vpn-dianogstics-v1.0.0/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – pfSense IDS Traffic Monitoring and EternalBlue Detection – v1.0.0</h5>
<p>Overview of firewall technologies and their role in enforcing network perimeter security.</p>
<p><strong>Skills:</strong> Network Security · Perimeter Defense · Firewall Policy</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/pfsense-ids-traffic-monitoring/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – OpenVPN Remote Access Deployment and Validation – v1.0.0</h5>
<p>Deployment and validation of an OpenVPN remote access solution to provide secure connectivity for remote systems.</p>
<p><strong>Skills:</strong> VPN Deployment · Encryption · Secure Remote Access</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/openvpn-remote-access-vpn-deployment-validation/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Troubleshooting pfSense DNS Resolution – v1.0.0</h5>
<p>Demonstrates diagnosing and resolving DNS failures in a hardened pfSense environment by enforcing controlled access under a default-deny firewall policy.</p>
<p><strong>Skills:</strong> DNS Troubleshooting · pfSense · Network Diagnostics</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-troubleshooting-pfsense-dns-resolution/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Report</a>
</p>
</div>

</div>

### 🔐 Endpoint Hardening & Access Control

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Deploy Controlled Folder Access via Local GPO – v1.0.0</h5>
<p>Implemented Controlled Folder Access (CFA) using Local Group Policy to restrict unauthorized applications from modifying protected directories and mitigate ransomware-based file encryption risks.</p>
<p><strong>Skills:</strong> CFA · Endpoint Hardening · GPO Security · Ransomware Defense</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-deploy-controlled-folder-access-local-gpo/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Hardening UAC via Local Group Policy – v1.0.0</h5>
<p>Implemented hardened User Account Control (UAC) settings using Local Group Policy to enforce credential-based elevation and secure desktop protections against privilege escalation.</p>
<p><strong>Skills:</strong> UAC Hardening · Privilege Management · GPO Security · Secure Desktop</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-hardening-uac-local-gpo/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – OS Patching Enforcement via Local GPO – v1.0.0</h5>
<p>Implemented automated OS patching using Local Group Policy to reduce vulnerability exposure while maintaining system availability.</p>
<p><strong>Skills:</strong> Patch Management · GPO Configuration · Endpoint Hardening · Update Policy Enforcement</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-os-patching-enforcement-local-gpo-v.1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Hardening Microsoft Edge via Local GPO – v1.0.0</h5>
<p>Hardened Microsoft Edge using Local Group Policy to reduce attack surface and enforce secure browser configurations.</p>
<p><strong>Skills:</strong> Browser Hardening · GPO Configuration · Endpoint Security</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-harden-microsoft-edge-local-gpo-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Applying a Local GPO for Session Lock Enforcement – v1.0.0</h5>
<p>Configured session lock policies using Local Group Policy to automatically secure idle systems and reduce unauthorized access risk.</p>
<p><strong>Skills:</strong> GPO Configuration · Endpoint Hardening · Access Control Enforcement</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-gpo-applying-local-gpo-session-lock-enforcement-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – SMB Hardening for Credential Theft Protection – v1.0.0</h5>
<p>Applied SMB security policies to reduce exposure to credential harvesting and lateral movement.</p>
<p><strong>Skills:</strong> SMB Hardening · Credential Protection · Lateral Movement Mitigation</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-smb-hardening-credential-theft-protection-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Endpoint Security with Windows Registry – v1.0.0</h5>
<p>Demonstrates using Windows Registry configuration to restrict system utilities and strengthen endpoint security controls.</p>
<p><strong>Skills:</strong> Registry Hardening · Threat Surface Reduction · OS Security</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-endpoint-security-windows-registry/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Enterprise Security Software Types – v1.0.1</h5>
<p>Comprehensive research into enterprise defensive technologies including EDR, IAM, IDS/IPS, and secure operating environments.</p>
<p><strong>Skills:</strong> EDR · IAM · Endpoint Protection · Defense-in-Depth</p>
<p align="center" style="margin-top:20px;">
<span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Research on the Top Penetration Testing Tools – v1.0.0</h5>
<p>Technical evaluation of industry-standard penetration testing tools used for vulnerability discovery and exploitation testing.</p>
<p><strong>Skills:</strong> Vulnerability Assessment · Penetration Testing Tools · Security Auditing</p>
<p align="center" style="margin-top:20px;">
<span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span>
</p>
</div>

</div>

### 🧱 Infrastructure Protection & Recovery

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – AD Disaster Recovery & Identity Restoration – v1.0.2</h5>
<p>Simulates a full Domain Controller failure and demonstrates how to restore an Active Directory environment using Bare Metal Recovery (BMR) on Windows Server 2016.</p>
<p><strong>Skills:</strong> Active Directory Recovery · BMR · DSRM · System State Restore · Disaster Recovery Validation</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-ad-disaster-recovery-identity-restoration-v1.0.2/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Report</a>
</p>
</div>

</div>

### 🚨 Incident Response & Monitoring

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Forced Browsing Data Breach – v1.1.0</h5>
<p>Post-incident investigation of a web application data breach caused by broken access control, including log analysis, root cause identification, and remediation of unauthorized data access.</p>
<p><strong>Skills:</strong> Incident Response · Log Analysis · Web Security · Access Control · Root Cause Analysis</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/forced-browsing-data-breach/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Linux Automation: ClamAV Security & System Maintenance – v1.0.0</h5>
<p>Demonstrates automated malware detection and system maintenance using cron scheduling and ClamAV, including log monitoring, quarantine workflows, and validation of security operations in a Linux environment.</p>
<p><strong>Skills:</strong> Security Operations · Linux Administration · Automation</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-linux-automation-clamav-system-maintenance/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Report</a>
</p>
</div>

</div>

### 🔍 Threat Hunting & Malware Analysis

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Portable Executable (PE) File Analysis Using PEStudio – v1.0.0</h5>
<p>Technical analysis of Windows Portable Executable (PE) files to identify structural anomalies, extract compilation metadata, and analyze internal strings to support static malware detection and threat hunting workflows.</p>
<p><strong>Skills:</strong> Static Analysis · PE File Structure · Malware Detection · Threat Hunting · PEStudio</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span></p>
</div>

</div>

 
## Lab Demonstrations

### 🛡️ Detection & Monitoring Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Network Traffic Monitoring with pfSense and Snort – v1.0.0</h5>
<p>Monitoring and analyzing network traffic using IDS/IPS tools to detect suspicious activity and potential intrusions.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span></p>
</div>

</div>

### 🔍 Vulnerability Assessment Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Vulnerability Scanning Using OpenVAS – v1.0.0</h5>
<p>Performing vulnerability assessments to identify and prioritize security weaknesses across networked systems.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Deploying OpenVAS with Docker – v1.0.0</h5>
<p>Containerized deployment of OpenVAS for scalable and repeatable vulnerability scanning environments.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – SSL/TLS Configuration Assessment with sslscan – v1.0.0</h5>
<p>Evaluating cryptographic configurations and identifying weak protocols and cipher suites in secure communications.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span></p>
</div>

</div>

### 🧬 Threat Detection Engineering (YARA) Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – YARA Environment Setup – v1.0.0</h5>
<p>Setting up a malware detection environment using YARA for rule-based file analysis.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Creating YARA Rules – v1.0.0</h5>
<p>Developing rule-based signatures to identify malware patterns and suspicious file characteristics.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Detecting Small PE Files Using YARA – v1.0.0</h5>
<p>Identifying suspicious executables through size-based and structural pattern matching.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Self-Matching YARA Rule – v1.0.0</h5>
<p>Validating YARA rule behavior by testing detection logic against controlled datasets.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Request Access</span></p>
</div>

</div>

<hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

## Continue Exploring

<p>
The security operations capabilities demonstrated in this section focus on protecting systems through monitoring, threat detection, security controls, and incident response. However, effective security requires more than technical defenses alone. Organizations also need structured processes to identify risk, evaluate security requirements, and align technology decisions with business objectives.
</p>

<p>
The projects presented here represent publicly available examples of security operations work. Additional implementation records, technical documentation, and supporting evidence are maintained privately in accordance with training provider publishing requirements.
</p>

<p>
Continue to the next section to explore how governance, risk management, compliance practices, and security frameworks help organizations identify risks, establish controls, and make informed security decisions.
</p>
