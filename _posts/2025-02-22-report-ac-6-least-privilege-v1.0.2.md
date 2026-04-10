---
title: "REPORT– AC-6 Least Privilege (NIST SP 800-53) – v1.0.2"
date: 2025-02-22
author: Eldon Gabriel
categories: [GRC]
tags: [Compliance, NIST SP 800-53, Access Control, Security Hardening, Identity Management]
excerpt: "Implementation of least privilege controls to reduce risk and limit unauthorized access in enterprise systems."
image:
  path: "/assets/images/posts/ac-6.png"
  thumbnail: "/assets/images/posts/ac-6.png"
---

# 0.0 Executive Summary

This report explains how the Principle of Least Privilege (PoLP) was applied using the NIST SP 800-53 AC-6 control.

The goal was to reduce risks such as unauthorized access, data breaches, and insider threats by limiting user permissions.

The final result improved security by removing excessive access and enforcing controlled, monitored permissions across systems.

 

# 1.0 Security Control Standard: AC-6 Least Privilege (NIST SP 800-53)

## 1.1 Project Description

The goal of this task was to ensure users and systems only have access to what they need to do their job.

This was done by applying the least privilege model using:

- Role-Based Access Control (RBAC)  
- Privileged Access Management (PAM)  
- Access monitoring and review processes  

These controls reduce the impact of compromised accounts and prevent misuse of system access.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on finding and removing unnecessary access rights.

### Key Actions & Observations

- Reviewed user accounts and found excessive or unused permissions  

Configured access control systems:

  - RBAC for role-based permissions  
  - PAM for managing privileged accounts  

Applied security controls by:

  - Enforcing Multi-Factor Authentication (MFA) for admin access  
  - Using Just-In-Time (JIT) access for sensitive tasks  

Verified supporting components:

  - Audit logs and access tracking  
  - Separation of Duties (SoD) controls  

- Documented all changes for audits and future reviews  

**Root Cause:**  

Default systems often give more access than needed to avoid breaking workflows. This creates security risks. The issue was fixed by enforcing strict access controls based on job roles.

 

## 1.3 Resolution and Validation

Access controls were tested to confirm they were working correctly.

| Parameter | Configuration Value |

| :--- | :--- |

| Management Tool | RBAC / PAM Systems |

| Control State | Enforced |

| Security Mode | Least Privilege |

| Scope | Users and Applications |

### Validation Steps

1. Attempted an admin action from a standard user account  

2. Verified the system blocked the action  

3. Confirmed the attempt was logged  

4. Tested normal user tasks to ensure no disruption  

5. Verified proper access based on assigned roles  

 

# 2.0 Conclusion

## 2.1 Key Takeaways

- Least privilege reduces the risk of unauthorized access  

- Excess permissions increase attack surface  

- RBAC and PAM help manage access effectively  

- MFA adds an extra layer of protection  

- Regular reviews prevent permission creep  

-- -

## 2.2 Security Implications and Recommendations

**Risk: Unauthorized Access**  
Users with too many permissions can access sensitive data.  

**Mitigation:**
Review and remove unnecessary access regularly.

**Risk: Privilege Escalation**
Attackers can use admin rights to take control of systems.  

**Mitigation:**
Use JIT access and require MFA for all privileged actions.

### Best Practices

- Apply least privilege across all systems  

- Monitor and review access logs regularly  

- Use centralized tools for access control  

- Re-check permissions after system changes  

- Document all access policies for compliance  

### Framework Alignment

- Supports NIST SP 800-53 (AC-6)  

- Aligns with ISO 27001 access control requirements  

- Supports the NIST Cybersecurity Framework (Protect function) by limiting access risks  
