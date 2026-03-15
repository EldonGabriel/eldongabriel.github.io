---
title: "Securing Sensitive Folders: Lessons in Access Rights and Permissions"
date: 2025-08-25
author: Eldon Gabriel
tags: [Windows Security, Access Control, PowerShell, Cybersecurity]
excerpt: "Hands-on lab experience in securing sensitive folders and restricting PowerShell, applying least privilege and defense-in-depth strategies in Windows environments."
image:
  path: "/assets/images/windowsystem.png"
  thumbnail: "/assets/images/windowsystem.png"
---

## <center>Introduction</center>

Today's lab focused on two main goals: locking down sensitive folders and restricting PowerShell. I practiced Windows security controls to prevent unauthorized access. This involved working with accounts, permissions, and group policies. The exercise demonstrated how least privilege and defense-in-depth operate in real Windows environments.

## <center>What I Studied</center>

- **Command-line tools:** `icacls` and `takeown` for managing file permissions.  
- **Local Group Policy Editor:** blocking applications like PowerShell.  
- **User and group management:** creating and modifying accounts in PowerShell, setting password policies, and expirations.  
- **Auditing:** reviewing permissions and access logs to maintain security.  
- **Least privilege:** assigning only the necessary rights to each group.  

## <center>What I Learned</center>

- File permissions control access: knowing a folder path isn’t enough without the correct ACLs.  
- Software restriction policies can stop programs like PowerShell. Misconfigurations, like accidentally blocking Admin, show why testing is critical.  
- There’s a thin line between keeping systems secure and keeping them usable.  
- A structured testing process is essential before applying new restrictions.  

## <center>Why It Matters</center>

- PowerShell is often used in cyberattacks to run malicious scripts. Restricting or monitoring it helps defend against fileless malware and advanced threats.  
- Proper file permissions and group policies protect confidential data and support compliance requirements.  
- Tools like AppLocker and Windows Defender Application Control give administrators more control. Logging PowerShell activity provides visibility and faster response.  

## <center>Reflection & Next Steps</center>

I’ll wait for results and review feedback to identify gaps. In the meantime, I’ll research my next exercise on using access permissions to block unauthorized access to sensitive folders. This builds on the lessons from this lab and sharpens my skills in access control and data security.

For complete configuration and validation details, see the engineering report below:

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;"> 
  <div style="flex: 0 1 45%; min-width: 600px; text-align: center;"> 
    <iframe src="{{ 'assets/guides/GUIDE – Using Access Permissions and Rights to Secure a Folder – v1.0.0.pdf' | relative_url }}" width="100%" height="900px" style="border:1px solid #ccc;"></iframe> 
    <figcaption>GUIDE – Using Access Permissions and Rights to Secure a Folder – v1.0.0.pdf'</figcaption> 
  </div> 
