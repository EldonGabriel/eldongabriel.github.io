---
title: "Using the Windows Registry to Restrict Untrusted User Accounts"
date: 2025-08-30
author: Eldon Gabriel
tags: [cybersecurity, windows, registry, endpoint-security]
excerpt: "Hands-on exercise in securing Windows endpoints by restricting untrusted user accounts via the DisallowRun registry key."
image: "/assets/images/fnlogo.png"
---

# Using the Windows Registry to Restrict Untrusted User Accounts

I recently worked on the MSAF exercise **“Use the Windows Registry To Restrict The Permissions Of Untrusted User Accounts.”** The goal was to prevent regular user accounts from running critical Windows utilities that could be misused in Living-off-the-Land (LOTL) attacks.

To prepare, I researched the Windows Registry in **_Windows Internals, 7th Edition_**, Chapter 10 on Management, Diagnostics, and Tracing. This gave me a solid understanding of registry hives, keys, and values, and how the registry is loaded into RAM at system startup. Registry keys act like folders, while values store actual configuration data. I learned the importance of critical keys like **SAM** and **HKEY_LOCAL_MACHINE**, and how to create restore points and back up the registry safely.

When performing the exercise, I ran into an issue switching from an administrator to a standard user account on my AWS cloud machine. Unlike other virtual machines, it didn’t allow seamless user switching. To resolve this, I configured **Remote Desktop access** for the untrusted account. I went through the system settings by typing `sysdm.cpl` in the Start Menu, enabling remote connections, enforcing Network Level Authentication, and adding the user to the Remote Desktop Users group. Once this was complete, I verified that the account could log in successfully.

After setting up the user account, I edited the registry to add the **DisallowRun key**. I created string values for the programs I wanted to block and verified that the restricted user could not execute them. This hands-on process reinforced the practical applications of registry restrictions, combined with Group Policy enforcement and endpoint monitoring, to reduce attack surfaces and enforce the principle of least privilege.

Completing this exercise helped me understand not only the structure and functions of the Windows Registry but also the operational steps needed to secure endpoints in a real-world environment. By controlling what untrusted users can access, I reduced potential avenues for LOTL attacks and strengthened overall system security.

<p align="center">
  <a href="https://github.com/EldonGabriel/eldongabriel.github.io/blob/main/assets/guides/GUIDE%20%E2%80%93%20Endpoint%20Security%20with%20the%20Windows%20Registry%20%E2%80%93%20v1.0.0.pdf" target="_blank">
    VIEW: GUIDE – Endpoint Security with the Windows Registry – v1.0.0
  </a>
</p>
