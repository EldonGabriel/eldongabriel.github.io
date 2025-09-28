---
title: "Hardening Windows 10 with Password & Account Lockout Policies"
date: 2025-09-28
author: Eldon Gabriel
tags: [Windows10, GPO, PasswordPolicy, AccountLockout, Cybersecurity, SystemHardening]
excerpt: "A hands-on walkthrough of configuring Windows 10 Local Group Policy to enforce strong password and account lockout settings, defending against brute-force and password guessing attacks."
image:
  path: "assets/images/posts/door.png"
  thumbnail: "assets/images/posts/door.png"
---

Strengthening authentication controls is one of the most effective ways to stop attackers before they ever get inside a system. In this exercise, I configured a Windows 10 machine with **strict password and account lockout settings** using the Local Group Policy Editor (`gpedit.msc`). The goal: defend against **password guessing** and **brute-force attacks** by eliminating weak sign-in options and enforcing strong password rules.  


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Applying the Policy</h1>
</div>  

I used **Local Group Policy** paths to configure three main areas:  

- **Logon Policy**  
  Disabled **convenience PIN sign-in** to remove weaker authentication fallbacks.  
<br>
- **Password Policy**  
  - Minimum password length: **10 characters**  
  - Password complexity: **Enabled** (uppercase, lowercase, numbers, symbols)  
  - Password history: **5 remembered passwords**  
  - Maximum password age: **90 days**  
  - Minimum password age: **24 hours**  
  - Reversible encryption: **Disabled**
<br>
- **Account Lockout Policy**  
  - Threshold: **5 failed logon attempts**  
  - Lockout duration: **15 minutes**  
  - Reset counter after: **15 minutes**  

Verification steps included forcing policy updates with `gpupdate /force`, reviewing settings in **secpol.msc**, and simulating failed login attempts to confirm lockout behavior.  


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why This Matters</h1>
</div> 

Weak or reused passwords remain one of the **top entry points** for attackers. By enforcing **length, complexity, and lockout controls**, organizations dramatically reduce the success rate of brute-force attempts.  

Even in a single-machine lab, these principles scale directly to enterprise environments via **Active Directory GPOs**. This approach supports compliance with **CIS Benchmarks**, **NIST 800-53**, and similar industry standards.  

For non-technical readers: imagine a door that automatically bolts itself after someone tries the wrong key too many times. That’s what account lockout policies do for user accounts.  


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Professional Relevance</h1>
</div>

This exercise reinforces skills aligned to:  

- **NICE Framework – System Administration (OM-SA-001):** Configuring operating system security settings and enforcing organizational policies.  
- **ASD Cyber Skills Framework – System Hardening:** Applying technical controls that reduce vulnerabilities and enforce compliance with security standards.  

These tasks directly map to the work of **IT Operations Technicians** and **junior Security Administrators** responsible for day-to-day system defense.  


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>

- **Password complexity and expiration** strengthen authentication baselines.  
- **Account lockout policies** disrupt brute-force and password guessing attacks.  
- **Verification matters** — security settings only count if they are tested.  
- Lab-based configurations scale directly into **enterprise compliance baselines**.  

For the full step-by-step process and deeper insights, see my **full report** below:  

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;">
    <iframe src="{{ 'assets/reports/REPORT – Deploying Strict Password & Account Lockout GPO – v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe>
    <figcaption>REPORT – Deploying Strict Password & Account Lockout GPO – v1.0.0</figcaption>
  </div>
</div>
