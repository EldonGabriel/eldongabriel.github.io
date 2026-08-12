---
title: "REPORT – Domain Group Policy Object (GPO) Deployment – v1.0.0"
date: 2026-08-11
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Windows Server, Active Directory, Group Policy, Security, Hardening]
excerpt: "Deployment and validation of a centralized Group Policy Object to secure the built-in Guest account status across domain-joined Windows assets."
image:
  path: /assets/images/posts/gpo-deployment.png
  thumbnail: /assets/images/posts/gpo-deployment.png
---

# Executive Summary

This report documents the deployment of a new Group Policy Object (GPO) within an Active Directory environment. The project focused on applying a centralized security configuration to domain-joined Windows workstations.

A dedicated GPO handled the security configuration instead of the Default Domain Policy. This approach isolates the security setting. It simplifies policy management. It reduces the risk of unintended changes to broader domain settings.

The GPO configured the **Accounts: Guest account status** setting as **Disabled**. The configuration applied to the targeted domain scope.

Testing confirmed successful policy application on both target workstations. Both workstations listed **Disable Guest Account** under **Applied Group Policy Objects**. Both workstations showed **Disabled** for the **Accounts: Guest account status** setting.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 Domain GPO Deployment

## 1.1 Project Description

The project established a standard security control for Windows workstations. The control applies within the Active Directory domain environment.
The project involved:

- Creating a dedicated GPO for the security configuration.
- Configuring the **Accounts: Guest account** status setting as Disabled.
- Linking the GPO to the Active Directory domain.
- Testing both workstations for successful policy application.

The GPO provides centralized management of the security configuration. The configuration applies to domain-joined computers within the configured GPO scope.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

## 1.2 Technical Task / Troubleshooting Process

The deployment followed a structured process. The process covered GPO creation, configuration, linking, and verification.

**Key Actions and Observations**

- Opened the Group Policy Management console (`gpmc.msc`) on the Domain Controller (`WS2016-DC02`).
- Created the **Disable Guest Account** GPO under the `corp.local` domain.
- Navigated to:
```text
Computer Configuration
 └── Policies
       └── Windows Settings
            └── Security Settings
                 └── Local Policies
                      └── Security Options
```
- Selected **Accounts: Guest account** status.
- Defined the policy setting as **Disabled**.
- Linked the GPO to the root of the `corp.local` domain.
- Ran `gpupdate /force` on the target workstations.
- Verified GPO application with `gpresult /r`.
- Verified the security setting with `secpol.msc`.

**Security Considerations**

The dedicated GPO separates the security configuration from the Default Domain Policy. This approach reduces the risk of unintended changes to the Default Domain Policy.

Disabling the built-in Guest account removes an unnecessary local access path.

 <hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

## 1.3 Resolution and Validation

Testing confirmed successful GPO application on both target workstations.

| Parameter | Configuration Value |
|---|---|
| **Management Tool** | Group Policy Management Console |
| **Domain Controller** | WS2016-DC02 |
| **Operating System** | Windows Server 2016 / Windows 10 |
| **Active Directory Domain** | corp.local |
| **Target Security Control** | Accounts: Guest account status = Disabled |
| **Key Change** | Dedicated GPO Creation, Linking, and Enforcement |
| **Validated Workstations** | WS-10-01, WS-10-02 |

**Validation Steps**

1. Confirmed **Enabled** under the GPO link status in Group Policy Management.
2. Ran `gpupdate /force` on both target workstations.
3. Ran `gpresult /r` on both workstations.
4. Verified that **Disable Guest Account** appeared under Applied Group Policy Objects on both workstations.
5. Opened `secpol.msc` on both workstations.
6. Confirmed that **Accounts: Guest account** status showed **Disabled** on both workstations.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">
 
# 2.0 CONCLUSION

## 2.1 Key Takeaways

- Dedicated GPOs isolate security configurations from the Default Domain Policy.
- Centralized Group Policy reduces the need for manual configuration on individual computers.
- `gpresult` confirms GPO application on target workstations.
- Local Security Policy confirms the resulting security configuration.

 <hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

## 2.2 Security Implications and Recommendations

**Risk: Unmonitored Local Accounts**

Built-in accounts can create unnecessary access paths.

**Recommendation:** 

Disable unused built-in accounts. Review local settings against organizational security baselines.

**Best Practices**

- Use dedicated GPOs for specific security configurations.
- Avoid modifying the Default Domain Policy for individual security settings.
- Test GPO changes on target workstations before broader deployment.
- Maintain clear documentation of GPO configurations and links.
- Verify both GPO application and the resulting security configuration.
