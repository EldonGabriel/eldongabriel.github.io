---
title: "Infrastructure & Systems"
layout: collection-item
slug: infrastructure-systems
collection: experience
collection_item: true
order: 1
permalink: /infrastructure-systems/
image:
  path: /assets/images/headers/is.png
  thumbnail: /assets/images/headers/is.png
  caption: "Infrastructure & Systems Administration Labs"
---

## Infrastructure Laboratory Overview

Modern IT infrastructure depends on stable operating systems, virtualization platforms, and reliable administrative processes. The labs and reports in this section demonstrate hands-on experience managing Windows and Linux systems, building virtual lab environments, and maintaining operational stability across infrastructure components.

These labs represent hands-on work performed in controlled environments designed to simulate real-world infrastructure administration tasks. Activities include operating system management, virtualization deployment, cloud infrastructure provisioning, system hardening, and operational troubleshooting.

| Category | Labs |
|--------|------|
| Windows Systems Administration | 12 |
| Linux Systems Administration | 6 |
| Virtualization & Infrastructure | 7 |
| Lab Demonstration | 47 |
| **Total Labs Documented** | **72** |

---

# Windows Systems Administration

Hands-on system administration tasks performed in Windows environments, focusing on system management, disk operations, service control, and operational troubleshooting.

## Windows Systems Administration Portfolio

### 🛡️ Endpoint Security Engineering & GPO Hardening

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Deploy Local GPO for Windows Security Policies – v1.0.0</h5>
<p>Configured Local Group Policy settings to enforce baseline Windows security protections.</p>
<p><strong>Skills:</strong> GPO Engineering · Endpoint Hardening</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/deploying-local-group-policy-to-strengthen-windows-security/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – GPO Hardening for Windows Application Control – v1.0.0</h5>
<p>Implemented execution restrictions and application whitelisting logic via Group Policy Objects.</p>
<p><strong>Skills:</strong> Application Control · Threat Surface Reduction</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/wcp-administration/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Harden UAC via Local Group Policy – v1.0.0</h5>
<p>Strengthened User Account Control configuration to prevent unauthorized privilege escalation.</p>
<p><strong>Skills:</strong> UAC Hardening · Privilege Security</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/protecting-win10-hardened-uac-settings/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – System Hardening via Local GPO: Windows Defender – v1.0.0</h5>
<p>Deployed centralized configurations for Windows Defender Antivirus to ensure real-time protection.</p>
<p><strong>Skills:</strong> Endpoint Protection · Windows Defender</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/hardening-windows-defender-local-gpo/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – Endpoint Security with the Windows Registry – v1.0.0</h5>
<p>Configured Windows Registry security settings to restrict untrusted user activity and enforce system-level access controls.</p>
<p><strong>Skills:</strong> ERegistry Hardening · Endpoint Security · Access Control</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/using-the-windows-registry-to-restrict-untrusted-user-accounts/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Applying a Local GPO for Session Lock Enforcement – v1.0.0</h5>
<p>Configured automatic workstation locking to prevent unauthorized physical access to unattended systems.</p>
<p><strong>Skills:</strong> Physical Security · Policy Enforcement</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/deploying-session-lock-gpo/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – System Hardening via Local GPO: Restricting Anonymous Connections – v1.0.0</h5>
<p>Hardened the OS by restricting null sessions and anonymous enumeration of SAM accounts and shares.</p>
<p><strong>Skills:</strong> Information Leakage · System Hardening</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/hardening-win10-restricting-anonymous-connections/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

</div>

### 🛠️ Infrastructure Operations & Diagnostics

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Enforcing Operating System Patching Policy via Local GPO – v1.0.0</h5>
<p>Configured Windows Update policies through GPO to ensure timely security patching.</p>
<p><strong>Skills:</strong> Vulnerability Management · Patch Compliance</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/enforcing-windows-patching-policies/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

</div>

