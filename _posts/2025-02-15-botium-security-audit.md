---
title: "REPORT – Botium Security Audit – v1.1.0"
date: 2025-02-15
author: Eldon Gabriel
categories: [Security Operations]
tags: [Security Audit, NIST CSF, Compliance, PCI DSS, Risk Management]
excerpt: "Security audit of Botium Toys' systems to find vulnerabilities, check compliance, and improve overall security."
image:
  path: /assets/images/posts/botium-security.png
  thumbnail: /assets/images/posts/botium-security.png
---

# 0.0 Executive Summary

This report describes the security audit of Botium Toys and the steps taken to improve its security controls.

The goal was to reduce risks such as data leaks, compliance violations, and system disruptions by applying stronger security practices based on the NIST Cybersecurity Framework (CSF).

The final result is a stronger security setup. Weak areas such as missing access controls and lack of encryption were identified and improved using structured and trackable security configurations that align with standards like PCI DSS, GDPR, and SOC 2.

---

# 1.0 Botium Security Audit

## 1.1 Project Description

The goal of this task was to set up a stronger security baseline to protect Botium Toys as its digital systems grow.

The NIST CSF was used to guide the process:
- Identify gaps in access control and encryption
- Limit unauthorized access using Role-Based Access Control (RBAC) and stronger password rules
- Improve accountability by defining breach response and disaster recovery procedures

These steps help protect important systems, including customer payment data and internal business operations, from attacks and misuse.

---

## 1.2 Technical Task / Troubleshooting Process

This process focused on finding weaknesses in the current setup and fixing them using structured security controls.

**Key Actions & Observations**

- Reviewed the current system and found that physical security was acceptable, but logical security needed improvement.

Applied controls within the audit scope:
  - Role-Based Access Control (RBAC)
  - Encryption for data at rest and in transit

Improved security by:
  - Enforcing stronger access rules and regular permission reviews
  - Using password management tools
  - Adding intrusion detection and prevention systems (IDS/IPS)
  - Upgrading outdated firewall systems

Verified supporting requirements:
  - PCI DSS and SOC 2 compliance checks
  - Disaster recovery planning and backup validation
- Documented all configurations to support repeat audits and compliance reporting

**Root Cause:** The company’s rapid growth led to gaps in security controls. Some data was not encrypted, and access permissions were too open. This was fixed by applying stricter, policy-based controls focused on protecting data and meeting compliance requirements.

---

## 1.3 Resolution and Validation

The security improvements were applied and then checked to confirm they work as expected.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | NIST CSF / Compliance Audit |
| **Control State** | Enforced |
| **Security Mode** | AES-256 Encryption / RBAC |
| **Scope** | Enterprise Infrastructure and Data |

**Validation Steps**

1. Reviewed the system against PCI DSS Requirement 3 to assess how cardholder data is protected.

2. Confirmed that AES-256 encryption prevents sensitive data from being stored or transmitted in plain text.

3. Verified that system performance and normal operations were not affected while access controls were strengthened.

---

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Security controls must replace insecure default settings to prevent data leaks and compliance issues.
* Using structured access control ensures only authorized users can reach sensitive systems.
* Testing is required to confirm that encryption and access controls are working correctly.
* Security planning should include disaster recovery as part of normal business operations.

---

## 2.2 Security Implications & Recommendations

**Risk: Unauthorized Access to Sensitive Data**  
Weak access control and poor password management can allow attackers or unauthorized users to access data.  

**Mitigation:** Use Role-Based Access Control (RBAC) and centralized password management tools.

**Risk: Regulatory Non-Compliance (PCI DSS/GDPR)**  
Missing encryption and weak response planning can lead to fines and loss of trust.  

**Mitigation:** Encrypt sensitive data using AES-256 and maintain a tested disaster recovery and breach response plan.

**Best Practices**

* Apply least privilege access and review user permissions regularly.
* Use centralized tools to manage encryption keys and monitor system activity.
* Validate security settings after system updates or process changes.
* Keep detailed documentation of all security configurations for audits and reviews.

**Framework Alignment**

* Aligns with NIST CSF for structured security improvements
* Supports PCI DSS for protecting payment card data
* Supports SOC 2 for maintaining operational reliability and security
* Strengthens Identify and Protect functions by addressing key control gaps
