---

title: "Webmin Secure Administration & Dual-Homed Architecture"
date: 2026-01-25
author: Eldon Gabriel
tags: [webmin, ubuntu, network-security, system-hardening, virtualization]
excerpt: "Deploy and secure Webmin using dual-homed networking to isolate management traffic and reduce attack surface."
image:
  path: /assets/images/posts/webmin-secure-admin.png
  thumbnail: /assets/images/posts/webmin-secure-admin.png

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>

This lab focused on deploying and securing Webmin on Ubuntu 24.04. The main goal was to use a dual-homed network setup to separate management traffic from external network traffic.

I worked with VirtualBox networking, Netplan configuration, and Webmin service management. I also used tools like `ss` and ping to verify connectivity and service status.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>

I learned how to configure multiple network adapters on a virtual machine and assign static IP addresses using Netplan.

I observed that Webmin listens on all interfaces by default (0.0.0.0), which is not secure. Limiting access to a private interface improves security.

I also ran into a VirtualBox issue where the GUI network name did not match the actual configuration. This showed that checking IP addresses is more reliable than trusting interface labels.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>

Separating management traffic from external traffic reduces the risk of unauthorized access.

By isolating Webmin on a private network, attackers on the WAN cannot detect or access the management port.

This approach supports secure system administration and reduces the overall attack surface.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job / Framework</h1>
</div>

**NICE Framework (SP-SYS-001):**  
Focuses on system setup, network configuration, and troubleshooting.

**ASD Cyber Skills Framework (SADM):**  
Covers secure system configuration and maintaining system performance.

**Practical Use:**  
This setup is commonly used in data centers and cloud environments where management access is restricted to secure internal networks.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>

- Do not expose management interfaces to public networks  
- Use network isolation to improve security  
- Verify network configuration using IP-level checks  
- Use PAM for better authentication control  
- Always validate results with tools like ping and `ss`  

---

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->

<div style="max-width:500px; margin:0 auto; background:rgba(255,255,255,0.05); padding:12px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/reports/REPORT – Webmin Secure Administration (Dual-Homed) – v1.1.0.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:8px; color:#aaa; font-size:0.9em;">
<strong>REPORT – Webmin Secure Administration (Dual-Homed) – v1.1.0</strong>
</p>

</div>

</div>
