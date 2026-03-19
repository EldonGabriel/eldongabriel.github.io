---
title: "Secure Linux Management with Cockpit"
date: 2026-01-27
author: Eldon Gabriel
tags: [Linux, Ubuntu, Cockpit, System Administration, Cybersecurity, SSH, UFW, Network Security, Homelab]
excerpt: "Using Cockpit to manage and secure multiple Linux systems from a single web interface."
image:
  path: /assets/images/posts/cockpit.png
  thumbnail: /assets/images/posts/cockpit.png
---

# Centralizing Control: Secure Linux Management with Cockpit

Managing a single Linux server is simple. However, as more systems are added, it becomes harder to track activity and maintain security. This project focused on setting up a web-based tool to manage multiple systems from one place while keeping security in mind.



<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>

This exercise focused on setting up and securing Cockpit, a web-based tool used to manage Linux systems. The goal was to move away from using only the terminal and instead manage systems from a central dashboard.

- **Module:** MSAF – System Administration Fundamentals (Level 2)  
- **Tools & Techniques:** Ubuntu 24.04 LTS, Cockpit, systemd services, UFW (Uncomplicated Firewall), and SSH for connecting multiple systems  
- **Core Focus:** Used basic security concepts such as user access control and network restrictions  



<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>

**Managing Services in One Place**  
I learned how to start, stop, and monitor system services using a web dashboard. This makes it easier to respond to system issues.

**Managing Multiple Systems with SSH**  
One main system was connected to another Linux machine using SSH. This shows that multiple systems can be controlled without installing extra software.

**Security Risks of Web Tools**  
Cockpit gives access to system data like `/etc/passwd` and logs. It also opens port 9090, which must be secured to prevent attacks.


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>

In real environments, it is important to see what is happening on a system. If an admin cannot quickly detect a failed service or an unknown user, it increases response time.

Cockpit makes system management easier, especially for newer administrators. However, access must be restricted using tools like UFW so only trusted users can connect.



<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job / Framework</h1>
</div>

**NIST NICE – System Administrator (SP-SYS-001)**  
This project builds skills in installing software, managing users, and controlling system access.

**ASD Cyber Skills Framework – System Administration (SADM)**  
Shows the ability to deploy systems and apply basic security settings.



<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>

1. **Security Comes First**  
   Access to port 9090 should always be restricted using UFW.

2. **SSH Must Be Secured**  
   Multi-system access depends on SSH. Disable root login and use secure settings.

3. **System Logging is Important**  
   All actions in Cockpit are logged, which helps track activity and meet security requirements.

4. **Simple Tools Scale Well**  
   Using SSH instead of extra software makes systems easier to manage and secure.



<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<div style="max-width:500px; margin:0 auto; background:rgba(255,255,255,0.05); padding:12px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/guides/SOP – Secure Linux Management & Multi-Host Orchestration – v1.0.1.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:8px; color:#aaa; font-size:0.9em;">
<strong>SOP – Secure Linux Management & Multi-Host Orchestration – v1.0.1</strong>
</p>

</div>

</div>


<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Technical Skills Demonstrated</h1>
</div>

- Linux system administration (Ubuntu 24.04)  
- Cockpit web-based system management  
- systemd service management  
- Firewall configuration using UFW  
- SSH-based remote system management  
- Basic system hardening and access control  



<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Conclusion</h1>
</div>

This project showed how Cockpit can simplify Linux system management through a single web interface. It improves visibility and control across multiple systems. However, proper security measures such as firewall rules and SSH hardening are required to protect the system.

When used correctly, Cockpit provides a strong balance between ease of use and secure system administration.
