---
title: "Enforcing Windows Patching Policies with Local Group Policy"
date: 2025-09-27
author: Eldon Gabriel
tags: [Windows10, GroupPolicy, Patching, Cybersecurity, SystemHardening]
excerpt: "A simple walkthrough showing how to use Local Group Policy to keep Windows 10 patched and protected against new threats."
image:
  path: "assets/images/posts/gpo.png"
  thumbnail: "assets/images/posts/gpo.png"
---

One of the easiest ways for attackers to break into a system is by using **unpatched software**. If updates are not installed, hackers can use old flaws to get in. In this exercise, I used the *Local Group Policy Editor* on a Windows 10 computer to make sure updates are installed **automatically**.  

The goal was simple: **stay secure while keeping the computer easy to use**.  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Configured</h1>
</div>

- **Turned on automatic updates**  
- **Allowed immediate installation** of certain updates  
- **Stopped driver installs** through updates  
- **Prevented auto restarts** when someone is logged in  
- **Left update features available**  
- **Enabled recommended updates** with important ones  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Validation</h1>
</div>

To confirm it worked, I:  

- Opened the *Local Group Policy Editor* (`gpedit.msc`) and applied the settings  
- Ran **`gpupdate /force`** to apply changes right away  
- Checked the results with **`gpresult /r`**  
- Reviewed *Windows Update logs*  
- Captured **video recordings** for proof  

The changes applied **immediately**, showing that Local Group Policy is a quick way to control updates on a single machine.  

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why This Matters</h1>
</div>

Regular patching is one of the **strongest defenses** in cybersecurity. It **closes the door** on new threats before they can cause damage.  

The *“No auto-restart”* rule made the system easier to use, but it also means admins must **plan restarts**. Without reboots, some updates don’t finish, leaving systems exposed.  

In bigger companies, these rules are enforced through **Active Directory Group Policy (AD GPO)**. This allows IT teams to keep **hundreds or thousands** of computers patched in the same way.  

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects
</h2>
  
<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects
</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->
<div style="flex:0 1 500px; background:rgba(255,255,255,0.05); padding:20px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/reports/REPORT – Enforcing Operating System Patching Policy via Local GPO – v1.0.0.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:12px; color:#aaa;">
<strong>REPORT – Enforcing Operating System Patching Policy via Local GPO – v1.0.0</strong>
</p>

</div>

</div>
