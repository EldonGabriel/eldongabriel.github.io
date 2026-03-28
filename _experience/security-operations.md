---
title: "Security Operations"
layout: collection-item
slug: security-operations
collection: experience
collection_item: true
order: 5
permalink: /security-operations/
image:
  path: /assets/images/headers/so.png
  thumbnail: /assets/images/headers/so.png
  caption: "Security Operations, Hardening, and Monitoring Labs"
---

### Security Operations Lab Overview

Security operations focuses on protecting systems, monitoring infrastructure activity, and responding to operational security risks. The labs in this section demonstrate hands-on experience implementing endpoint hardening controls, deploying secure remote access solutions, performing disaster recovery procedures, and analyzing system behavior through operational monitoring tools in controlled lab environments.

These labs demonstrate operational security practices including system hardening, VPN deployment, backup and recovery planning, and monitoring system activity through logs and operational security tools.

| Category | Labs |
|--------|------|
| Perimeter Defense & Secure Connectivity | 3 |
| Endpoint Hardening & Access Control | 6 |  
| Infrastructure Protection & Recovery | 1 | 
| Threat Hunting & Malware Analysis | 1 |
| Lab Demonstration |  8 |
| **Total Security Operations Labs Documented** | **19** |

---

# Security Operations Portfolio

Hands-on configuration of system security controls designed to protect infrastructure, enforce access restrictions, and support disaster recovery capabilities.

### 🛡️ Perimeter Defense & Secure Connectivity

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>Secure Connectivity: Architecting Enterprise IPsec VPNs</h5>
<p>Demonstrates building and validating a site-to-site IPsec VPN between enterprise locations to secure data in transit over untrusted networks.</p>
<p><strong>Skills:</strong> IPsec VPN · IKE · ACLs · NAT Exemption · Network Security · CLI Troubleshooting</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/architecting-enterprise-ipsec-vpns/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Field Notes</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Perimeter Defense: Firewall Fundamentals – v1.0.0</h5>
<p>Overview of firewall technologies and their role in enforcing network perimeter security.</p>
<p><strong>Skills:</strong> Network Security · Perimeter Defense · Firewall Policy</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – OpenVPN Remote Access Deployment and Validation – v1.0.0</h5>
<p>Deployment and validation of an OpenVPN remote access solution to provide secure connectivity for remote systems.</p>
<p><strong>Skills:</strong> VPN Deployment · Encryption · Secure Remote Access</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

</div>

### 🔐 Endpoint Hardening & Access Control

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>Using the Windows Registry to Restrict Untrusted User Accounts</h5>
<p>Demonstrates using Windows Registry configuration to restrict system utilities and strengthen endpoint security controls.</p>
<p><strong>Skills:</strong> Registry Hardening · Threat Surface Reduction · OS Security</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/using-the-windows-registry-to-restrict-untrusted-user-accounts/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Research on the Top Penetration Testing Tools – v1.0.0</h5>
<p>Technical evaluation of industry-standard security tools including Nmap, Burp Suite, and Metasploit, assessing their utility in vulnerability discovery and exploitation testing.</p>
<p><strong>Skills:</strong> Vulnerability Assessment · Penetration Testing Tools · Security Auditing</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Enterprise Security Software Types – v1.0.1</h5>
<p>Comprehensive research into enterprise-grade defensive solutions including EDR, IAM, IDS/IPS, and the implementation of Secure Standard Operating Environments (SSOE).</p>
<p><strong>Skills:</strong> EDR · IAM · Endpoint Protection · Defense-in-Depth</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>Deploying Local Group Policy to Harden SMB Sessions</h5>
<p>Applied SMB security policies to reduce exposure to credential harvesting and lateral movement.</p>
<p><strong>Skills:</strong> SMB Hardening · Credential Protection · Lateral Movement Mitigation</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/deploying-local-group-policy-to-harden-smb-sessions/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>Monitoring Windows Processes with Procmon: A Practical Guide</h5>
<p>Demonstrates using Microsoft Process Monitor to observe Windows system activity, analyze process behavior, and investigate interactions with the file system and registry.</p>
<p><strong>Skills:</strong> Security Monitoring · Process Analysis · Sysinternals Diagnostics</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/procmon-incident-response/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>Applying Local GPO for Session Lock Enforcement</h5>
<p>Configured session lock policies using Local Group Policy to automatically secure idle systems and reduce unauthorized access risk.</p>
<p><strong>Skills:</strong> GPO Configuration · Endpoint Hardening · Access Control Enforcement</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/deploying-session-lock-gpo/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Field Notes</a>
</p>
</div>

</div>

### 🧱 Infrastructure Protection & Recovery

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>Active Directory Disaster Recovery & Identity Restoration</h5>
<p>Simulates a full Domain Controller failure and demonstrates how to restore an Active Directory environment using Bare Metal Recovery (BMR) on Windows Server 2016.</p>
<p><strong>Skills:</strong> Active Directory Recovery · BMR · DSRM · System State Restore · Disaster Recovery Validation</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/active-directory-bare-metal-recovery/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Field Notes</a>
</p>
</div>

</div>

### 🔍 Threat Hunting & Malware Analysis

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Portable Executable (PE) File Analysis Using PEStudio – v1.0.0</h5>
<p>Technical analysis of Windows Portable Executable (PE) files to identify structural anomalies, extract compilation metadata, and analyze internal strings to support static malware detection and threat hunting workflows.</p>
<p><strong>Skills:</strong> Static Analysis · PE File Structure · Malware Detection · Threat Hunting · PEStudio</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

</div>

---

## Lab Demonstrations

### 🛡️ Detection & Monitoring Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Network Traffic Monitoring with pfSense and Snort – v1.0.0</h5>
<p>Monitoring and analyzing network traffic using IDS/IPS tools to detect suspicious activity and potential intrusions.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

</div>

### 🔍 Vulnerability Assessment Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Vulnerability Scanning Using OpenVAS – v1.0.0</h5>
<p>Performing vulnerability assessments to identify and prioritize security weaknesses across networked systems.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Deploying OpenVAS with Docker – v1.0.0</h5>
<p>Containerized deployment of OpenVAS for scalable and repeatable vulnerability scanning environments.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – SSL/TLS Configuration Assessment with sslscan – v1.0.0</h5>
<p>Evaluating cryptographic configurations and identifying weak protocols and cipher suites in secure communications.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

</div>

### 🧬 Threat Detection Engineering (YARA) Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – YARA Environment Setup – v1.0.0</h5>
<p>Setting up a malware detection environment using YARA for rule-based file analysis.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Creating YARA Rules – v1.0.0</h5>
<p>Developing rule-based signatures to identify malware patterns and suspicious file characteristics.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Detecting Small PE Files Using YARA – v1.0.0</h5>
<p>Identifying suspicious executables through size-based and structural pattern matching.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Self-Matching YARA Rule – v1.0.0</h5>
<p>Validating YARA rule behavior by testing detection logic against controlled datasets.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

</div>

---

# Portfolio Documentation

This section summarizes hands-on security operations labs including system hardening, VPN deployment, disaster recovery procedures, and operational monitoring activities performed in controlled lab environments. Additional configuration notes, lab documentation, and technical records are maintained within a private research archive.  
