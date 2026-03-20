---
title: "Deploying User Rights Policies on a Single Machine"
date: 2025-10-16
author: Eldon Gabriel
tags: [Cybersecurity, Windows, GPO, SystemHardening, AccessControl, MCSI]
excerpt: "Configured User Rights Assignment policies via Local Group Policy to enforce least privilege and secure Windows endpoints."
image:
  path: "/assets/images/posts/user_rights.png"
  thumbnail: "/assets/images/posts/user_rights.png"
---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Exercise Core Function</h1>
</div>

In this exercise, I focused on hardening a standalone Windows 10 workstation using the **Local Group Policy Editor**. The goal was to define **User Rights Assignment policies** to control which users can perform sensitive system actions, enforce least privilege, and reduce security risks. Key policies configured included logon rights, pagefile creation, symbolic link creation, debugging programs, remote shutdown, device driver management, profiling, and file ownership.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>
The lab involved navigating the **Local Group Policy Editor** to apply security settings for Windows User Rights:

- Using `gpedit.msc` to configure User Rights Assignment policies  
- Running `gpupdate /force` to apply changes immediately  
- Verifying enforcement via **Local Security Policy** `(secpol.msc)`  

Key concepts reinforced include the **principle of least privilege**, **system hardening**, and **access control**.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>
Key observations and lessons from this exercise:

- **Hands-on GPO configuration builds confidence** in endpoint security hardening  
- **Verification through secpol.msc** confirms policy enforcement  
- **Understanding the impact of misconfigured rights** is crucial to prevent privilege escalation  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>
Defining User Rights policies is critical for enterprise defense and compliance:

- Restricts unauthorized administrative actions  
- Reduces risk of privilege escalation and insider misuse  
- Reinforces operational understanding of secure system configuration  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job/Framework</h1>
</div>
- **NICE (OM-SA-001 / System Administrator):** Strengthens endpoint access control and policy enforcement  
- **ASD Cyber Skills Framework – Secure Configuration Management:** Demonstrates practical application of baseline hardening  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>
- Local Group Policy allows precise control of user privileges without requiring Active Directory  
- Properly defined User Rights reduce exposure to privilege escalation  
- Hands-on application reinforces real-world cybersecurity skills  
- Enforcing least privilege is fundamental to Windows system hardening  

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects
</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->
<div style="flex:0 1 500px; background:rgba(255,255,255,0.05); padding:20px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/reports/REPORT – Hardening Windows User Rights via Local Group Policy – v1.0.0.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:12px; color:#aaa;">
<strong>REPORT – Hardening Windows User Rights via Local Group Policy – v1.0.0</strong>
</p>

</div>

</div>
