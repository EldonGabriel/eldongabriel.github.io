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

This report documents the configuration and validation of multi-factor authentication (MFA) within the OpenSSH daemon and Pluggable Authentication Modules (PAM) architecture on an Ubuntu Linux system. The objective was to improve remote access security by enforcing dual-factor authentication using SSH public keys and 6-digit TOTP verification codes while suppressing standard password-based authentication.

The implementation combined OpenSSH configuration hardening with PAM-based MFA integration, user access restrictions, and authentication rate limiting. The result is a hardened SSH configuration that reduces the risk of brute-force attacks, credential reuse, and unauthorized remote access.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 SSH Hardening with Multi-Factor Authentication

## 1.1 Project Description

The goal of this task was to develop practical Linux hardening and remote-access security skills by integrating the OpenSSH daemon with the Linux PAM authentication framework.

The implementation included the following:

- Installing and configuring the Google Authenticator PAM module (`libpam-google-authenticator`)
- Enforcing public key and keyboard-interactive authentication
- Restricting direct access to approved user accounts
- Implementing MFA rate-limiting protections
- Validating authentication enforcement through controlled testing

This approach improves administrative access security by requiring multiple independent authentication factors before SSH access is granted.

## 1.2 Technical Task / Troubleshooting Process

The process focused on strengthening remote authentication policies and validating system enforcement behavior.

**Key Actions & Observations**

* Verified that the Google Authenticator PAM package was not installed before beginning the deployment process.

* Updated repository indexes and installed the `libpam-google-authenticator` package on the Ubuntu Server.

* Executed the MFA initialization wizard under the target standard user account (`eldon`) to generate secure TOTP secret profiles.

* Configured single-use token enforcement and rate limiting to reduce replay and brute-force attack attempts.

* Updated `/etc/pam.d/sshd` to integrate the `pam_google_authenticator.so` module into the SSH authentication workflow.

* Disabled the default password-authentication routine to remove standard password prompts from SSH login sequences.

* Updated `/etc/ssh/sshd_config` to enforce:
  - `UsePAM yes`
  - `KbdInteractiveAuthentication yes`
  - `AuthenticationMethods publickey,keyboard-interactive`

* Applied SSH user-access restrictions using the `AllowUsers eldon` directive.

* Restarted the OpenSSH daemon to apply the updated security configurations.

* Verified active runtime settings using SSH diagnostic validation commands.

**Root Cause:** Default OpenSSH configurations relied primarily on single-factor authentication methods and standard password authentication. This increased the risk of credential-based attacks and unauthorized remote access. The issue was mitigated by implementing centralized PAM-driven multi-factor authentication policies.

## 1.3 Resolution and Validation

The SSH and PAM configurations were validated through authentication testing, unauthorized access simulations, and configuration verification.

| Parameter | Configuration Value |
| :--- | :--- |
| **Authentication Framework** | OpenSSH / PAM Integration |
| **Authentication Mode** | Public Key + TOTP MFA |
| **Password Authentication** | Disabled |
| **Rate Limiting** | Max 3 Attempts per 30 Seconds |
| **Token Enforcement** | Single-Use TOTP Validation |
| **Scope** | Remote SSH Administrative Access |

**Validation Steps**

1. Verified that standard password prompts were suppressed during SSH login attempts.

2. Confirmed that valid SSH key authentication was required before MFA prompts were presented.

3. Simulated invalid private-key authentication attempts and confirmed immediate connection rejection.

4. Attempted unauthorized root access and verified that connections were denied.

5. Confirmed that disabling public key authentication prevented access to the MFA prompt stage.

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* OpenSSH MFA deployments require coordinated configuration across both the SSH daemon and PAM authentication framework.

* Combining public key authentication with TOTP verification significantly strengthens remote administrative access security.

* SSH authentication enforcement should be validated using standard user contexts instead of administrative override sessions.

* Time synchronization is critical for reliable TOTP validation and MFA stability.

## 2.2 Security Implications & Recommendations

**Risk: Single-Factor Administrative Authentication**

Relying solely on passwords or standalone SSH keys increases exposure to credential theft and unauthorized remote access attempts.

**Mitigation:** Enforce multi-factor authentication directly within the SSH authentication workflow.

**Risk: Unauthorized Administrative Access**

Unrestricted SSH access increases the risk of brute-force attacks and direct privileged-account targeting.

**Mitigation:** Restrict SSH access to approved users and disable direct root authentication.

**Best Practices**

* Backup SSH and PAM configuration files before implementing authentication changes

* Maintain active SSH sessions during configuration updates to prevent accidental administrative lockout

* Validate live SSH configurations using diagnostic commands such as `sshd -T`

* Review authentication logs regularly to identify unauthorized access attempts or configuration issues

**Framework Alignment**

* Supports NIST SP 800-53 (Access Control and Identification & Authentication)

* Aligns with CIS Linux Benchmarks for SSH and authentication hardening

* Supports ISO 27001 Annex A access control and credential management requirements
