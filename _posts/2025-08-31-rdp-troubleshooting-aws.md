---
title: "RDP Troubleshooting for AWS Users"
date: 2025-08-31
author: Eldon Gabriel
tags: [Windows, RDP, AWS, Cybersecurity]
excerpt: "A hands-on guide to troubleshooting Remote Desktop access for new user accounts on AWS-hosted Windows 10 VMs."
image:
  path: "/assets/images/rdp.png"
  thumbnail: "/assets/images/rdp.png"
---

Following up on my work with registry restrictions for untrusted accounts, I encountered another aspect of endpoint security: ensuring remote access works correctly for new Windows user accounts on cloud-hosted VMs. While registry keys help enforce application restrictions, users still need proper RDP access to perform their tasks safely.  

When I first attempted to switch users on an AWS-hosted Windows 10 VM, I noticed that the system didn’t allow seamless local account switching. Signing out of the Administrator caused the VM to shut down, and the new account didn’t appear in the Start Menu sign-in options. This behavior is typical for certain AWS Windows 10 AMIs, which automatically configure a dedicated account for RDP sessions. To resolve this, I created a new RDP connection profile for the untrusted account, enabling the VM to recognize it remotely without altering the default session.  

With the RDP profile configured, I verified the account could log in by running `whoami` and checking its group memberships. I also added the user to the Remote Desktop Users group both through the GUI and via the command line with:  

```
net localgroup "Remote Desktop Users" Eldon /add
```

Completing this exercise highlighted the importance of understanding how remote access is managed in virtualized environments. It reinforced the practical steps needed to configure secure RDP access, verify user permissions, and troubleshoot unexpected behaviors unique to cloud-hosted VMs.  

By ensuring that only authorized accounts can log in via RDP, and by combining this with proper group membership and firewall validation, I strengthened the VM’s operational security posture. This hands-on experience complements my previous work with registry restrictions, showing how layered controls—both endpoint and remote access—can reduce attack surfaces and enforce the principle of least privilege.  


 <div style="text-align:center;">
  <h1 style="display: inline-block; border-bottom: 3px solid #fff; padding-bottom: 5px;">Related Projects</h1>

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;">
    <iframe src="{{ '/assets/guides/GUIDE – RDP Troubleshooting for AWS Users – v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe>
    <figcaption>GUIDE – RDP Troubleshooting – AWS VM Access – v1.0.0</figcaption>
  </div>
