---
title: "Protecting Windows 10 with Hardened UAC Settings"
date: 2025-09-24
author: Eldon Gabriel
tags: [Windows10, UAC, GroupPolicy, Cybersecurity, SystemHardening]
excerpt: "A practical walkthrough on hardening Windows 10 UAC settings using Group Policy to enforce credential prompts and secure desktop elevation."
image:
  path: "assets/images/posts/hardeninguac.png"
  thumbnail: "assets/images/posts/hardeninguac.png"
---

When it comes to system security, one of the easiest attack paths is when users (or even admins) can click **_“Yes”_** without thinking. That’s where **_User Account Control (UAC)_** steps in. It forces anyone—standard users or admins—to stop, authenticate, and prove they should be making a sensitive change.

For this exercise, I used the **_Local Group Policy Editor_** to tighten UAC and make sure credentials were required for all administrative actions. The goal: stop malicious software or unauthorized users from sneaking changes past me.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Configured</h1>
</div>

- **_Enabled Admin Approval Mode_** for the built-in Administrator account  
- **_Required credentials for all elevation prompts_** (not just a quick “Yes” click)  
- **_Forced prompts to appear on the secure desktop_** to block spoofing attempts  
- **_Ensured installations trigger prompts_** before making changes  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Validation</h1>
</div>

After applying the policies, I ran an application with admin privileges. Instead of a casual prompt, I was forced onto the **_secure desktop_** to enter my credentials. Exactly the behavior I wanted—clear evidence that the system was properly hardened.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why This Matters</h1>
</div>

By enforcing UAC through Group Policy, I reduced the risk of **_unauthorized changes, credential theft, and privilege escalation_**. Even built-in administrators have to prove themselves before executing sensitive actions. It’s a small step in system hardening, but one that creates a huge barrier for attackers.  

For a deeper dive into the exact configuration steps, validation process, and supporting observations, check out my full **_UAC Hardening Report_** below. It details every policy path and setting applied, so you can see exactly how this exercise strengthens system security.

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects
</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->
<div style="flex:0 1 500px; background:rgba(255,255,255,0.05); padding:20px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/reports/REPORT – Harden UAC via Local Group Policy – v1.0.0.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:12px; color:#aaa;">
<strong>REPORT – Harden UAC via Local Group Policy – v1.0.0</strong>
</p>

</div>

</div>>
