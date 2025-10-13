---
title: "Deploying Local Group Policy to Strengthen Windows Security"
date: 2025-10-12
author: Eldon Gabriel
tags: [Cybersecurity, Windows, GPO, EndpointSecurity, MCSI]
excerpt: "Hands-on exercise applying Local Group Policy settings to harden a Windows 10 workstation and improve system security posture."
image:
  path: "assets/images/posts/local_gpo_lab.png"
  thumbnail: "assets/images/posts/local_gpo_lab.png"
---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Exercise Core Function</h1>
</div> 
In this exercise, I focused on enhancing the security of a standalone Windows workstation by applying a Local Group Policy Object (GPO). The goal was to reinforce system integrity, access control, and protocol hardening in a controlled environment.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>
The lab involved navigating the **Local Group Policy Editor** to configure policies that strengthen endpoint security.  

Key tools and techniques applied:

- Using **gpedit.msc** to locate and apply policy settings  
- Exploring **Administrative Templates** and **Security Settings** paths  
- Verifying policy application and persistence on a standalone workstation  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>
Key observations and lessons from this exercise:

- **Hands-on configuration builds foundational skills** in system hardening  
- **Validating policy changes** ensures intended security outcomes  
- **Understanding GPO precedence** is critical for consistent policy enforcement  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>
Applying local GPOs is important for enterprise security and compliance:

- Reduces exposure to unauthorized access and misconfigurations  
- Supports baseline system hardening before deployment in larger environments  
- Enhances operational security understanding for both isolated and domain-connected systems  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job/Framework</h1>
</div>
- **NICE (Cyber Defense Analyst / IT Operations Technician):** Reinforces endpoint hardening, policy validation, and system access management  
- **ASD Cyber Skills Framework – Advanced Beginner:** Highlights practical application of policy enforcement and baseline security controls  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>
- Local GPOs provide direct control over system security posture  
- Validating and documenting applied settings ensures consistency  
- Baseline policy enforcement reduces the risk of exploits and misconfigurations  
- Skills learned are directly transferable to professional enterprise security roles  

---

See my report below for a complete technical summary and validation of this lab exercise:
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;"> 
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;"> 
    <iframe src="{{ 'assets/reports/REPORT – Deploy Local GPO for Windows Security Policies – v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe> 
    <figcaption>REPORT – Deploy Local GPO for Windows Security Policies – v1.0.0.pdf</figcaption> 
  </div> 
</div>
