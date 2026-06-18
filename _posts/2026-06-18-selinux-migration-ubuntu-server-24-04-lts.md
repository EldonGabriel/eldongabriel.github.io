---
title: "REPORT – SELinux Migration on Ubuntu Server 24.04 LTS – v1.0.0"
date: 2026-06-18
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Linux, Hardening, Security Architecture, Access Control, SELinux, AppArmor]
excerpt: "A technical report on migrating from AppArmor to SELinux on Ubuntu Server 24.04 LTS to enhance system security."
image: 
  path: /assets/images/posts/selinux-migration.png 
  thumbnail: /assets/images/posts/selinux-migration.png
---

# 0.0 Executive Summary

This report details how I migrated an Ubuntu Server 24.04 system from AppArmor to SELinux. The goal was to replace the default AppArmor security module with SELinux to provide stricter control over how processes access files and system resources.

The process involved purging AppArmor, installing SELinux, and configuring the boot process. I followed a step-by-step plan to ensure the server stayed stable while switching over to the new security framework.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 System Hardening

## 1.1 Project Description

The purpose of this project was to harden the Ubuntu Server by switching to a more restrictive security model.

The work included:

* Removing AppArmor services and profiles.
* Installing and enabling the SELinux packages.
* Updating boot settings to load the security framework.
* Triggering a full filesystem relabel.
* Setting the system to Enforcing mode.

This process helps restrict processes to approved resources and reduces the risk of unauthorized access.

## 1.2 Technical Task / Troubleshooting Process

The focus was on swapping security modules without breaking system access.

**Key Actions and Observations**

* Reviewed the current system state and removed AppArmor to prevent software conflicts.
* Installed the SELinux ecosystem and updated the kernel boot configuration.
* Rebuilt the system initialization files and verified that security policies were active.
* During testing, SELinux remained disabled after reboot until the remaining AppArmor packages and profiles were removed from the server.
* After the first reboot, the system relabeled files with SELinux contexts. A second reboot was required before the server reported SELinux as Enforcing.

**Security Consideration:** All AppArmor packages and profiles had to be removed before SELinux could initialize correctly.

## 1.3 Resolution and Validation

The system was tested to confirm that SELinux was properly mediating access.

| Parameter | Configuration Value |
|---|---|
| Assessment Tool | System Management Controls |
| Target Assets | Process Access Control |
| Assessment Type | Security Hardening |
| Operating System | Ubuntu Server 24.04 |
| Security Framework | SELinux |
| Mode | Enforcing |

**Validation Steps**

1. Verified that SELinux was loaded and reporting an active status.
2. Confirmed the system was operating in Enforcing mode with the base policy loaded.
3. Verified that system processes were running with the correct security contexts.
4. Issue Encountered: Initial migration attempt failed because SELinux packages were installed before all AppArmor components were removed.
5. Resolution: Verified remaining packages, purged them from the system, and rebuilt the initial ramdisk.

# 2.0 CONCLUSION

## 2.1 Key Takeaways

* SELinux limits what processes can do, which helps contain a service if it gets compromised.
* A clean system state is required before integrating the security framework.
* Filesystem relabeling is a necessary step that must be validated through a specific reboot cycle.
* SELinux provides more granular access controls and policy enforcement than the default AppArmor configuration used in this environment.

## 2.2 Security Implications and Recommendations

**Risk: Inconsistent Security Contexts**

Incorrect file labeling prevents the system from properly restricting process access.

**Recommendation:** Always trigger a full filesystem relabel when switching security frameworks to ensure every file is indexed correctly.

**Risk: Legacy Module Conflict**

Running multiple security frameworks causes instability and prevents enforcement.

**Recommendation:** Fully purge legacy modules and verify the system state before initializing the new security framework.

**Best Practices**

* Regularly audit system logs to identify blocked actions and verify policy compliance.
* Test security framework transitions in a staged environment before deploying to production.
* Maintain a secure baseline by utilizing kernel-level enforcement for all critical processes.

**Framework Alignment**

* Supports NIST SP 800-53 Access Control and System Integrity requirements.
* Aligns with ISO/IEC 27001:2022 security management and operational security goals.
