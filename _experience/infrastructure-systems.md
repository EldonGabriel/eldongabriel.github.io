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

Modern IT infrastructure depends on stable operating systems, virtualization platforms, and reliable administrative processes. The labs and reports in this section demonstrate hands-on experience managing Windows and Linux systems, building virtual lab environments, and maintaining operational stability across infrastructure components.

### Infrastructure Lab Overview

| Category | Labs |
|--------|------|
| Windows Systems Administration | 11 |
| Linux Systems Administration | 4 |
| Virtualization & Lab Infrastructure | 3 |
| Video Demonstration Labs | 27 |
| **Total Infrastructure Labs Documented** | **45** |

These labs represent hands-on work performed in controlled environments designed to simulate real-world infrastructure administration tasks. Activities include operating system management, virtualization deployment, cloud infrastructure provisioning, system hardening, and operational troubleshooting.

---

## Windows Systems Administration

Hands-on system administration tasks performed in Windows environments, focusing on system management, disk operations, service control, and operational troubleshooting.

**Lab Index**

- **REPORT – Active Directory Bare Metal Recovery (BMR) Backup and Restore – v1.0.0**  
  Demonstrates performing a full system backup and recovery of an Active Directory domain controller using Bare Metal Recovery procedures.

  **Skills Demonstrated:** Active Directory administration, system backup, disaster recovery

- **REPORT – Windows Disk Management Using Command Line – v1.0.0**  
  Using command-line utilities such as `chkdsk` and `fsutil` to analyze disk health, repair file system errors, and manage Windows storage systems.

- **REPORT – Windows Service Management – v1.0.0**  
  Investigating and controlling Windows services using administrative tools and command-line utilities to maintain system stability.

- **REPORT – Windows Event Log Analysis – v1.0.0**  
  Examining system and security event logs to identify operational issues and potential security indicators.


---


## Linux Systems Administration

Administration of Linux-based systems including user management, file permissions, system processes, and log analysis in server environments.

**Lab Index**

- **REPORT – Linux System Admin Commands – v1.0.0**  
  Documentation of common Linux administrative commands including `grep`, `ps`, `lsof`, `df`, and `chmod`, along with additional utilities used for system monitoring, troubleshooting, and resource management.

  **Skills Demonstrated:** Linux CLI administration, process monitoring, system diagnostics, file permission management

- **REPORT – Linux User and Group Management – v1.0.0**  
  Creating and managing user accounts and groups while enforcing proper privilege separation.

- **REPORT – Linux File Permissions and Ownership – v1.0.0**  
  Understanding and applying Linux permission models to secure system resources.

- **REPORT – Linux Process and Service Management – v1.0.0**  
  Monitoring system processes and managing services using system administration tools.

---


## Virtualization & Lab Infrastructure

Building and managing virtual environments used for cybersecurity research, testing, and infrastructure simulation.

**Lab Index**

- **REPORT – VirtualBox Network Modes – v1.0.0**  
  Exploring NAT, Bridged, Host-Only, and Internal networking configurations used to control virtual machine connectivity.

- **REPORT – System Administration Virtualization in Cybersecurity – v1.0.1**  
  Demonstrating how virtualization enables isolated testing environments for system administration and security research.

- **REPORT – Virtual Lab Environment Deployment – v1.0.0**  
  Designing and deploying virtual lab environments used to simulate real-world infrastructure and security scenarios.

---

## Video Demonstrations

The following videos demonstrate practical system administration, virtualization, cloud deployment, and security configuration tasks. These demonstrations complement the written technical reports within this portfolio and showcase hands-on lab execution in controlled environments.

---

## Virtualization

- **Install and Configure VMware ESXi with vSphere in Windows and Linux VMs**  
  Demonstrates deploying virtual machines within VMware Hands-on Labs using ESXi and the vSphere client. The lab validates network connectivity between a Linux and Windows VM within the same subnet.

  **Skills Demonstrated:** Virtual machine deployment, vSphere administration, network configuration, connectivity testing

- **Create a Snapshot of a Virtual Machine to Recover the OS to a Safe State**  
  Shows how to create and manage VM snapshots to preserve system state before making configuration changes or conducting security testing.

  **Skills Demonstrated:** Snapshot management, virtualization safety practices, system rollback planning

