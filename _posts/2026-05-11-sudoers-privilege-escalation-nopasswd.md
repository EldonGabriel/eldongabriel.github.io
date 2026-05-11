---
title: "SUMMARY – Sudoers Privilege Escalation and NOPASSWD Implementation – v1.0.0"
date: 2026-05-11
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Linux, Sudoers, Privilege Management, Security Hardening, Access Control]
excerpt: "Technical implementation of granular privilege escalation and passwordless execution within the Linux sudoers framework."
image:
  path: /assets/images/posts/sudoers.png
  thumbnail: /assets/images/posts/sudoers.png
---

# 0.0 Executive Summary

This report documents the implementation and analysis of granular privilege escalation using the `sudoers` framework in an Ubuntu Server environment. The objective was to configure specific user privileges that allowed cross-user script execution without password prompts. This project focused on utilizing the `NOPASSWD` directive to enable automation while maintaining the Principle of Least Privilege (PoLP).

The result was a validated, noninteractive execution path, where a restricted user could execute a specific script as another target user. This reduces the need for manual authentication and restricts execution to a controlled command path.

 <hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

# 1.0 Sudoers Privilege Escalation

## 1.1 Project Description

The goal of this task was to develop proficiency in managing advanced Linux permissions and automating cross-user tasks without compromising the system security.

The implementation utilized the `/etc/sudoers` configuration to

* Define specific execution rights for individual users
* Implement passwordless execution for targeted binaries and scripts
* Enforce cross-user context switching (e.g., user1 executing as user2)
* Validate security enforcement through non-interactive command testing

This workflow demonstrates how system administrators can enable secure automated processes by scoping elevated privileges to specific verified scripts.

 <hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

## 1.2 Technical Task / Troubleshooting Process

The process focused on utilizing the `visudo` utility to modify the system's authorization policy with precise syntax.

### Key Actions and Observations

* **User and Resource Preparation**
    * Created two restricted accounts (`user1` and `user2`) to test privilege boundaries
    * Developed a shell script (`/usr/local/bin/hello.sh`) owned by the target user
    * Applied restricted permissions (`700`) to ensure only authorized execution

<hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

* **Sudoers Policy Implementation**
    * Used `sudo visudo` to safely edit the configuration with syntax validation
    * Added a scoped rule: `user1 ALL=(user2) NOPASSWD: /usr/local/bin/hello.sh`
    * Enabled `user1` to execute the script as `user2` without a password

<hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

* **Privilege Validation**
    * Executed: `sudo -u user2 /usr/local/bin/hello.sh`
    * Used `whoami` within the script to confirm execution context as `user2`

  <hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

### Troubleshooting Highlights

* **Syntax Sensitivity**
    * Identified that `sudoers` rules are highly sensitive to formatting and order
    * Prevented misconfiguration by using `visudo`, which blocks invalid syntax

* **Permission Denied Errors**
    * Encountered execution failures due to strict file permissions (`700`)
    * Resolved by ensuring correct user context (`-u user2`) matched the defined policy

  <hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

## 1.3 Resolution and Validation

The configuration was validated by testing the noninteractive execution path and verifying the identity context.

| Parameter | Configuration Value |
| --- | --- |
| **Primary Tool** | Sudoers Framework (`visudo`) |
| **Privilege Type** | NOPASSWD Implementation |
| **Execution Path** | /usr/local/bin/hello.sh |
| **Scope** | Controlled Cross-User Execution |

### Validation Steps

1. **Passwordless Verification**
   * Confirmed that `user1` could execute the script without a password prompt

2. **Context Verification**
   * Verified execution context using `whoami`, confirming execution as `user2`

3. **Policy Scope Proof**
   * Attempted to run other commands using `sudo`
   * Confirmed that access was denied or required a password

4. **Negative Testing**
   * Verified that unauthorized commands outside the defined rule were not permitted

 <hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;"> 

# 2.0 CONCLUSION

## 2.1 Key Takeaways

* **Granular Control:** The `sudoers` file enables precise control over command execution and user context
* **Automation Support:** `NOPASSWD` allows non-interactive execution for scripts and services
* **Configuration Safety:** `visudo` prevents syntax errors that can break administrative access
* **Least Privilege:** Restricting access to specific scripts reduces the attack surface

 

## 2.2 Security Implications and Recommendations

### Risk: Script Modification (Privilege Escalation)

If a script defined in the `sudoers` file is modified by unauthorized users, it can be used to execute malicious commands with elevated privileges.

**Mitigation**

* Enforce strict ownership (`root` or target user)
* Apply secure permissions (`700` or `755`)
* Store scripts in protected directories such as `/usr/local/bin`

 

### Risk: Stale Privilege Entries

Unused or outdated `NOPASSWD` rules may create hidden access paths.

**Mitigation**

* Regularly audit `/etc/sudoers` and `/etc/sudoers.d/`
* Remove entries tied to unused users or deprecated scripts

 

### Best Practices

* Always use `visudo` for editing privilege configurations
* Define rules using absolute paths to prevent abuse
* Limit `NOPASSWD` usage to only required commands
* Combine privilege rules with strict filesystem permissions
* Document all changes for auditing and compliance tracking

 

### Framework Alignment

* **NIST SP 800-53 (AC-6):** Enforcement of Least Privilege
* **CIS Control 5:** Account and privilege management
* **PCI-DSS / SOC 2:** Controlled and auditable access mechanisms
