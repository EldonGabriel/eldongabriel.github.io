---
title: "Infrastructure & Systems"
layout: collection-item
slug: infrastructure-systems
collection: experience
collection_item: true
order: 3
permalink: /infrastructure-systems/
image:
  path: /assets/images/headers/is.png
  thumbnail: /assets/images/headers/is.png
  caption: "Infrastructure & Systems Administration Labs"
---

## Infrastructure Laboratory Overview

This section demonstrates how I build, harden, and validate enterprise infrastructure across Windows, Linux, cloud, and virtualized environments.

My work focuses on applying security controls at the system level, ensuring that operating systems, network configurations, and infrastructure components are not only functional, but secured and aligned with industry frameworks.

These labs reflect hands-on implementation across system administration, virtualization, cloud provisioning, and infrastructure security. Each environment is designed to simulate real-world conditions, where configurations are enforced, tested, and validated to ensure stability, access control, and operational resilience.

### Lab Distribution Summary

| Category | Labs |
|--------|------|
| Technical Foundations | 2 |  
| Windows Systems Administration | 7 | 
| System Administration & Maintenance | 3 |
| Troubleshooting & System Diagnostics | 5 |
| Linux Systems Administration | 2 |
| Virtualization & Infrastructure | 5 |
| Lab Demonstrations | 33 |
| **Total Labs Documented** | **57** |

---

### 🧠 Technical Foundations

These reports focus on core system knowledge, including how hardware, memory, and processing work together to support computing operations.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Introduction to Computer Hardware and Processing – v1.0.0</h5>
<p>Overview of core computer components, including CPU, RAM, storage, and how data is processed at the hardware level.</p>
<p><strong>Skills:</strong> Hardware Fundamentals · Data Processing · System Architecture</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-introduction-computer-hardware-processing/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">
View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Binary Systems, Data Representation and Logic Gates – v1.0.0</h5>
<p>Analysis of how computers process binary data using encoding systems and logic gates to produce meaningful outputs.</p>
<p><strong>Skills:</strong> Binary Conversion · Data Encoding · Logic Gates · System Analysis</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-binary-systems-data-representation-logic-gates/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">
View Report</a>
</p>
</div>

</div>

---

## Windows Systems Administration

Hands-on system administration tasks performed in Windows environments, focusing on system management, security controls, and troubleshooting.

---

### 🛡️ Endpoint Security & GPO Hardening
<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>SOP – Hardening Windows Defender Using Local GPO – v1.0.1</h5>
<p>Deployed centralized configurations for Windows Defender Antivirus to ensure real-time protection.</p>
<p><strong>Skills:</strong> Endpoint Protection · Windows Defender</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/sop-hardening-windows-defender-using-local-gpo-v1.0.1/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>SOP – Anonymous Access Restriction & Recon Hardening – v1.0.2</h5>
<p>Hardened the OS by restricting null sessions and anonymous enumeration of SAM accounts and shares.</p>
<p><strong>Skills:</strong> Information Leakage · System Hardening</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/sop-anonymous-access-restriction-recon-hardening-v1.0.2/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – OS Patching Enforcement via Local GPO – v1.0.0</h5>
<p>Configured automated patch management policies using Local Group Policy to ensure systems remain up to date and secure.</p>
<p><strong>Skills:</strong> Patch Management · Policy Enforcement · System Maintenance</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-os-patching-enforcement-local-gpo-v.1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Hardening Microsoft Edge via Local GPO – v1.0.0</h5>
<p>Applied Group Policy configurations to secure Microsoft Edge by restricting extensions, downloads, and unsafe browser behaviors.</p>
<p><strong>Skills:</strong> Browser Hardening · Web Security · GPO Configuration</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-harden-microsoft-edge-local-gpo-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Deploy Controlled Folder Access via Local GPO – v1.0.0</h5>
<p>Implemented Controlled Folder Access to prevent unauthorized applications from modifying protected directories.</p>
<p><strong>Skills:</strong> Ransomware Protection · Data Integrity · Endpoint Hardening</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-deploy-controlled-folder-access-via-local-gpo-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Endpoint Security with Windows Registry – v1.0.0</h5>
<p>Configured Windows Registry security settings to restrict untrusted user activity and enforce system-level access controls.</p>
<p><strong>Skills:</strong> Registry Hardening · Endpoint Security · Access Control</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-endpoint-security-windows-registry/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – GPO Hardening for Windows Application Control – v1.0.0</h5>
<p>Configured Group Policy controls to restrict unauthorized software execution and strengthen application control mechanisms.</p>
<p><strong>Skills:</strong> Application Control · Threat Surface Reduction · GPO Enforcement</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-gpo-hardening-for-windows-application-control-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

</div>

