---
title: "UTM Kali Linux Shared Folder Guide: Persistent File Sharing for Cybersecurity Labs"
date: 2025-10-17
author: Eldon Gabriel
tags: [Cybersecurity, Virtualization, Linux, UTM, SystemAdministration]
excerpt: "Configured a persistent shared folder between macOS and Kali Linux in UTM to enable reliable cross-platform file transfer for cybersecurity lab environments."
image:
  path: "/assets/images/posts/utm_kali_shared_folder.png"
  thumbnail: "/assets/images/posts/utm_kali_shared_folder.png"
---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>
I configured a persistent shared folder between **macOS (host)** and **Kali Linux (guest)** in **UTM**. The goal was to create a reliable method for transferring files—such as reports, tools, and evidence—between both systems.

**Tools and Techniques Used:** `mount`, `/etc/fstab`, and the **9p (Plan 9 Filesystem)** protocol over **VirtIO**.

**Key Concept:** Learning how file systems work in virtual machines and fixing errors when new drivers like **VirtIO-FS** do not function properly.

 

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>
Initially, the VirtIO-FS mount did not work. Kali displayed repeated errors about a missing tag and bad filesystem type. Switching to **9p over VirtIO** immediately resolved the issue.

**Hands-on Skills Gained:**  
- Mounting shared folders in Linux using alternate protocols  
- Configuring `/etc/fstab` for persistence  
- Troubleshooting low-level virtual file system errors  

**Observation:**  
The **9p protocol** was unexpectedly effective. Even when VirtIO-FS support was unavailable, it maintained stable host–guest communication.

 

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>
In cybersecurity labs, shared folders are essential. They allow data to move securely and quickly between systems. A bad mount configuration can delay workflows or break lab operations.

This strengthens **system readiness**, improves **operational efficiency**, and enables secure **evidence handling**—all vital for both enterprise and individual security professionals.

 

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job / Framework</h1>
</div>
- **NIST NICE Role:** System Administrator (OM-SA-001) – maintaining and troubleshooting secure virtual systems  
- **ASD Cyber Skills Framework:** Operate and Maintain – managing secure, resilient lab infrastructure  

This capability helps analysts securely transfer tools, logs, and reports between isolated environments without relying on insecure network paths.

 

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>
- Always know fallback protocols: **9p** works when **VirtIO-FS** fails  
- Use `/etc/fstab` for reliable, automated mounting  
- Mastering cross-platform integration builds confidence in hybrid setups  
- Efficient file transfer supports productivity and secure operations  
- Virtualization troubleshooting is a foundational skill for cybersecurity professionals  

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects
</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->
<div style="flex:0 1 500px; background:rgba(255,255,255,0.05); padding:20px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/guides/GUIDE – UTM Kali Linux Shared Folder Configuration – v1.0.0.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:12px; color:#aaa;">
<strong>GUIDE – UTM Kali Linux Shared Folder Configuration – v1.0.0</strong>
</p>

</div>

</div>