- **Lab Setup – Create a Virtual Machine in VMware**  
  Demonstrates deploying Kali Linux and Windows 11 ARM virtual machines using VMware Fusion and configuring NAT networking to validate VM communication.

  **Skills Demonstrated:** VM deployment, virtualization networking, OS installation

---

## Cloud Infrastructure

- **Lab Setup – Deploy a Virtual Machine in AWS**  
  Demonstrates launching an Ubuntu virtual machine in Amazon EC2, generating SSH keys, configuring security groups, and validating remote access from Kali Linux.

  **Skills Demonstrated:** Cloud VM provisioning, SSH key management, firewall configuration

- **Lab Setup – Deploy a Virtual Machine in Google Cloud Platform (GCP)**  
  Shows how to deploy a Linux virtual machine using Google Compute Engine and configure secure SSH access.

  **Skills Demonstrated:** Cloud infrastructure deployment, SSH authentication, firewall rules

- **Windows 10 VM on Google Cloud Platform (GCP)**  
  Demonstrates deploying and managing a Windows virtual machine in GCP and validating system functionality.

  **Skills Demonstrated:** Cloud administration, Windows VM provisioning, secure remote access

---

## Linux System Administration

- **Linux Firewall Configuration with Shorewall | Restricted SSH Access Lab**  
  Demonstrates configuring a host-based firewall on Ubuntu to restrict SSH access to a trusted IP address using zone-based firewall rules.

  **Skills Demonstrated:** Linux firewall configuration, access control, network security

- **Linux Performance Monitoring with SAR (sysstat)**  
  Shows installation and usage of SAR to monitor CPU, memory, disk activity, and network performance on Linux systems.

  **Skills Demonstrated:** System monitoring, performance analysis, Linux administration

- **Cockpit Linux Administration Lab | Multi-Host Management**  
  Demonstrates installing Cockpit and managing multiple Linux hosts through a web-based administration interface.

  **Skills Demonstrated:** Linux administration, remote system management, service control

- **Webmin Linux Administration and Firewall Configuration**  
  Shows how to install Webmin and configure firewall restrictions to control administrative access.

  **Skills Demonstrated:** Linux server management, firewall configuration, remote administration

---

## Windows System Administration

- **Use Procmon to View and Analyze Running Processes**  
  Demonstrates capturing and analyzing system activity using Microsoft Process Monitor.

  **Skills Demonstrated:** Process monitoring, system analysis, troubleshooting

- **Use a Password Manager to Protect Sensitive Credentials**  
  Demonstrates secure credential storage using a password management tool.

  **Skills Demonstrated:** credential protection, security hygiene

- **Recover File Ownership Using the Windows Registry**  
  Shows registry-based techniques for recovering ownership of protected files.

  **Skills Demonstrated:** NTFS permissions management, registry administration

- **Restrict Permissions of Untrusted Users via Windows Registry**  
  Demonstrates preventing unauthorized execution of system utilities using registry-based restrictions.

  **Skills Demonstrated:** system hardening, access control

- **Securing Sensitive Folders with Windows Access Permissions**  
  Demonstrates configuring NTFS permissions to protect sensitive directories.

  **Skills Demonstrated:** access control, file security

- **Configure Windows Firewall and Block SMB Access**  
  Demonstrates creating firewall rules to prevent SMB traffic.

  **Skills Demonstrated:** firewall administration, network hardening

---

## Windows Administration & Maintenance

- **Network and Sharing Center – Connectivity Troubleshooting**  
  Demonstrates reviewing network connections and diagnosing connectivity issues.

  **Skills Demonstrated:** Windows networking, troubleshooting

- **Windows Credential Manager Lab**  
  Demonstrates managing stored credentials used for network resources.

  **Skills Demonstrated:** credential management

- **BitLocker Preparation – Disk Security Planning**  
  Demonstrates preparing a Windows drive for encryption and configuring NTFS permissions.

  **Skills Demonstrated:** disk management, encryption planning

- **Programs and Features – Application Management**  
  Demonstrates installing and uninstalling software using Windows administrative tools.

  **Skills Demonstrated:** software lifecycle management

