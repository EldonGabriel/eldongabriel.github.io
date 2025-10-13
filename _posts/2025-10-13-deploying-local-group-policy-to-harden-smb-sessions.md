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

Securing SMB communications is a practical, high-impact control for stopping credential theft and session hijacking before attackers can move laterally. In this exercise I hardened a standalone Windows endpoint using **Local Group Policy (LGPO)** and a registry change to:

- Enforce SMB signing for both clients and servers,
- Disable the legacy **SMBv1** protocol, and
- Block unencrypted password exchanges while applying an idle session timeout.

These steps close common attack vectors used by tools that capture or replay SMB authentication traffic.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Applying the Policy</h1>
</div>  

I used Local Group Policy paths and a registry edit to configure client and server SMB settings, and verified SMBv1 was disabled.  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why This Matters</h1>
</div> 

Unsigned or legacy SMB traffic can be intercepted, replayed, or manipulated by an attacker. Enforcing SMB signing ensures **data integrity** and **authentication**, while disabling SMBv1 removes an outdated attack surface. Together, these controls reduce the risk of credential theft and lateral movement.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Professional Relevance</h1>
</div>

This exercise maps to practical job tasks and industry frameworks:

- **NICE (NIST):** *System Administration (OM-SA-001)* — configuring and validating OS security controls.  
- **ASD Cyber Skills Framework:** *Secure System Configuration (SS-02)* — applying configuration standards to reduce exploitable features.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>

- **SMB signing enforces data integrity and authentication**, stopping packet tampering and replay attacks.  
- **Disabling SMBv1 applies Least Functionality**, removing legacy attack surfaces exploited by real-world malware.  
- **Idle session timeouts reduce exposure windows** for hijacked or abandoned sessions.  
- **Local Group Policy demonstrates repeatable endpoint hardening** that scales into enterprise GPOs.

---

See my report below for a complete technical summary and validation of this lab exercise:

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;">
    <iframe src="{{ 'assets/reports/REPORT – SMB Hardening for Credential Theft Protection – v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe>
    <figcaption>REPORT – SMB Hardening for Credential Theft Protection – v1.0.0</figcaption>
  </div>
</div>
