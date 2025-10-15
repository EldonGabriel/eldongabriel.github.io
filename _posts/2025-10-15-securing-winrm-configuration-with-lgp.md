---
title: "Securing WinRM Configuration with Local Group Policy"
date: 2025-10-15
author: Eldon Gabriel
tags: [Cybersecurity, WinRM, GroupPolicy, WindowsSecurity, SystemHardening, MCSI]
excerpt: "Deployed a Local Group Policy Object to securely configure Windows Remote Management (WinRM) for encrypted, authenticated remote administration."
image:
  path: "/assets/images/posts/winrm.png"
  thumbnail: "/assets/images/posts/winrm.png"
---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Exercise Core Function</h1>
</div>
In this exercise, I focused on securely configuring Windows Remote Management (WinRM) on a standalone Windows 10 workstation using Local Group Policy. The goal was to enforce encrypted communication, disable weak authentication methods, and prevent storage of administrative credentials for safe remote administration.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>
The lab involved navigating the **Local Group Policy Editor** to apply security settings for WinRM.

Key tools and techniques applied:

- Using **gpedit.msc** to configure WinRM Client and Service policies  
- Running **winrm quickconfig** and **winrm get winrm/config** to validate settings  
- Ensuring firewall and network profile configuration supports remote management  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>
Key observations and lessons from this exercise:

- **Hands-on GPO configuration builds confidence** in endpoint security hardening  
- **Verification through PowerShell** confirms policy enforcement (`[Source="GPO"]`)  
- **Network profile and firewall settings** are critical for enabling remote management  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>
Securing WinRM is vital for enterprise defense and compliance:

- Prevents unauthorized access and credential exposure  
- Supports baseline endpoint hardening prior to deployment  
- Reinforces operational understanding of secure remote administration  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job/Framework</h1>
</div>
- **NICE (OM-ADM-001 / System Administration):** Strengthens policy enforcement and endpoint access control  
- **ASD Cyber Skills Framework – Advanced Beginner:** Demonstrates practical application of secure system configuration and validation  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>
- Disable Basic and Digest authentication to eliminate cleartext credentials  
- Require encrypted traffic for all remote management  
- Validate applied settings through PowerShell outputs  
- Local Group Policy ensures consistent and repeatable endpoint hardening  
- Skills learned are directly applicable to enterprise cybersecurity operations  

---

See my report below for a complete technical summary and validation of this lab exercise:
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;"> 
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;"> 
    <iframe src="{{ 'assets/reports/REPORT – WinRM Secure Configuration and Validation – v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe> 
    <figcaption>REPORT – WinRM Secure Configuration and Validation – v1.0.0</figcaption> 
  </div> 
</div>