### 📡 Network Protocol Security

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – WinRM Secure Configuration and Validation – v1.0.0</h5>
<p>Configured and validated secure Windows Remote Management settings for administrative traffic.</p>
<p><strong>Skills:</strong> WinRM · Secure Remote Administration</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/securing-winrm-configuration-with-lgp/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – SMB Protocol: Function and Security Risks – v1.0.0</h5>
<p>Analyzed the SMB protocol architecture and documented operational and security risks.</p>
<p><strong>Skills:</strong> Network Protocols · Threat Analysis</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/blocking-smb-access-strengthening-network-security-with-windows-firewall/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

</div>

---

### 🐧 Linux Systems Administration

Administration of Linux-based systems including user management, file permissions, system processes, and log analysis in server environments.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – Cockpit Secure System Administration – v1.0.0</h5>
<p>Configured Cockpit for secure browser-based Linux system management and service monitoring.</p>
<p><strong>Skills:</strong> Linux Administration · Server Management</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – Webmin Secure Administration – v1.0.0</h5>
<p>Deployed and secured Webmin to manage Linux services, users, and configuration through a web interface.</p>
<p><strong>Skills:</strong> Linux Service Management · System Configuration</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Linux File Permissions Management – v1.0.0</h5>
<p>Managed file and directory permissions using chmod, chown, and chgrp to enforce proper access control.</p>
<p><strong>Skills:</strong> Linux Permissions · Access Control</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Linux System Administration Commands – v1.0.0</h5>
<p>Documentation of essential Linux commands used for system monitoring, troubleshooting, and resource management.</p>
<p><strong>Skills:</strong> Linux CLI Administration · Process Monitoring · System Diagnostics</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

</div>

### 📑 Linux Administration Guides

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – SAR Performance Monitoring on Ubuntu – v1.0.0</h5>
<p>Implemented SAR to monitor CPU, memory, disk I/O, and network utilization on Ubuntu servers.</p>
<p><strong>Skills:</strong> Linux Monitoring · Performance Diagnostics · System Analysis</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

</div>

---

### 🌐 Virtualization & Infrastructure

Focuses on the virtualization frameworks that support secure enterprise environments.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">


<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – VirtualBox Network Modes – v1.0.0</h5>
<p>Analysis of VirtualBox networking configurations including NAT, Bridged, Host-Only, and Internal networking modes.</p>
<p><strong>Skills:</strong> Virtual Networking · Lab Infrastructure · Network Configuration</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – System Administration Virtualization in Cybersecurity – v1.0.1</h5>
<p>Explains the role of virtualization platforms in building isolated environments for system administration and cybersecurity testing.</p>
<p><strong>Skills:</strong> Virtualization · Lab Architecture · Security Testing Environments</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>IR – AWS MGN Agent Removal & Environment Cleanup – v1.0.0</h5>
<p>Documented the removal of AWS MGN migration agents and performed post-migration environment cleanup and validation.</p>
<p><strong>Skills:</strong> AWS Migration · Cloud Cleanup · Incident Remediation</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

</div>

### 📑  Virtualiztion & Infrastructure Guides

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – VMware-to-AWS Migration Runbook – v1.1.0</h5>
<p>Step-by-step runbook documenting migration procedures from VMware environments to AWS EC2, including post-migration agent cleanup and validation.</p>
<p><strong>Skills:</strong> Cloud Migration · AWS EC2 · Infrastructure Runbooks</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/aws-mgn-agent-removal-vmware-to-ec2/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – Building a vSphere 8 Nested Lab on AMD Ryzen 6000 – v1.0.0</h5>
<p>Built a nested VMware vSphere 8 lab environment on AMD Ryzen hardware by bypassing firmware virtualization restrictions.</p>
<p><strong>Skills:</strong> Virtualization · Lab Architecture · Hypervisor Deployment</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/bypassing-firmware-locks-nested-vsphere-8/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – UTM Kali Linux Shared Folder Configuration – v1.0.0</h5>
<p>Configured shared folder integration between host and Kali Linux virtual machine within UTM virtualization environment.</p>
<p><strong>Skills:</strong> Virtualization · Linux VM Management · File Integration</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/utm-kali-linux-shared-folder-guide/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

