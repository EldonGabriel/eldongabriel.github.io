---
title: "REPORT – Linux Hardening: PAM Authentication & Account Policy Enforcement – v1.0.0"
date: 2026-05-25
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Linux, Hardening, PAM, Access Control, Security Hardening, System Administration]
excerpt: "Technical implementation of password complexity enforcement, account lockout protection, and local authentication hardening using PAM."
image:
  path: /assets/images/posts/PAM.png
  thumbnail: /assets/images/posts/PAM.png
---

# 0.0 Executive Summary

This report documents the configuration and validation of Pluggable Authentication Modules (PAM) on an Ubuntu Linux system.

The objective was to improve local account security by enforcing password complexity requirements, restricting password reuse, and implementing account lockout protection against repeated failed login attempts.

The result is a hardened authentication configuration that reduces the risk of brute-force attacks, weak credentials, and unauthorized access.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 PAM Authentication & Account Policy Enforcement

## 1.1 Project Description

The goal of this task was to develop practical Linux hardening skills by configuring PAM-based authentication and implementing password security controls.

The implementation included the following:
- Enforcing password complexity requirements using `pam_pwquality`
- Restricting password reuse with `pam_pwhistory`
- Configuring failed-login lockout protection using `pam_faillock`
- Validating authentication behavior through controlled testing

This approach improves local account security by centralizing authentication controls and reducing common credential-related risk.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on strengthening local authentication policies and validating the system enforcement behavior.

**Key Actions & Observations**

* Modified PAM configuration files located in `/etc/pam.d/`.

* Updated `/etc/pam.d/common-password` to enforce password length, complexity, and history restrictions.

* Configured `pam_pwquality` to require uppercase, lowercase, numeric, and special characters.

* Configured `pam_pwhistory` to block the reuse of the previous five passwords.

* Updated `/etc/pam.d/common-auth` to apply account lockouts after repeated failed login attempts.

* Configured a 10-minute automatic unlock timer using `unlock_time=600`.

* Tested weak password submissions and confirmed the system rejected non-compliant passwords.

* Triggered repeated failed logins to validate the account lockout functionality.

* Verified authentication events and lockout counters using PAM auditing tools and the system logs.

**Root Cause:** Default Linux authentication settings allowed weaker password controls and limited protection against repeated failed login attempts. This was resolved by implementing centralized Privileged Access Management (PAM) security policies.

 

## 1.3 Resolution and Validation

The PAM configuration was validated through password testing, failed login simulations, and authentication log reviews.

| Parameter | Configuration Value |
| :--- | :--- |
| **Authentication Framework** | PAM |
| **Password Policy** | Enforced |
| **Lockout Threshold** | 3 Failed Attempts |
| **Unlock Timer** | 10 Minutes |
| **Password History** | Last 5 Passwords |
| **Scope** | Local System Authentication |

**Validation Steps**

1. Weak passwords were configured, and the system was confirmed to reject invalid inputs.

2. Triggered repeated failed login attempts and verified account lockout enforcement after the third attempt.

3. Confirmed password history restrictions block the reuse of recently used credentials.

4. Authentication logs and lockout counters were reviewed to verify active policy enforcement.

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* PAM centralizes Linux authentication and account security management.  
* Strong password policies reduce the success rates of brute-force and dictionary attacks.  
* Account lockout controls help to prevent repeated authentication abuse.  
* Authentication testing should be performed using standard user accounts, instead of root-level sessions.  

 

## 2.2 Security Implications & Recommendations

**Risk: Weak Credential Policies**  
Weak passwords and unrestricted password reuse increase the risk of account compromise.  

**Mitigation:** Enforce strong password requirements and maintain password history restrictions.

**Risk: Brute-Force Attacks**  
Unlimited failed login attempts allow attackers to repeatedly target the user accounts.  

**Mitigation:** Apply account lockout thresholds and automatic unlock timers.

**Best Practices**

* Backup PAM configuration files before making changes  
* Test authentication policies using non-privileged accounts  
* Review authentication logs regularly for abnormal login activity  
* Apply change management procedures before modifying production authentication systems  

**Framework Alignment**

* Supports NIST SP 800-53 (Access Control and Identification & Authentication)  
* Aligns with CIS Linux Benchmarks for password and authentication hardening  
* Supports ISO 27001 Annex A access control and credential management requirements  
