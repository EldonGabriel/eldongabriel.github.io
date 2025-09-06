---
title: "Mastering GCP: Windows 10 VM Deployment"
date: 2025-09-06
author: Eldon Gabriel
tags: [Windows, GCP, Virtualization, Cybersecurity, Cloud]
excerpt: "An independent lab demonstrating deployment of a Windows 10 virtual machine on Google Cloud Platform, showcasing cloud virtualization, secure configuration, and system administration skills."
image: 
  path: "/assets/images/posts/gcpblog.png"
  thumbnail: "/assets/images/posts/gcpblog.png"
---

<center>
  <h1 style="display: inline-block; width: 50%; border-bottom: 3px solid #fff; padding-bottom: 4px;">Introduction</h1>
</center>

Cloud computing is a core part of modern IT and cybersecurity. To strengthen my virtualization and system administration skills, I created an **independent lab project**: deploying a Windows 10 virtual machine on Google Cloud Platform (GCP).

This project demonstrates my ability to work with cloud infrastructure, configure secure access, and manage a Windows environment outside of traditional on-premises setups.

You can watch the full lab demonstration here: [Watch Video](https://youtu.be/rNI50WIqZWc)

<center>
  <h2 style="display: inline-block; width: 50%; border-bottom: 3px solid #fff; padding-bottom: 4px;">Lab Objectives</h2>
</center>

The main goals of this lab were:

- Deploy a Windows 10 VM in GCP.
- Configure networking and firewall rules for secure remote access.
- Connect to the system and validate functionality.
- Document the process for professional development.

<center>
  <h2 style="display: inline-block; width: 50%; border-bottom: 3px solid #fff; padding-bottom: 4px;">Steps Taken</h2>
</center>

### 1. Provisioning the VM
I logged into the GCP Console and used **Compute Engine** to create a new instance.

- **Operating System:** Windows 10 Pro  
- **Resources:** 2 vCPUs, 4 GB RAM  
- **Storage:** 50 GB SSD boot disk  

### 2. Securing Access
Configured firewall rules to allow **Remote Desktop Protocol (RDP)** traffic on port 3389.

### 3. Generating Credentials and Connecting
Created a username and password in the GCP console, then connected to the VM using an RDP client.

### 4. System Validation
Once inside the VM, I:

- Confirmed the **Local Server name** was correctly set.
- Verified that **50 GB of storage** was available on the C: drive.

> I did not check CPU, RAM, or OS details, as exposing these values is unnecessary and follows **cybersecurity best practices**.

<center>
  <h2 style="display: inline-block; width: 50%; border-bottom: 3px solid #fff; padding-bottom: 4px;">Key Skills Demonstrated</h2>
</center>

- **Cloud Virtualization:** Deploying and managing Windows environments in GCP.  
- **System Administration:** Performing setup and validation of virtual systems.  
- **Secure Networking:** Configuring firewall rules and controlling RDP access.  

<center>
  <h2 style="display: inline-block; width: 50%; border-bottom: 3px solid #fff; padding-bottom: 4px;">Practical Applications</h2>
</center>

Organizations use this type of deployment to:

- Provide remote desktops for employees.  
- Test applications in isolated environments.  
- Support hybrid infrastructures combining cloud and on-premises resources.  

<center>
  <h2 style="display: inline-block; width: 50%; border-bottom: 3px solid #fff; padding-bottom: 4px;">Conclusion</h2>
</center>

This independent lab reinforced my ability to apply Windows administration skills in a **cloud environment**. By deploying a Windows 10 VM on GCP, I demonstrated hands-on experience in **virtualization, secure configuration, and system management** — all essential skills for modern IT and cybersecurity roles.
