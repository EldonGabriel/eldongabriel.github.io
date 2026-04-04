---
title: "REPORT – Endpoint Security with Windows Registry – v1.0.0"
date: 2025-08-30
author: Eldon Gabriel
categories: [Security Operations]
tags: [Windows, Registry, Endpoint Security, Hardening, System Administration]
excerpt: "Implementation of registry-level restrictions to disallow unauthorized executable runs and harden the Windows OS against common user-mode threats."
image:
  path: "/assets/images/registry.png"
  thumbnail: "/assets/images/registry.png"
---
 
# 0.0 Executive Summary

This report explains how system-level restrictions were applied using the Windows Registry on a standalone workstation.

The main goal was to reduce the risk of malware execution and unauthorized system changes. This was done by applying security controls through changes to registry keys and values.

The final result improved system security by replacing the default behavior, where users can run any program, with controlled settings that block unauthorized or risky executables.

---

# 1.0 Endpoint Security with Windows Registry

## 1.1 Project Description

The goal of this task was to apply endpoint security controls using the Windows Registry.

The purpose was to prevent unauthorized users from running unwanted programs and accessing sensitive system tools.

The Registry Editor was used to:
- Block specific executables from running  
- Limit access to system management tools  
- Document key registry paths and value types used for control  

These controls help protect systems from misuse, especially on standalone machines that are not managed by a domain controller.

---

## 1.2 Technical Task / Troubleshooting Process

The process focused on reviewing default system behavior and applying restrictions at the registry level.

### Key Actions & Observations
- Reviewed default system behavior and identified that any user can run executable files  
- Used the Registry Editor (regedit.exe) to apply changes  

- Configured the following registry paths:
  - HKEY_CURRENT_USER (HKCU)  
  - HKEY_LOCAL_MACHINE (HKLM)  

- Applied restrictions by:
  - Creating a `DisallowRun` key under the Explorer path  
  - Adding a list of blocked executable files  

- Verified related components:
  - Registry Editor functionality  
  - User profile behavior and settings  

- Documented all changes for repeatable system hardening  

**Root Cause:**  
By default, Windows allows users to run most programs without restriction. This can expose the system to misuse or malware. The issue was resolved by applying registry-based restrictions that block specific executables from running.

 
## 1.3 Resolution and Validation

The system was secured by applying and testing the registry-based restrictions.

| Parameter | Configuration Value |
| :--- | :--- |
| Management Tool | regedit.exe |
| Control State | Enforced |
| Security Mode | DisallowRun Restrictions |
| Scope | User Profiles |

### Validation Steps

1. Attempted to run a restricted program such as `cmd.exe` or a blocked installer  

2. Verified that the system blocked the execution and displayed a warning message  

3. Confirmed that allowed applications still worked normally  

4. Checked system stability after applying the registry changes  

5. Ensured no unintended issues were introduced by the restrictions  

 

# 2.0 CONCLUSION

## 2.1 Key Takeaways

- Default Windows settings allow users to run most applications without restriction  
- Registry-based controls can block specific executables from running  
- Testing is required to confirm that restrictions are working as expected  
- Care must be taken to avoid blocking important system or business applications  

 

## 2.2 Security Implications and Recommendations

**Risk: Running Malicious Tools**  
Attackers or untrusted users may run built-in tools to perform harmful actions or hide activity.

**Mitigation:**  
Use registry restrictions such as `DisallowRun` to block known risky executables.

**Risk: Unauthorized System Changes**  
Users with access to system tools may modify settings and weaken security.

**Mitigation:**  
Restrict access to tools like Control Panel and Registry Editor using Group Policy or registry controls.

### Best Practices

- Apply least privilege so users only have the access they need  
- Use Group Policy for centralized control in enterprise environments  
- Test changes to ensure legitimate applications are not blocked  
- Document all registry changes for troubleshooting and audits  

### Framework Alignment

- Supports endpoint hardening best practices such as CIS Control 4  
- Aligns with NIST guidance for secure configuration and access control  
- Supports the Protect function of the NIST Cybersecurity Framework by limiting unauthorized execution of applications  