</div>

---

## Lab Demonstrations

### 🏗️ Virtualization & Infrastructure Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – VMware ESXi and vSphere VM Deployment and Network Connectivity Test – v1.0.0</h5>
<p>Hands-on setup of enterprise hypervisor environments using ESXi and vSphere management.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Virtual Machine Snapshot Creation for System Rollback – v1.0.0</h5>
<p>Demonstrating the use of snapshots to create point-in-time recovery marks before system changes.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – VMware Fusion VM Deployment and Inter-VM Network Connectivity – v1.0.0</h5>
<p>Standardized workflow for provisioning new virtual hardware within a VMware environment.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Windows Subsystem for Linux Installation and Configuration – v1.0.0</h5>
<p>Configuring WSL to enable a native Linux environment directly within Windows.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Two-VM Virtualized Cybersecurity Lab Environment – v1.0.0</h5>
<p>Architecting a secure, isolated lab with a victim and attacker machine for security testing.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Setting Up a Secure Software Development Environment – v1.0.0</h5>
<p>Configuration of a secure and efficient development environment with essential tools, runtimes, and workflows to support secure coding and system development practices.</p>
<p align="center" style="margin-top:20px;">
<span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

</div>

### ☁️ Cloud Infrastructure Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – AWS EC2 Virtual Machine Deployment and Secure SSH Access – v1.0.0</h5>
<p>Provisioning EC2 instances within AWS, including Security Group and remote access validation.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – GCP Compute Engine Virtual Machine Deployment and SSH Access – v1.0.0</h5>
<p>Deploying Compute Engine instances on Google Cloud Platform with VPC integration.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Windows 10 VM on Google Cloud Platform (GCP) - v1.0.0</h5>
<p>Advanced deployment of a Windows 10 instance on GCP for remote desktop and management tasks.</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/Mastering-GCP-windows-10/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Blog</a></p>
</div>

</div>

### 🐧 Linux Administration & Security Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux Command-Line Exploration and Documentation Lookup – v1.0.0</h5>
<p>Hands-on exploration of Linux command documentation using built-in tools such as man and cat to understand command syntax and options.</p>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/FR4KFGZfAoE" frameborder="0" allowfullscreen></iframe>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux User and Group Management – v1.0.0</h5>
<p>Demonstration of Linux account lifecycle tasks including user creation, group assignment, ownership changes, and account removal.</p>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/uOdoAZIpx1M" frameborder="0" allowfullscreen></iframe>
</div> 

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – File Discovery and Analysis in Linux – v1.0.0</h5>
<p>Using Linux command-line tools to locate, navigate, and analyze files for system investigation and log analysis tasks.</p>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/HBcQVczahMM" frameborder="0" allowfullscreen></iframe>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux File and Directory Management – v1.0.0</h5>
<p>Hands-on file system management within a Linux environment, including directory organization and command-line file operations.</p>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/lhkrFbimQKg" frameborder="0" allowfullscreen></iframe>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux File Permission and Directory Access Control – v1.0.0</h5>
<p>Practical demonstration of managing Linux file permissions and securing directories through user and group access control.</p>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/5qKJk-fID3g" frameborder="0" allowfullscreen></iframe>
</div> 

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux Log and Data Filtering with grep – v1.0.0</h5>
<p>Demonstration of log analysis techniques using grep to filter server logs and extract relevant user and system data.</p>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/lUVLujgD4b4" frameborder="0" allowfullscreen></iframe>
</div> 

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux Firewall Configuration with Shorewall – v1.0.0</h5>
<p>Configuring Shorewall to manage Netfilter and secure network traffic on Linux servers.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux Performance Monitoring with SAR (sysstat) – v1.0.0</h5>
<p>Real-time and historical performance data collection using the System Activity Reporter.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux System Administration with Cockpit – v1.0.0</h5>
<p>Using the Cockpit web console for graphical server management and system health monitoring.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Secure Linux Administration with Webmin – v1.0.0</h5>
<p>Centralized administration of users, services, and configs through the Webmin portal.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

