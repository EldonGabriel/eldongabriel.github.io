---
title: "Deploying Local Group Policy to Harden SMB Sessions"
date: 2025-10-13
author: Eldon Gabriel
tags: [Windows10, GPO, SMB, GroupPolicy, EndpointHardening, Cybersecurity, MCSI]
excerpt: "A hands-on walkthrough of using Local Group Policy and the Windows Registry to enforce SMB signing, disable SMBv1, and reduce the risk of credential theft and session hijacking."
image:
  path: "assets/images/posts/shield.png"
  thumbnail: "assets/images/posts/shield.png"
---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Exercise Core Function</h1>
</div>
In this exercise, I focused on hardening SMB communication on a standalone Windows 10 workstation using Local Group Policy and a registry change. The goal was to enforce secure authentication, disable legacy protocols, and prevent credential theft in a controlled environment.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>
The lab involved navigating the **Local Group Policy Editor** and registry paths to strengthen SMB client and server security.

Key tools and techniques applied:

- Using `gpedit.msc` to apply SMB signing and protocol settings  
- Editing the **Registry** to disable SMBv1  
- Verifying policy application and system behavior through PowerShell and SMB diagnostics  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>
Key observations and lessons from this exercise:

- **Hands-on configuration reinforces endpoint hardening skills**  
- **Policy validation ensures intended security outcomes**  
- **Disabling legacy protocols reduces exposure to real-world attack vectors**  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>
Securing SMB traffic is critical for enterprise security:

- Prevents credential theft via packet capture or replay attacks  
- Enforces **data integrity** and **authentication** through SMB signing  
- Removes outdated attack surfaces by disabling SMBv1  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job/Framework</h1>
</div>
- **NICE (NIST):** *System Administration (OM-SA-001)* — configuring and validating OS security controls  
- **ASD Cyber Skills Framework – Advanced Beginner:** *Secure System Configuration (SS-02)* — applying policy standards and baseline hardening  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>
- **SMB signing enforces integrity and authentication**, stopping replay and tampering attacks  
- **Disabling SMBv1 removes legacy attack surfaces**, applying Least Functionality  
- **Idle session timeouts reduce exposure windows** for abandoned sessions  
- **Local Group Policy enables repeatable, scalable endpoint hardening**  

---

See my report below for a complete technical summary and validation of this lab exercise:

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;">
    <iframe src="{{ 'assets/reports/REPORT – SMB Hardening for Credential Theft Protection – v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe>
    <figcaption>REPORT – SMB Hardening for Credential Theft Protection – v1.0.0</figcaption>
  </div>
</div>
