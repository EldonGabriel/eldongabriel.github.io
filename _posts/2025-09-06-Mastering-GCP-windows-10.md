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

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Introduction</h1>
</div>

Cloud computing is a core part of modern IT and cybersecurity. To strengthen my virtualization and system administration skills, I created an **independent lab project**: deploying a Windows 10 virtual machine on Google Cloud Platform (GCP).

This project demonstrates my ability to work with cloud infrastructure, configure secure access, and manage a Windows environment outside of traditional on-premises setups.

<section>

<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Cloud Infrastructure Demonstration
</h2>

<div style="display:grid; grid-template-columns:repeat(auto-fit, minmax(350px,1fr)); gap:25px; max-width:800px; margin:auto;">

<div style="background:rgba(255,255,255,0.05); padding:25px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">
<h3 style="color:#fff; border-bottom:2px solid #fff; padding-bottom:10px;">Windows 10 VM on Google Cloud</h3>

<p style="color:#ccc;">
Deployed and administered a Windows 10 virtual machine within Google Cloud Platform, demonstrating cloud infrastructure provisioning and remote system management.
</p>

<iframe width="100%" height="220" src="https://www.youtube.com/embed/rNI50WIqZWc" title="Windows 10 VM on GCP" frameborder="0" allowfullscreen></iframe>

<p style="margin-top:10px; color:#aaa;">
<strong>Focus:</strong> Cloud Virtualization • Infrastructure Provisioning • Remote Administration
</p>

</div>

</div>

</section>

---
  
  <h2 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Lab Objectives</h2>
</div>

The main goals of this lab were:

- Deploy a Windows 10 VM in GCP.
- Configure networking and firewall rules for secure remote access.
- Connect to the system and validate functionality.
- Document the process for professional development.

<div style="text-align:center;">
  <h2 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Steps Taken</h2>
</div>

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

<div style="text-align:center;">
  <h2 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Skills Demonstrated</h2>
</div>

- **Cloud Virtualization:** Deploying and managing Windows environments in GCP.  
- **System Administration:** Performing setup and validation of virtual systems.  
- **Secure Networking:** Configuring firewall rules and controlling RDP access.  

<div style="text-align:center;">
  <h2 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Practical Applications</h2>
</div>

Organizations use this type of deployment to:

- Provide remote desktops for employees.  
- Test applications in isolated environments.  
- Support hybrid infrastructures combining cloud and on-premises resources.  

<div style="text-align:center;">
  <h2 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Conclusion</h2>
</div>

This independent lab reinforced my ability to apply Windows administration skills in a **cloud environment**. By deploying a Windows 10 VM on GCP, I demonstrated hands-on experience in **virtualization, secure configuration, and system management** — all essential skills for modern IT and cybersecurity roles.