### ⚙️ System Administration & Maintenance

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Windows Disk Management with CHKDSK and FSUTIL – v1.0.0</h5>
<p>Using built-in Windows tools to check disk health, repair filesystem errors, and validate storage integrity.</p>
<p><strong>Skills:</strong> Disk Management · Filesystem Repair · Storage Integrity</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-windows-disk-management-chkdsk-fsutil-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">
View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);"> 
<h5>REPORT – Windows Control Panel Administration – v1.0.0</h5> <p>Implemented execution restrictions and application whitelisting logic via Group Policy Objects.</p> <p><strong>Skills:</strong> Application Control · Threat Surface Reduction</p> 
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-windows-control-panel-administration/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p> 
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – Windows System Administration Labs (11 Modules) – v1.0.0</h5>
<p>Collection of structured Windows system administration labs covering core operational tasks, system configuration, and environment management across multiple scenarios.</p>
<p><strong>Skills:</strong> Windows Administration · System Configuration · Troubleshooting · Lab Environment Management</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/guide-windows-system-administration-labs-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

</div>

### 🔍 Troubleshooting & System Diagnostics

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – USB Storage Failure Analysis and Disk Validation – v1.0.0</h5>
<p>Investigation of USB storage instability to determine if failures were caused by filesystem corruption or physical hardware defects.</p>
<p><strong>Skills:</strong> Hardware Diagnostics · Disk Validation · CHKDSK · Root Cause Analysis</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-usb-storage-failure-analysis/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">
View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – USB Filesystem Corruption Due to Improper Removal – v1.0.0</h5>
<p>Analysis of a corrupted USB device caused by improper removal during active disk operations, resulting in filesystem failure.</p>
<p><strong>Skills:</strong> Filesystem Troubleshooting · Disk Management · Data Integrity · Root Cause Analysis</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-usb-filesystem-corruption/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">
View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Restore USB Access on a Windows 10 VM – v1.1.0</h5>
<p>Resolved USB passthrough issues in a virtualized environment by configuring VirtualBox USB filters and validating filesystem integrity.</p>
<p><strong>Skills:</strong> Virtualization · USB Passthrough · Disk Management · CHKDSK · Root Cause Analysis</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-restore-usb-access-windows-10-vm/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">
View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Workstation Power Failure Investigation – v1.0.0</h5>
<p>Diagnosed and resolved hardware instability caused by insufficient power supply capacity following system upgrades.</p>
<p><strong>Skills:</strong> Hardware Diagnostics · Power Load Calculation · Root Cause Analysis (RCA) · Data Integrity</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-workstation-power-failure-investigation/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Troubleshooting Remote Access and Network Isolation – v1.0.0</h5>
<p>Resolved Remote Desktop access failures by fixing Group Policy conflicts and implementing a dual-homed network design for secure management.</p>
<p><strong>Skills:</strong> RDP Troubleshooting · Group Policy · Network Isolation · Access Control · Root Cause Analysis</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/troubleshooting-remote-access-network-isolation/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">
View Report</a>
</p>
</div>

</div>

---

### 🐧 Linux Systems Administration

Administration and hardening of Linux-based systems, including user management, access control enforcement, system processes, and log analysis within server environments.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – SAR Performance Monitoring on Ubuntu – v1.0.1</h5>
<p>Utilized system activity reporting tools to monitor CPU, memory, and I/O performance on Ubuntu systems for operational diagnostics and system health analysis.</p>
<p><strong>Skills:</strong> System Monitoring · Performance Analysis · Linux Diagnostics</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-sar-performance-monitoring-ubuntu-v1.0.1/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Linux File Permissions Management – v1.0.0</h5>
<p>Managed file and directory permissions using chmod, chown, and chgrp to enforce proper access control.</p>
<p><strong>Skills:</strong> Linux Permissions · Access Control</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/linux-file-permissions-management/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

</div>

---

### 🌐 Virtualization & Infrastructure

Design and deployment of virtualized environments used to support secure system administration, testing, and infrastructure validation across isolated lab environments.

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Enterprise Hybrid-Cloud Migration – v1.2.0</h5>
<p>A practical troubleshooting case study on migrating VMware virtual machines to AWS EC2 and resolving kernel driver removal issues from the AWS Application Migration Service.</p>
<p><strong>Skills:</strong> Cloud Migration · AWS EC2 · Infrastructure Runbooks</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-enterprise-hybrid-cloud-migration-v1.2.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – vSphere 8 Nested Lab on AMD Ryzen 5 6600H – v1.0.0</h5>
<p>Demonstrates the setup of a nested virtualization environment using VMware vSphere 8 on AMD Ryzen 6000 hardware, including configuration of nested ESXi hosts and lab networking.</p>
<p><strong>Skills:</strong> Nested Virtualization · VMware vSphere · Lab Deployment · Infrastructure Configuration</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/guide-vsphere-8-nested-lab-amd-ryzen-5-6600h/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – UTM Kali Linux Shared Folder Configuration – v1.0.0</h5>
<p>Configured shared folder integration between host and Kali Linux virtual machine within UTM virtualization environment.</p>
<p><strong>Skills:</strong> Virtualization · Linux VM Management · File Integration</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/guide-utm-kali-linux-shared-folder-configuration-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – GCP Windows 10 VM Deployment – v1.0.0</h5>
<p>Demonstrates deploying and configuring a Windows 10 virtual machine in Google Cloud Platform, including network setup, access configuration, and system initialization.</p>
<p><strong>Skills:</strong> GCP · Cloud Infrastructure · VM Deployment · Remote Access Configuration</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/guide-gcp-windows-10-vm-deployment-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>GUIDE – Cybersecurity Virtualization Labs (VMware, WSL, GCP, AWS) – v1.0.0</h5>
<p>Provides an overview of building and managing cybersecurity-focused virtualization labs across multiple platforms including VMware, WSL, GCP, and AWS for testing and learning environments.</p>
<p><strong>Skills:</strong> Virtualization · Multi-Cloud Environments · Lab Architecture · Infrastructure Design</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/guide-cybersecurity-virtualizationlabs-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a> 
</p>
</div> 

