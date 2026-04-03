---
title: "SOP – Securing Folder Access with Permissions – v1.0.1"
date: 2025-08-25
author: Eldon Gabriel
tags: [Windows Security, Access Control, NIST, Cybersecurity]
excerpt: "Implementation of discretionary access controls (DAC) and Group Policy restrictions to secure sensitive data within a Windows environment."
image:
  path: "/assets/images/windowsystem.png"
  thumbnail: "/assets/images/windowsystem.png"
---

# 0.0 Executive Summary
This report documents the implementation of local access permissions and rights to secure a confidential folder on a Windows system. The project successfully demonstrated the creation of structured user groups, the application of the Principle of Least Privilege (POLP) via NTFS permissions, and the enforcement of administrative restrictions through Group Policy Objects (GPOs). By restricting PowerShell access for standard users and isolating sensitive data to authorized groups, the environment achieved alignment with NIST SP 800-53 (AC-6) standards.


# 1.0 Using Access Permissions and Rights to Secure a Folder

## 1.1 Project Description
The objective of this task was to secure a confidential directory by managing local users, groups, and filesystem permissions. The project aimed to prevent unauthorized data access and limit the execution of administrative tools like PowerShell for non-privileged accounts. The environment utilized a Windows-based virtual machine to validate that security controls correctly differentiated between "Finance" personnel, "Standard" users, and "Administrators," ensuring that only designated identities could interact with sensitive organizational assets.
 
## 1.2 Technical Task / Troubleshooting Process
The process involved the manual configuration of identity structures and the subsequent application of security descriptors.

**Key Actions & Observations**
* **Identity Management:** Created localized users and a "Finance" group to establish a role-based access control (RBAC) foundation.

* **Permission Application:** Utilized `icacls` and GUI-based security tabs to strip "Authenticated Users" from the confidential folder and assign "Full Control" exclusively to the Finance group.

* **GPO Enforcement:** Configured Group Policy to disallow the execution of PowerShell for standard users, mitigating the risk of command-line based reconnaissance.

* **Audit and Verification:** Performed cross-account testing to ensure that standard users were successfully denied directory access and tool execution.

**Root Cause:** Overly permissive default settings (such as "Everyone" or "Authenticated Users" having Read access) were identified as the primary risk, resolved through explicit permission inheritance breaks.

## 1.3 Resolution and Validation
Access control was finalized through the validation of group-specific rights and the successful lockout of unauthorized accounts.

| Parameter | Configuration Value |
| :--- | :--- |
| **Control Framework** | NIST 800-53 (AC-6) |
| **Primary Tool** | NTFS Permissions / GPO |
| **Restricted Group** | Finance |
| **Enforcement** | Deny PowerShell (Standard Users) |

**Validation Steps**
1. **Finance Access:** Confirmed the "Finance" user could create, read, and delete files within the confidential directory.
2. **Standard User Lockout:** Verified that non-finance users received "Access Denied" prompts when attempting to enter the folder.
3. **Policy Check:** Successfully blocked PowerShell execution for the standard user, receiving the "This app has been blocked by your system administrator" notification.
 

# 2.0: CONCLUSION

## 2.1 Key Takeaways
* **Implicit Deny:** Security is strongest when default permissions are removed and replaced with explicit, group-based authorizations.

* **Multi-Layered Defense:** Combining NTFS permissions with Group Policy restrictions (like blocking PowerShell) provides a deeper defense than folder security alone.

* **Scalability:** While implemented locally, these principles are directly transferable to Active Directory Domain Services using Domain Groups and GPOs.

## 2.2 Security Implications & Recommendations

**Risk: Privilege Creep** Over time, users may accumulate unnecessary group memberships, granting them access to sensitive data they no longer require.  

**Mitigation:** Conduct regular user and group membership audits to ensure continued alignment with the Principle of Least Privilege.

**Risk: Unauthorized Administrative Action** Standard users with access to PowerShell or Command Prompt can perform internal reconnaissance or attempt to bypass local security.  

**Mitigation:** Enforce strict Group Policy restrictions on administrative tools and enable Windows Security Logs to audit all failed access attempts to sensitive directories.
