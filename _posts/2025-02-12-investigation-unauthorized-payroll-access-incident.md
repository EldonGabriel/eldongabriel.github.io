---
title: "REPORT – Investigation of Unauthorized Payroll Access Incident – v1.2.0"
date: 2025-02-12
author: Eldon Gabriel
categories: [Identity Security]
tags: [Incident Response, Access Control, Insider Threat, Identity Management]
excerpt: "Investigation into unauthorized access to a payroll system using a former contractor account."
image:
  path: /assets/images/posts/payroll-access.png
  thumbnail: /assets/images/posts/payroll-access.png
---

# 0.0 Executive Summary

This report covers an investigation into unauthorized access to a payroll system using a former contractor account. The goal was to reduce risk by improving identity and access controls and fixing weaknesses in the account offboarding process.

The issue was caused by inactive accounts remaining enabled after termination. This was addressed by enforcing automated account expiration and improving access control policies. As a result, only active and authorized users can now access payroll systems.

 

# 1.0 Investigation of Unauthorized Payroll Access Incident

## 1.1 Project Description

The goal of this task was to improve identity management and prevent access from users who no longer work for the organization.

The investigation used log review and access checks to:
- Identify accounts that were no longer in use but still active  
- Detect unauthorized login attempts  
- Review gaps in the offboarding process  

These steps help protect sensitive systems like payroll from unauthorized access.

 

## 1.2 Technical Task / Troubleshooting Process

This process focused on finding weaknesses in account management and applying controls to prevent unauthorized access.

**Key Actions & Observations**

* Reviewed logs and found that a former contractor account (`j_doe_contractor`) was still active 30 days after termination.  

* Checked authentication logs and identified an unauthorized login attempt from IP address `198.51.100.42`.  

* Configured identity system policies including:  
  - Account expiration rules  
  - Geographic login restrictions (geofencing)  

* Enabled Multi-Factor Authentication (MFA) for payroll access.  

* Set up automatic account deactivation when contracts end.  

* Verified supporting systems:
  - Audit logs for tracking login attempts  
  - HR-to-IT integration for account lifecycle management  

* Documented all changes to support repeatability and audits.  

**Root Cause:** The organization relied on manual offboarding. This caused delays in disabling accounts after termination. The issue was resolved by automating account expiration and enforcing policy-based controls.

 

## 1.3 Resolution and Validation

The new access controls were tested and confirmed to work as expected.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | Identity & Access Management (IAM) |
| **Control State** | Enforced |
| **Security Mode** | Automated Lifecycle Management |
| **Scope** | Contractor and Employee Accounts |

**Validation Steps**

1. Attempted to log in using expired contractor credentials.  

2. Verified the system blocked access and triggered a security alert.  

3. Confirmed active users could still access systems without issues.  

4. Verified failed login attempts were recorded in logs for auditing.  

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Inactive accounts should not remain enabled after employment ends.  
* Automating account expiration reduces human error.  
* Logging and monitoring help detect unauthorized access attempts.  
* Strong identity controls ensure only authorized users can access sensitive systems.  

 

## 2.2 Security Implications & Recommendations

**Risk: Residual Access from Former Users**  
Inactive accounts can still be used if not disabled properly.  

**Mitigation:** Automate account removal through HR and identity system integration.

**Risk: Credential Theft or Reuse**  
Stolen credentials can be used without extra protections.  

**Mitigation:** Require Multi-Factor Authentication (MFA) for all sensitive systems.

**Best Practices**

* Apply least privilege so users only have access they need.  
* Perform regular access reviews to remove unused accounts.  
* Integrate HR systems with identity management tools.  
* Maintain logs for auditing and incident response.  

**Framework Alignment**

* Aligns with NIST SP 800-53 (Account Management)  
* Supports ISO 27001 controls for removal of access after termination  
* Supports the NIST CSF Protect function through improved identity security  
