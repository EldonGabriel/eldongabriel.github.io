---
title: "REPORT – SSH Hardening with Multi-Factor Authentication – v1.0.0"
date: 2026-05-28
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Linux, Hardening, PAM, Access Control, Security Hardening, System Administration]
excerpt: "Technical implementation of SSH multi-factor authentication (MFA), public key authentication enforcement, and user access whitelisting using OpenSSH and PAM."
image:
  path: /assets/images/posts/ssh.png
  thumbnail: /assets/images/posts/ssh.png
---

# 0.0 Executive Summary

This report documents the configuration and validation of multi-factor authentication (MFA) within the OpenSSH daemon and Pluggable Authentication Modules (PAM) architecture on an Ubuntu Linux system. The objective was to improve remote access security by enforcing dual-factor authentication using SSH public keys and a 6-digit TOTP code while completely suppressing standard password prompts.

The result is a hardened SSH configuration that drastically reduces the risk of automated brute-force attacks, unauthorized credential reuse, and unauthorized SSH access.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 SSH Hardening with Multi-Factor Authentication

## 1.1 Project Description

The goal of this task was to develop practical Linux system administration and hardening skills by integrating the OpenSSH daemon configuration with the Linux PAM subsystem.

The implementation included the following aspects:

- Installing and configuring the Google Authenticator PAM shared library (`libpam-google-authenticator`)
- Restricting user authentication strictly to public key and keyboard-interactive authentication
- Implementing rate-limiting and single-use token constraints to mitigate replay and brute-force attacks
- Validating authentication constraints and access control policies through multi-scenario testing

This approach improves administrative access boundaries by centralizing authentication controls and ensuring that access requires multiple independent factors.

## 1.2 Technical Task / Troubleshooting Process

The process focused on strengthening remote authentication policies and validating system enforcement behavior.

**Key Actions & Observations**

* Verified that the `google-authenticator` package was absent from the local package database before performing installation tasks.

* Updated local repository indexes and installed the `libpam-google-authenticator` library on the Ubuntu Server.

* Executed the initialization wizard interactively under the target unprivileged user account (`eldon`) to generate shared secret profiles.

* Configured single-use token restrictions to enforce strict 30-second synchronization boundaries and rate-limited users to a maximum of three attempts per 30 seconds.

* Modified the SSH PAM configuration file at `/etc/pam.d/sshd` to append the `pam_google_authenticator.so` authentication module.

* Commented out the default system authentication routine (`@include common-auth`) within `/etc/pam.d/sshd` to remove the standard user password challenge.

* Updated global configuration parameters within `/etc/ssh/sshd_config` to enforce `UsePAM yes`, `KbdInteractiveAuthentication yes`, and `AuthenticationMethods publickey,keyboard-interactive`.

* Applied user access whitelisting restrictions using the `AllowUsers eldon` directive inside the SSH configuration.

* Restarted the OpenSSH service to apply the updated authentication settings.

* Verified active SSH configuration settings using diagnostic commands to confirm correct configuration loading.

**Root Cause:** Default OpenSSH configurations relied on single-factor authentication schemes or fallback standard system password loops without enforcing multi-factor authentication requirements. This was resolved by implementing centralized PAM-driven MFA policies.

## 1.3 Resolution and Validation

The PAM and SSH configurations were validated through interactive login attempts, unauthorized profile testing, and administrative log reviews.

| Parameter | Configuration Value |
| :--- | :--- |
| **Authentication Framework** | OpenSSH / PAM Integration |
| **Password Policy** | Bypassed / Standard Password Suppressed |
| **Lockout Threshold** | Rate Limited (Max 3 attempts per 30s) |
| **Unlock Timer** | 30-Second Window / Token Expiration |
| **Token Policy** | Single-Use TOTP Enforcement |
| **Scope** | Remote SSH Administration Access Control |

**Validation Steps**

1. Established connection sequences from the Windows client to verify that standard password prompts are missing and replaced by public key passphrase authentication.

2. Simulated cryptographic failures using unconfigured private keys to ensure that direct connections are rejected with explicit permission failures.

3. Attempted direct administrative root access and validated that the connections were immediately dropped at the access boundary.

4. Verified that disabling public key fallback parameters explicitly prevents keyless connections from bypassing the secondary challenge mechanics.

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* OpenSSH requires coordinated adjustments across both the network daemon service (`/etc/ssh/sshd_config`) and local PAM authentication subsystem (`/etc/pam.d/sshd`).

* Using a comma in `AuthenticationMethods` forces each authentication step to succeed in sequence before access is granted.

* Running initialization wizards under administrative contexts instead of standard target contexts creates file ownership permission lockouts.

* MFA token validation depends on accurate system time synchronization.

## 2.2 Security Implications & Recommendations

**Risk: Single-Factor Administrative Authentication**  
Relying solely on credentials or compromised static keys exposes network management access to automated targeting or credential stuffing attacks.

**Mitigation:** Enforce multi-factor authentication requirements directly at the network boundary level of the daemon.

**Risk: Privilege Escalation and Direct Root Targeting**  
Leaving direct root access unmonitored allows attackers to conduct dictionary attacks directly against privileged accounts.

**Mitigation:** Explicitly disable direct root authentication paths and whitelist specific operational identifiers using service control lists.

**Best Practices**

* Backup core server configurations before performing structural adjustments within authentication files

* Maintain active, working SSH test sessions during modifications to avoid accidental administrator lockout

* Verify live running configurations using built-in diagnostic test variables like `sshd -T`

* Audit centralized authentication logs frequently to track unauthorized access indicators or configuration defects

**Framework Alignment**

* Supports NIST SP 800-53 (Access Control and Identification & Authentication)

* Aligns with CIS Linux Benchmarks for password and authentication hardening

* Supports ISO 27001 Annex A access control and credential management requirements
```
