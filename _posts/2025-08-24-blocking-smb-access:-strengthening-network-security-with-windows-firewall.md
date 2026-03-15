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

<p>As a Security Systems Specialist, I focus on building practical skills that can be directly applied to securing systems. I configured Windows Firewall to create a custom rule blocking Server Message Block (SMB) access, demonstrating how host-based controls can reduce exposure to network-level attacks. This hands-on work ties into my report, which examines SMB’s role in file sharing, its common use cases, and the security challenges it introduces in modern environments.</p>

<center><h3>Foundational Knowledge</h3></center>

<p>The SMB protocol allows computers on a network to share files, printers, and other resources. While SMB facilitates collaboration and resource management in Windows networks, it is a frequent target for cyber attacks, especially older versions like SMBv1. Blocking unnecessary SMB traffic is a key defensive strategy in protecting systems from exploits such as EternalBlue and WannaCry.</p>

<p>During this exercise, I turned on Windows Firewall and created a rule to prevent SMB access to the machine, specifically blocking TCP ports 139 and 445. This hands-on experience reinforced the importance of controlling protocol access and the practical application of network security principles.</p>

<center><h3>Lessons Learned</h3></center>

**Firewall Configuration Matters:** Enabling Windows Firewall and creating custom rules allows precise control over which protocols and ports are accessible, reducing the attack surface.

**Understanding Protocol Risks:** Blocking SMB demonstrates awareness of the vulnerabilities in outdated protocols like SMBv1 and the importance of limiting exposure to public networks.

**Practical Application:** This exercise connected theory from my SMB report to real-world network defense, illustrating how system administrators and security engineers implement protective measures.

**Documentation Skills:** Writing the report and documenting firewall configuration steps helps communicate technical concepts clearly and supports portfolio-building efforts.

<center><h3>Final Thoughts</h3></center>

<p>Blocking SMB access through Windows Firewall is a small but impactful step in securing a network. This exercise, paired with my report, shows the practical application of cybersecurity concepts, from protocol understanding to defensive implementation. It reflects my commitment to building a strong, hands-on portfolio and developing the skills necessary to protect modern network environments.</p>

See my full technical report for detailed configuration and validation steps:

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;"> 
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;"> 
    <iframe src="{{ 'assets/reports/REPORT%20%E2%80%93%20SMB%20Protocol%20Function%20and%20Security%20Risks%20%E2%80%93%20v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe> 
    <figcaption>REPORT – SMB Protocol: Function and Security Risks – v1.0.0</figcaption> 
  </div> 