- **Windows System Information (msinfo32)**  
  Demonstrates collecting system information for auditing and troubleshooting.

  **Skills Demonstrated:** system auditing, hardware inspection

- **Windows Event Viewer – System Monitoring**  
  Demonstrates reviewing system and security logs for operational issues.

  **Skills Demonstrated:** log analysis, system monitoring

- **Windows Registry Editor – Safe Configuration Changes**  
  Demonstrates safely creating, editing, and deleting registry keys.

  **Skills Demonstrated:** registry administration, configuration management

- **Task Scheduler – Automated Maintenance Tasks**  
  Demonstrates scheduling automated maintenance tasks using Windows Task Scheduler.

  **Skills Demonstrated:** system automation, maintenance workflows

- **Windows Defender Firewall Configuration**  
  Demonstrates managing firewall rules to control network traffic.

  **Skills Demonstrated:** network security, firewall configuration

- **Windows Disk Optimization**  
  Demonstrates analyzing and optimizing drive performance.

  **Skills Demonstrated:** system maintenance

- **Windows Disk Cleanup Utility**  
  Demonstrates removing temporary files to improve system performance.

  **Skills Demonstrated:** storage management

  ---

## Portfolio Documentation

This section summarizes hands-on infrastructure, virtualization, cloud, and operating system administration labs performed as part of my ongoing cybersecurity and systems administration training.

While this page highlights representative reports and demonstrations, it is supported by a much larger collection of technical documentation, lab notes, and system configuration records maintained within my research archive.

To keep the site streamlined and focused on key projects, not all documentation artifacts are displayed directly.

Complete reports, lab documentation, and supporting technical materials are available upon request for professional or technical review.

---

## Video Demonstrations

The following videos demonstrate practical system administration, virtualization, cloud deployment, and security configuration tasks. These demonstrations complement the written technical reports within this portfolio and showcase hands-on lab execution in controlled environments.

---

## Virtualization & Lab Infrastructure

- **Install and Configure VMware ESXi with vSphere in Windows and Linux VMs**  
  Demonstrates deploying virtual machines within VMware Hands-on Labs using ESXi and the vSphere client. The lab validates network connectivity between a Linux and Windows VM within the same subnet.

  **Skills Demonstrated:** Virtual machine deployment, vSphere administration, network configuration, connectivity testing

- **Create a Snapshot of a Virtual Machine to Recover the OS to a Safe State**  
  Shows how to create and manage VM snapshots to preserve system state before making configuration changes or conducting security testing.

  **Skills Demonstrated:** Snapshot management, virtualization safety practices, system rollback planning

- **Lab Setup – Create a Virtual Machine in VMware**  
  Demonstrates deploying Kali Linux and Windows 11 ARM virtual machines using VMware Fusion and configuring NAT networking to validate VM communication.

  **Skills Demonstrated:** VM deployment, virtualization networking, OS installation

---

## Cloud Infrastructure Labs

- **Lab Setup – Deploy a Virtual Machine in AWS**  
  Demonstrates launching an Ubuntu virtual machine in Amazon EC2, generating SSH keys, configuring security groups, and validating remote access from Kali Linux.

  **Skills Demonstrated:** Cloud VM provisioning, SSH key management, firewall configuration

- **Lab Setup – Deploy a Virtual Machine in Google Cloud Platform (GCP)**  
  Shows how to deploy a Linux virtual machine using Google Compute Engine and configure secure SSH access.

  **Skills Demonstrated:** Cloud infrastructure deployment, SSH authentication, firewall rules

- **Windows 10 VM on Google Cloud Platform (GCP)**  
  Demonstrates deploying and managing a Windows virtual machine in GCP and validating system functionality.

  **Skills Demonstrated:** Cloud administration, Windows VM provisioning, secure remote access

---

## Linux System Administration Labs

- **Linux Firewall Configuration with Shorewall | Restricted SSH Access Lab**  
  Demonstrates configuring a host-based firewall on Ubuntu to restrict SSH access to a trusted IP address using zone-based firewall rules.

  **Skills Demonstrated:** Linux firewall configuration, access control, network security

