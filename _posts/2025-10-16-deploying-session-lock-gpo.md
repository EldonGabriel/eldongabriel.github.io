---
title: "Deploying User Session Lock Policies on a Single Machine"
date: 2025-10-16
author: Eldon Gabriel
tags: [Cybersecurity, Windows, GPO, SystemHardening, EndpointSecurity, MCSI]
excerpt: "Configured Local Group Policy to enforce automatic session locks, improving Windows endpoint security."
image:
  path: "/assets/images/posts/session_lock.png"
  thumbnail: "/assets/images/posts/session_lock.png"
---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Exercise Core Function</h1>
</div>
In this exercise, I focused on hardening a standalone Windows 10 workstation using the **Local Group Policy Editor**. The goal was to define **session lock policies** to automatically lock the machine after inactivity, preventing unauthorized access and reducing security risks. The key configuration involved setting the **Interactive logon: Machine inactivity limit** to 15 seconds.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>
The lab involved navigating the **Local Group Policy Editor** to apply session lock settings:

- Using `gpedit.msc` to configure the machine inactivity limit  
- Running `gpupdate /force` to immediately apply policy changes  
- Verifying functionality by leaving the system idle for 15 seconds  

Key concepts reinforced include **endpoint hardening**, **access control**, and **policy-based security enforcement**.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>
Key observations and lessons from this exercise:

- **Hands-on GPO configuration builds practical skills** in endpoint security  
- **Immediate verification confirms policy effectiveness**  
- **Even small policies significantly reduce exposure** to unauthorized access  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>
Enforcing session locks is critical for enterprise security and compliance:

- Reduces risk of unauthorized access to unattended systems  
- Supports operational security best practices  
- Reinforces the importance of defense-in-depth measures at the endpoint  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job/Framework</h1>
</div>
- **NICE (PR.PT-001 / Protect and Defend roles):** Improves endpoint policy enforcement and operational security  
- **ASD Cyber Skills Framework – Secure Configuration Management:** Demonstrates practical application of endpoint hardening techniques  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>
- Local Group Policy allows precise control over session behavior without Active Directory  
- Automatic session locks reduce the window for unauthorized access  
- Hands-on configuration reinforces real-world endpoint security skills  
- Small, simple policies can have a large impact on overall security posture  

---

See my report below for a complete technical summary and validation of this lab exercise:
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;"> 
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;"> 
    <iframe src="{{ 'assets/reports/REPORT – Applying a Local GPO for Session Lock Enforcement – v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe> 
    <figcaption>REPORT – Applying a Local GPO for Session Lock Enforcement – v1.0.0</figcaption> 
  </div> 
</div>