</div>

### 🪟 Windows System Administration Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Setting Up a Computer for Network Integration – v1.0.0</h5>
<p>Preparation and configuration of a workstation for integration into a business network, including system setup, connectivity configuration, and validation.</p>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/m4MngVs_bmM" frameborder="0" allowfullscreen></iframe>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Joining a Windows Workstation to a Domain – v1.0.0</h5>
<p>Demonstration of joining a Windows workstation to a domain, enabling centralized authentication, policy enforcement, and enterprise system management.</p>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/JE3jutqyI4Q" frameborder="0" allowfullscreen></iframe>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Analyze Windows Processes with Procmon – v1.0.0</h5>
<p>Using Process Monitor to audit registry, file system, and network activity in real-time.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Secure Credentials with a Password Manager – v1.0.0</h5>
<p>Best practices for credential hygiene using secure vaulting solutions.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Use Registry to Restore File Ownership – v1.0.0</h5>
<p>Direct Registry manipulation to recover ownership and access permissions on critical files.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Block SMB Access with Windows Firewall – v1.0.0</h5>
<p>Mitigating lateral movement by creating firewall rules to block SMB traffic on endpoints.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

</div>

### 🛡️ Windows Administration & Hardening (GPO) Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – GPO to Enforce Session Locks – v1.0.0</h5>
<p>Configuring idle-time lockouts to protect physical security of endpoints.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Securely Configure WinRM with GPO – v1.0.0</h5>
<p>Securing remote management traffic using encrypted listeners and policy enforcement.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Windows Defender Hardening via GPO – v1.0.0</h5>
<p>Configuring advanced Defender settings, including real-time scanning and cloud protection.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Deployed Exploit Guard via GPO – v1.0.0</h5>
<p>Enabling Attack Surface Reduction (ASR) rules and memory protection through Exploit Guard.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted – Available for Professional Review</span></p>
</div>

</div>

### ⚙️ Managed Operations & Automation Labs

Utilizing advanced Windows management tools to automate recurring maintenance tasks, monitor system health, and secure data-at-rest.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:30px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1); text-align:center;">
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 8px; margin-bottom:15px;">
<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/wlgnNwbKe3w" title="BitLocker" frameborder="0" allowfullscreen></iframe>
</div>
<h4>🔐 Data Security</h4>
<p>Demonstrating the planning and deployment of BitLocker Drive Encryption to protect data-at-rest.</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1); text-align:center;">
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 8px; margin-bottom:15px;">
<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/z8nXF2OleGo" title="Task Scheduler" frameborder="0" allowfullscreen></iframe>
</div>
<h4>🤖 Automation</h4>
<p>Automating recurring system maintenance and cleanup tasks via the Windows Task Scheduler.</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1); text-align:center;">
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 8px; margin-bottom:15px;">
<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/rw7QL5BgQgI" title="Event Viewer" frameborder="0" allowfullscreen></iframe>
</div>
<h4>🛠️ Diagnostics</h4>
<p>Advanced monitoring and troubleshooting techniques using the Windows Event Viewer.</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1); text-align:center;">
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 8px; margin-bottom:15px;">
<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" src="https://www.youtube.com/embed/WZtkpKxr9xE" title="Firewall" frameborder="0" allowfullscreen></iframe>
</div>
<h4>🛡️ Network Hardening</h4>
<p>Configuring host-based firewall rules to restrict unauthorized traffic and secure network entry points.</p>
</div>

</div>

---

# Portfolio Documentation

This section summarizes hands-on infrastructure, virtualization, cloud, and operating system administration labs performed as part of my ongoing cybersecurity and systems administration training.

While this page highlights representative reports and demonstrations, it is supported by a larger collection of technical documentation, lab notes, and system configuration records maintained within my research archive.

To keep the site streamlined and focused on key projects, not all documentation artifacts are displayed directly.

Complete reports, lab documentation, and supporting technical materials are Restricted – Available for Professional Review for professional or technical review.