- **Linux Performance Monitoring with SAR (sysstat)**  
  Shows installation and usage of SAR to monitor CPU, memory, disk activity, and network performance on Linux systems.

  **Skills Demonstrated:** System monitoring, performance analysis, Linux administration

- **Cockpit Linux Administration Lab | Multi-Host Management**  
  Demonstrates installing Cockpit and managing multiple Linux hosts through a web-based administration interface.

  **Skills Demonstrated:** Linux administration, remote system management, service control

- **Webmin Linux Administration and Firewall Configuration**  
  Shows how to install Webmin and configure firewall restrictions to control administrative access.

  **Skills Demonstrated:** Linux server management, firewall configuration, remote administration

---

## Windows System Administration Labs

- **Use Procmon to View and Analyze Running Processes**  
  Demonstrates capturing and analyzing system activity using Microsoft Process Monitor.

  **Skills Demonstrated:** Process monitoring, system analysis, troubleshooting

- **Use a Password Manager to Protect Sensitive Credentials**  
  Demonstrates secure credential storage using a password management tool.

  **Skills Demonstrated:** credential protection, security hygiene

- **Recover File Ownership Using the Windows Registry**  
  Shows registry-based techniques for recovering ownership of protected files.

  **Skills Demonstrated:** NTFS permissions management, registry administration

- **Restrict Permissions of Untrusted Users via Windows Registry**  
  Demonstrates preventing unauthorized execution of system utilities using registry-based restrictions.

  **Skills Demonstrated:** system hardening, access control

- **Securing Sensitive Folders with Windows Access Permissions**  
  Demonstrates configuring NTFS permissions to protect sensitive directories.

  **Skills Demonstrated:** access control, file security

- **Configure Windows Firewall and Block SMB Access**  
  Demonstrates creating firewall rules to prevent SMB traffic.

  **Skills Demonstrated:** firewall administration, network hardening

---

## Windows Administration & Maintenance Labs

- **Network and Sharing Center – Connectivity Troubleshooting**  
  Demonstrates reviewing network connections and diagnosing connectivity issues.

  **Skills Demonstrated:** Windows networking, troubleshooting

- **Windows Credential Manager Lab**  
  Demonstrates managing stored credentials used for network resources.

  **Skills Demonstrated:** credential management

- **BitLocker Preparation – Disk Security Planning**  
  Demonstrates preparing a Windows drive for encryption and configuring NTFS permissions.

  **Skills Demonstrated:** disk management, encryption planning

- **Programs and Features – Application Management**  
  Demonstrates installing and uninstalling software using Windows administrative tools.

  **Skills Demonstrated:** software lifecycle management

- **Windows System Information (msinfo32)**  
  Demonstrates collecting system information for auditing and troubleshooting.

  **Skills Demonstrated:** system auditing, hardware inspection

- **Windows Event Viewer – System Monitoring**  
  Demonstrates reviewing system and security logs for operational issues.

  **Skills Demonstrated:** log analysis, system monitoring

- **Windows Registry Editor – Safe Configuration Changes**  
  Demonstrates safely creating, editing, and deleting registry keys.

  **Skills Demonstrated:** registry administration, configuration management

- **Task Scheduler – Automated Maintenance Tasks**  
  Demonstrates scheduling automated maintenance tasks using Windows Task Scheduler.

  **Skills Demonstrated:** system automation, maintenance workflows

- **Windows Defender Firewall Configuration**  
  Demonstrates managing firewall rules to control network traffic.

  **Skills Demonstrated:** network security, firewall configuration

- **Windows Disk Optimization**  
  Demonstrates analyzing and optimizing drive performance.

  **Skills Demonstrated:** system maintenance

- **Windows Disk Cleanup Utility**  
  Demonstrates removing temporary files to improve system performance.

  **Skills Demonstrated:** storage management

  ---

## Portfolio Documentation

This section summarizes hands-on infrastructure, virtualization, cloud, and operating system administration labs performed as part of my ongoing cybersecurity and systems administration training.

While this page highlights representative reports and demonstrations, it is supported by a much larger collection of technical documentation, lab notes, and system configuration records maintained within my research archive.

To keep the site streamlined and focused on key projects, not all documentation artifacts are displayed directly.

Complete reports, lab documentation, and supporting technical materials are available upon request for professional or technical review.
