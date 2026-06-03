---
title: "REPORT – Password Strength Assessment – v1.0.0"
date: 2026-05-31
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Linux, Hardening, Account Security, Access Control, Security Hardening, System Administration]
excerpt: "Authorized password strength assessment on a Linux system using John the Ripper to identify weak passwords and improve account security."
image:
  path: /assets/images/posts/john.png
  thumbnail: /assets/images/posts/john.png
---

# 0.0 Executive Summary

This report shows the setup and execution of an authorized password strength assessment on a Linux system. The goal was to identify weak passwords that could allow unauthorized access to the system. The assessment focused on a test account named `katy`, which was given admin rights for testing. 

The assessment tested passwords against a known password list to identify weak credentials. Testing confirmed that a weak administrative password could be recovered, showing the risk of weak passwords.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 Password Strength Assessment

## 1.1 Project Description

The goal of this task was to build Linux administration and security auditing skills using John the Ripper and Linux account management tools.

The setup included:

- Combining Linux account information for password testing

- Restricting access to sensitive password files

- Using a common password list for testing

- Running a password strength assessment against a test account

- Securely removing temporary audit files after testing

This process helps administrators find weak passwords before attackers can use them.

## 1.2 Technical Task / Troubleshooting Process

The process focused on reviewing password data and checking password strength.

### Key Actions & Observations

* Created a temporary test account named `katy`.

* Added the account to the sudo group.

* Combined account data from `/etc/passwd` and `/etc/shadow`.

* Isolated the target account for testing.

* Restricted access to audit files.

* Verified that the extracted account data was correct.

* Prepared a password dictionary for testing.

* Ran John the Ripper against the target account.

* Selected the password format manually when automatic detection failed.

* Verified the assessment results.

* Removed temporary audit files using the `shred` utility.

**Root Cause:** John the Ripper could not automatically identify the password format. Setting the correct format manually resolved the issue.

## 1.3 Resolution and Validation

The assessment results were reviewed through testing and tool output verification.

| Parameter | Configuration Value |
|---|---|
| Assessment Tool | John the Ripper |
| Target Account | `katy` |
| Assessment Type | Password Strength Assessment |
| Word List | RockYou |
| Password Format | Manual Configuration |
| File Protection | Secure Data Handling |

**Validation Steps**

1. Verified that account data merged correctly from both system files.

2. Confirmed that file permissions restricted access to authorized users.

3. Tested automatic password format detection and found that it failed.

4. Applied the correct password format and confirmed the assessment completed successfully.

5. Verified that the recovered password matched the test account password.

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Password assessments may require data from multiple Linux account files.

* Modern password protection methods help slow password guessing attacks.

* Manual password format selection may be required when automatic detection fails.

* Temporary password files should be removed after testing to reduce security risks.

## 2.2 Security Implications & Recommendations

**Risk: Weak Administrative Passwords**

Using common passwords on admin accounts increases the risk of unauthorized access.

**Mitigation:** Use PAM policies to enforce strong password length and complexity requirements.

**Risk: Exposed Password Data**

Leaving password files on a system after testing creates unnecessary security risks.

**Mitigation:** Securely remove temporary files when testing is complete.

**Best Practices**

* Back up important data before running password assessments

* Limit testing to approved accounts and systems

* Use manual password format selection when automatic detection fails

* Review authentication logs for unusual activity

**Framework Alignment**

* Supports NIST SP 800-53 access control and security auditing standards

* Aligns with CIS Linux Benchmark recommendations for password strength testing

* Supports ISO 27001 access control and account security requirements
