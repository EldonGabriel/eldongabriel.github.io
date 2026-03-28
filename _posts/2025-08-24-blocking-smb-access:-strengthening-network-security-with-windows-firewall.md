---
title: "Blocking SMB Access: Strengthening Network Security with Windows Firewall"
date: 2025-08-24
author: Eldon Gabriel
tags: [cybersecurity, portfolio, SMB, firewall, network-security]
excerpt: "A hands-on guide to turning on Windows Firewall, blocking SMB traffic, and understanding protocol security risks."
image:
  path: "/assets/images/smb.png"
  thumbnail: "/assets/images/smb.png"
---

<p>As a Security Systems Specialist, I focus on building hands-on skills that help protect real systems. In this task, I configured Windows Firewall to block Server Message Block (SMB) traffic. This shows how host-based security controls can reduce the risk of network attacks.</p>

<p>This work connects to my report, where I explain what SMB is used for, how it works in file sharing, and the security risks it can create in modern networks.</p>

<center><h3>Foundational Knowledge</h3></center>

<p>SMB is a protocol that lets computers share files, printers, and other resources on a network. It is commonly used in Windows environments to support teamwork and resource sharing.</p>

<p>However, SMB is also a common target for cyber attacks, especially older versions like SMBv1. These older versions have known weaknesses that attackers can exploit.</p>

<p>Blocking unnecessary SMB traffic is an important security step. It helps protect systems from attacks like EternalBlue and WannaCry.</p>

<p>In this exercise, I enabled Windows Firewall and created a rule to block SMB traffic by stopping TCP ports 139 and 445. This helped me understand how controlling network access can improve security.</p>

<center><h3>Lessons Learned</h3></center>

<p><strong>Firewall Configuration Matters:</strong> Using Windows Firewall with custom rules allows you to control which ports and protocols are allowed. This reduces the system’s exposure to attacks.</p>

<p><strong>Understanding Protocol Risks:</strong> Blocking SMB shows the importance of knowing which protocols are risky, especially outdated ones like SMBv1.</p>

<p><strong>Practical Application:</strong> This task connects theory to real-world security. It shows how system administrators and security engineers protect systems in practice.</p>

<p><strong>Documentation Skills:</strong> Writing clear reports and documenting steps helps explain technical work and builds a strong professional portfolio.</p>

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->
<div style="max-width:500px; margin:0 auto; background:rgba(255,255,255,0.05); padding:12px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ 'assets/reports/REPORT – SMB Protocol Function and Security Risks – v1.1.0.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:8px; color:#aaa; font-size:0.9em;">
<strong>REPORT – SMB Protocol: Function and Security Risks – v1.1.0</strong>
</p>

</div>

</div>

<center><h3>Final Thoughts</h3></center>

<p>Blocking SMB access through Windows Firewall is a small but impactful step in securing a network. This exercise, paired with my report, shows the practical application of cybersecurity concepts, from protocol understanding to defensive implementation. It reflects my commitment to building a strong, hands-on portfolio and developing the skills necessary to protect modern network environments.</p>
