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

This report shows the setup and testing of multi-factor authentication (MFA) for SSH on an Ubuntu Linux system.

The goal was to make remote logins more secure by requiring two login steps:

- an SSH key

- a 6-digit TOTP code

Normal password logins were disabled.

The setup used OpenSSH and PAM to control login access and reduce the risk of brute-force attacks and unauthorized access.

Testing confirmed that users needed both a valid SSH key and a valid TOTP code before the system allowed access.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 SSH Hardening with Multi-Factor Authentication

## 1.1 Project Description

The goal of this task was to build Linux hardening and SSH security skills using OpenSSH and PAM.

The setup included:

- Installing the Google Authenticator PAM module (`libpam-google-authenticator`)

- Requiring SSH public key authentication

- Requiring TOTP verification codes

- Restricting SSH access to approved users

- Testing login security with different login scenarios

This setup improves SSH security by requiring two separate login factors before access is granted.

## 1.2 Technical Task / Troubleshooting Process

The process focused on improving SSH login security and testing the new settings.

Key Actions & Observations

* Checked that the Google Authenticator package was not already installed.

* The `libpam-google-authenticator` package was installed on the Ubuntu Server.

* Ran the MFA setup wizard under the standard user account (`eldon`).

* Enabled single-use TOTP codes and basic rate limiting.

* Modified `/etc/pam.d/sshd` to load the `pam_google_authenticator.so` module.

* Disabled normal password prompts inside the SSH PAM configuration.

* Updated `/etc/ssh/sshd_config` with the following settings

  - `UsePAM yes`

  - `KbdInteractiveAuthentication yes`

  - `AuthenticationMethods publickey,keyboard-interactive`

* Restricted SSH access using:

  - `AllowUsers eldon`

* The SSH service was restarted to apply the new settings.

* Verified the SSH configuration using the built-in test commands.

Root Cause: Default SSH settings allowed single-factor logins using standard passwords. This increases the risk of unauthorized access. This issue was resolved by enabling PAM-based MFA.

## 1.3 Resolution and Validation

SSH and PAM settings were tested through login attempts and configuration checks.

| Parameter | Configuration Value |
|---|---|
| Authentication System | OpenSSH / PAM |
| Login Method | SSH Key + TOTP |
| Password Login | Disabled |
| Rate Limit | 3 Attempts per 30 Seconds |
| Token Protection | Single-Use TOTP |
| Scope | Remote SSH Access |

**Validation Steps**

1. Verified that password prompts no longer appeared during SSH login attempts.

2. It was confirmed that valid SSH keys were required before the MFA prompt appeared.

3. Tested invalid SSH keys and confirmed that access had been denied.

4. Attempted direct root SSH access and confirmed that the connection was blocked.

5. It was verified that disabling public key authentication prevented access to the MFA prompt.

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* SSH MFA requires changes to both the SSH service and PAM configuration files.

* SSH keys combined with TOTP codes improve the security of remote logins.

* MFA testing should be performed using standard user accounts instead of root sessions.

* The correct system time is important for TOTP authentication to function properly.

## 2.2 Security Implications & Recommendations

**Risk: Single-Factor SSH Login**

Using only passwords or SSH keys increases the risk of unauthorized access if the credentials are stolen.

**Mitigation:** Require MFA for all remote SSH logins.

**Risk: Unauthorized SSH Access**

Open SSH access increases the exposure to brute-force attacks and login abuse.

**Mitigation:** Restrict SSH access to approved users and disable direct root logins.

**Best Practices**

* Backup SSH and PAM files before making changes

* Keep an active SSH session open during testing

* Test SSH settings using commands like `sshd -T`

* Review SSH logs for suspicious login attempts

**Framework Alignment**

* Supports NIST SP 800-53 access control requirements

* Aligns with CIS Linux Benchmark recommendations

* Supports ISO 27001 access control guidance
