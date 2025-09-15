---
title: "Hardening Windows Security with GPO"
date: 2025-09-09
author: Eldon Gabriel
tags: [Cybersecurity, Windows, GPO, Endpoint Security]
excerpt: "A hands-on look at securing Windows machines using Group Policy Objects for application control and secure credential entry."
image:
  path: "assets/images/posts/windowshardening.png"
  thumbnail: "assets/images/posts/windowshardening.png"
---

This blog covers two practical exercises I completed in Windows system hardening using Group Policy Objects (GPOs). First, I restricted the ability to install applications to reduce risk from unauthorized software. Second, I enforced secure credential entry to protect sensitive logins from malware or local attacks.


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Exercise Core Function</h1>
</div>
- Restrict application installations via GPO to prevent unauthorized software.
- Enforce secure credential entry with Secure Desktop and logon restrictions.


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>
- Explored Local Group Policy settings for application installation control and credential management.
- Configured Secure Desktop and credential entry restrictions for safer logons.
- Used tools and commands like `gpedit.msc` and `gpresult /r` to verify policy enforcement.
- Practiced understanding Windows security options, including credential UI, logon behavior, and administrative account enumeration.
- Applied these configurations in line with endpoint security best practices and system hardening frameworks.


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>
- GPOs are a powerful way to enforce security policies at the endpoint level.
- Hands-on lab experience highlighted the importance of testing policies before enterprise deployment.
- Observed that small changes, like disabling automatic logon or restricting software installs, significantly reduce attack surfaces.
- Learned troubleshooting steps for policy enforcement, including verifying effective settings and understanding policy precedence.


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>
- Properly configured GPOs help prevent unauthorized software installation and credential theft, reducing enterprise risk.
- These exercises demonstrate real-world ways to enforce compliance, strengthen endpoint security, and reduce lateral movement by attackers.
- Even small configuration changes can have a significant impact on operational security and protecting sensitive data.


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job / Framework</h1>
</div>

- These exercises map to **System Administrator / Security Operations roles (NIST NICE: Protection and Defense Awareness and Training (PR.AT), Information Protection Processes and Procedures (PR.IP))**, focusing on access control and endpoint protection.
- Skills gained are directly applicable in professional environments for hardening Windows endpoints, mitigating insider threats, and supporting compliance frameworks like ISO 27001 or NIST CSF.


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>
- GPOs enable administrators to enforce critical security policies across endpoints.
- Testing policy application is essential before enterprise-wide rollout.
- Small configuration changes, like secure logon enforcement and application restriction, greatly reduce risk.
- Hands-on labs bridge theory with real-world cybersecurity application.


<div style="text-align:center;">
  <h3 style="display: inline-block; border-bottom: 3px solid #fff; padding-bottom: 5px;">Related Projects</h3>
</div>

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;">
    <iframe src="{{ '/assets/reports/REPORT – GPO Hardening for Windows Application Control – v1.0.0.pdf' | relative_url }}" width="100%" height="800px" style="border:1px solid #ccc;"></iframe>
    <figcaption>REPORT – GPO Hardening for Windows Application Control – v1.0.0</figcaption>
  </div>
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;">
    <iframe src="{{ '/assets/reports/REPORT – Secure Credential Entry via Group Policy Objective (GPO) – v1.0.0.pdf' | relative_url }}" width="100%" height="800px" style="border:1px solid #ccc;"></iframe>
    <figcaption>REPORT – Secure Credential Entry via GPO – v1.0.0</figcaption>
  </div>
</div>
