 ---
title: "Protecting Sensitive Folders with Controlled Folder Access via Local Group Policy"
date: 2025-09-22
author: Eldon Gabriel
tags: [Windows, Security, GPO, Controlled Folder Access, Endpoint Security]
excerpt: "Hands-on experience configuring Controlled Folder Access (CFA) on Windows 10 to protect against ransomware using Local Group Policy."
image:
  path: "assets/images/posts/CFA.png"
  thumbnail: "assets/images/posts/CFA.png"
---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Exercise Core Function</h1>
</div>

In this exercise, I set up **Controlled Folder Access (CFA)** on a Windows 10 machine using **Local Group Policy** to protect against ransomware. I **enabled CFA**, selected folders to protect, and allowed certain applications for **trusted access**. This setup requires **Windows Defender Antivirus** for real-time protection. I used **gpedit.msc** and security settings for CFA, testing both trusted and untrusted applications to ensure functionality. This provided practical experience in **endpoint security** and **system hardening**.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>

I learned how to protect folders from **ransomware** and other **unauthorized changes**. Testing showed that untrusted applications could **not modify protected folders**, while trusted applications could. The exercise demonstrated the need to **verify settings** and understand exceptions for normal workflows. Troubleshooting reinforced the importance of correctly configuring **folder paths** and **trusted applications** to avoid operational issues.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>

**Controlled Folder Access** helps protect against ransomware, a common **enterprise threat**. By restricting write access to sensitive folders, **risk is reduced** and compliance with organizational security policies is supported. This exercise highlights the importance of **proactive endpoint protection** to defend against real-world threats.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job / Framework</h1>
</div>

This exercise develops skills for **Endpoint Security Administrators** and **Cybersecurity Operations Specialists**, aligning with the **NICE Protect and Defend** and **ASD Cyber Skills** frameworks. These skills are directly applicable to roles requiring **protection of critical data** and **secure configuration management**.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>

- Setting up **Controlled Folder Access** strengthens protection against ransomware and **unauthorized access**.  
- Selecting the right **folders** to protect and **applications** to allow ensures smooth operation.  
- Working with **Local Group Policy** and **Windows Defender Exploit Guard** builds practical security skills.  
- Testing confirms that security controls function **without disrupting normal workflows**.  
- Documenting and verifying CFA settings provides **audit-ready evidence** of compliance and **risk management**.