</div> 

---

## Lab Demonstrations

### 🏗️ Virtualization & Infrastructure Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – VMware ESXi and vSphere VM Deployment and Network Connectivity Test – v1.0.0</h5>
<p>Hands-on setup of enterprise hypervisor environments using ESXi and vSphere management.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Virtual Machine Snapshot Creation for System Rollback – v1.0.0</h5>
<p>Demonstrating the use of snapshots to create point-in-time recovery marks before system changes.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – VMware Fusion VM Deployment and Inter-VM Network Connectivity – v1.0.0</h5>
<p>Standardized workflow for provisioning new virtual hardware within a VMware environment.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Windows Subsystem for Linux Installation and Configuration – v1.0.0</h5>
<p>Configuring WSL to enable a native Linux environment directly within Windows.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Two-VM Virtualized Cybersecurity Lab Environment – v1.0.0</h5>
<p>Architecting a secure, isolated lab with a victim and attacker machine for security testing.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Setting Up a Secure Software Development Environment – v1.0.0</h5>
<p>Configuration of a secure and efficient development environment with essential tools, runtimes, and workflows to support secure coding and system development practices.</p>
<p align="center" style="margin-top:20px;">
<span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

</div>

### ☁️ Cloud Infrastructure Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – AWS EC2 Virtual Machine Deployment and Secure SSH Access – v1.0.0</h5>
<p>Provisioning EC2 instances within AWS, including Security Group and remote access validation.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – GCP Compute Engine Virtual Machine Deployment and SSH Access – v1.0.0</h5>
<p>Deploying Compute Engine instances on Google Cloud Platform with VPC integration.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>Mastering GCP: Windows 10 VM Deployment</h5>
<p>Advanced deployment of a Windows 10 instance on GCP for remote desktop and management tasks.</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/Mastering-GCP-windows-10/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
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
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux Performance Monitoring with SAR (sysstat) – v1.0.0</h5>
<p>Real-time and historical performance data collection using the System Activity Reporter.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Linux System Administration with Cockpit – v1.0.0</h5>
<p>Using the Cockpit web console for graphical server management and system health monitoring.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Secure Linux Administration with Webmin – v1.0.0</h5>
<p>Centralized administration of users, services, and configs through the Webmin portal.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
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
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Secure Credentials with a Password Manager – v1.0.0</h5>
<p>Best practices for credential hygiene using secure vaulting solutions.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Use Registry to Restore File Ownership – v1.0.0</h5>
<p>Direct Registry manipulation to recover ownership and access permissions on critical files.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Block SMB Access with Windows Firewall – v1.0.0</h5>
<p>Mitigating lateral movement by creating firewall rules to block SMB traffic on endpoints.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

</div>

### 🛡️ Windows Administration & Hardening (GPO) Labs

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – GPO to Enforce Session Locks – v1.0.0</h5>
<p>Configuring idle-time lockouts to protect physical security of endpoints.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Securely Configure WinRM with GPO – v1.0.0</h5>
<p>Securing remote management traffic using encrypted listeners and policy enforcement.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Windows Defender Hardening via GPO – v1.0.0</h5>
<p>Configuring advanced Defender settings, including real-time scanning and cloud protection.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>LAB – Deployed Exploit Guard via GPO – v1.0.0</h5>
<p>Enabling Attack Surface Reduction (ASR) rules and memory protection through Exploit Guard.</p>
<p align="center" style="margin-top:20px;"><span style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:rgba(255,255,255,0.5); border-radius:5px; font-weight:bold; font-size:0.9em;">Restricted: Request Access</span></p>
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

This section represents applied infrastructure engineering across operating systems, virtualization platforms, and cloud environments. Each lab demonstrates how systems are configured, secured, and validated to meet operational and security requirements.

While selected projects are presented here, they are supported by a larger archive of structured reports, lab documentation, and system configuration records maintained within a private research repository.

Additional documentation is available upon request for professional or technical review.
