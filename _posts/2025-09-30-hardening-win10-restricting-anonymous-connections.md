---
title: "Hardening Windows 10 by Restricting Anonymous Connections"
date: 2025-09-30
author: Eldon Gabriel
tags: [Windows10, GPO, AnonymousAccess, NullSession, Cybersecurity, SystemHardening]
excerpt: "A practical walkthrough on hardening Windows 10 by restricting anonymous connections through Local Group Policy, blocking null session enumeration of shares and named pipes."
image:
  path: "assets/images/posts/nt.png"
  thumbnail: "assets/images/posts/nt.png"
---

Anonymous access has long been a way for attackers to silently enumerate users, groups, and shares on a Windows system. In this exercise, I hardened a standalone Windows 10 machine by configuring **Local Group Policy** settings that restrict null session access and deny anonymous logons. The goal: remove unauthenticated pathways into the system and reduce exposure to common enumeration attacks.  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Applying the Policy</h1>
</div>  

I used **Local Group Policy** paths to configure two main areas:

### Anonymous Access Restrictions

- **Path:** `Computer Configuration → Windows Settings → Security Settings → Local Policies → Security Options`  
- **Policies Configured:**  
  - *Network access: Do not allow anonymous enumeration of SAM accounts and shares* → **Enabled**  
  - *Network access: Restrict anonymous access to Named Pipes and Shares* → **Enabled**  

### User Rights Assignment

- **Path:** `Computer Configuration → Windows Settings → Security Settings → Local Policies → User Rights Assignment`  
- **Policy Configured:**  
  - *Deny access to this computer from the network* → **Guests, Local account**  

### Verification  

I verified the settings with the following command:  

~~~
cmd
reg query HKLM\SYSTEM\CurrentControlSet\Services\LanManServer\Parameters /v RestrictNullSessAccess
~~~
The output confirmed a DWORD value of 0x1, proving the restrictions were successfully applied.

<div style="text-align:center;"> <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why This Matters</h1> </div>

Null sessions are often abused by attackers for reconnaissance before launching targeted attacks. By cutting off anonymous access, organizations can significantly reduce their attack surface and comply with baseline hardening standards such as CIS and NIST 800-53.

For non-technical readers: think of this as locking a building’s utility doors so that strangers can’t sneak inside to scope out the layout before attempting a break-in.

<div style="text-align:center;"> <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Professional Relevance</h1> </div>

This exercise reinforces skills aligned to:

NICE Framework – System Administration (OM-SA-001): Applying OS-level security configurations to protect systems from unauthorized access.

ASD Cyber Skills Framework – System Hardening: Implementing security policies that restrict access and reduce system vulnerabilities.

These capabilities directly map to the responsibilities of junior Security Administrators and IT Operations Technicians.

<div style="text-align:center;"> <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1> </div>

Anonymous access restrictions prevent unauthenticated enumeration.

User Rights assignments harden the system against unwanted network logons.

Command-line validation is critical for proving security controls are active.

Local hardening methods scale to enterprise-wide policies via Active Directory GPO.

For the full step-by-step process and deeper insights, see my full report below:

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;"> <div style="flex: 0 1 45%; min-width: 600px; text-align: center;"> <iframe src="{{ 'assets/reports/REPORT – System Hardening via Local GPO: Restricting Anonymous Connections – v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe> <figcaption>REPORT – System Hardening via Local GPO: Restricting Anonymous Connections – v1.0.0</figcaption> </div> </div>
