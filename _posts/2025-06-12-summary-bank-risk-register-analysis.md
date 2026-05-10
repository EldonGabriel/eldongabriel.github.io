---
title: SUMMARY – Governance, Risk & Compliance: Bank Risk Register Analysis – v1.0.2
date: 2025-06-12
author: Eldon Gabriel
categories: [GRC]
tags: [Risk Management, Banking Security, Compliance, Threat Assessment, Financial Services]
excerpt: "Analysis of operational and technical risks for a coastal financial institution, prioritizing threats to customer data and business continuity."
image:
  path: /assets/images/posts/bank-risk.png
  thumbnail: /assets/images/posts/bank-risk.png
---

# 0.0 Executive Summary

This report presents a risk register assessment for a coastal financial institution. The objective was to identify, evaluate, and prioritize operational and technical risks affecting critical systems and customer data.

A structured risk matrix was used to assess threats such as Business Email Compromise (BEC), unauthorized access, and exposed backup systems. Each risk was scored based on likelihood and impact to determine priority levels.

The outcome is an improved and more controlled risk management process. High-risk issues, including unencrypted customer data and insecure backups, were identified and prioritized for remediation. This strengthens overall security posture, supports compliance requirements, and reduces the likelihood of data breaches and financial loss.

# 1.0 Bank Risk Register Analysis

## 1.1 Project Description

The objective of this task was to implement a centralized Risk Register to improve visibility and control over security risks within the organization.

A risk scoring model was used to:

- Identify threats that could impact banking operations  
- Rank risks based on likelihood and impact  
- Prioritize remediation efforts based on business importance  

The scope included both on-premise systems and remote users. This ensured that risks affecting internal networks, remote access, and customer data were properly assessed and recorded.

## 1.2 Technical Task / Troubleshooting Process

The system environment was reviewed to identify weaknesses in default configurations and gaps in existing security controls.

**Key Actions & Observations**

* **Action 1:** Reviewed system setup and identified gaps in data protection and backup security  
* **Observation:** Some systems relied on default configurations with limited security hardening  

* **Action 2:** Identified and categorized threats including Business Email Compromise (BEC), physical access threats, and database compromise  
* **Observation:** Multiple attack vectors existed across email, access control, and data storage layers  

* **Action 3:** Evaluated environment scope consisting of 100 on-premise users and 20 remote users  
* **Observation:** Remote access increased the attack surface and required additional controls  

* **Action 4:** Reviewed email security controls such as SPF, DKIM, and DMARC  
* **Observation:** Email authentication controls were either partially implemented or required validation  

* **Action 5:** Assessed encryption of customer data and security of backup systems  
* **Observation:** Some backups were exposed or not properly secured  

**Control Review**

- Email security protections (SPF, DKIM, DMARC) were evaluated  
- Encryption of sensitive customer data was verified  
- Access controls for both local and remote users were reviewed  
- Backup systems were checked for exposure and improper configuration  

**Root Cause:**  
The primary issue was reliance on default system configurations. These configurations typically prioritize availability over security, resulting in weak encryption, excessive permissions, and insufficient access restrictions. This was addressed by implementing stricter, policy-driven controls and focusing on high-risk areas identified in the Risk Register.

## 1.3 Resolution and Validation

Security controls were implemented based on prioritized risk scores from the Risk Register.

| Parameter | Configuration Value |
| :--- | :--- |
| Management Tool | Risk Register / Risk Matrix |
| Control State | Enforced |
| Approach | Risk-Based Prioritization |
| Scope | On-Premise and Remote Systems |

**Validation Steps**

1. Simulated a Business Email Compromise (BEC) attempt to verify email security controls were functioning  
2. Verified that encryption of customer data reduced associated risk levels  
3. Confirmed that access restrictions did not interfere with normal system operations  
4. Ensured system stability after applying security controls  

# 2.0: Conclusion

## 2.1 Key Takeaways

- A Risk Register provides a structured approach to identifying and prioritizing security risks  
- High-risk issues must be addressed first to minimize potential operational and financial impact  
- Validation is essential to confirm that implemented controls function correctly  
- Security controls must balance protection with maintaining normal business operations  

## 2.2 Security Implications & Recommendations

**Risk: Business Email Compromise (BEC)**  
Attackers may use phishing or spoofed emails to trick users into transferring funds or disclosing sensitive information.  
**Mitigation:**  
- Implement SPF, DKIM, and DMARC for email authentication  
- Conduct regular phishing awareness training for users  
- Monitor email traffic for anomalies and suspicious behavior  

**Risk: Unprotected Backup Databases**  
Backups that are exposed or unencrypted may lead to unauthorized data access or theft.  
**Mitigation:**  
- Restrict access to backup systems using strict access controls  
- Remove public exposure of backup services  
- Encrypt all backup data both at rest and in transit  

**Risk: Access Control Weaknesses**  
Excessive permissions increase the risk of unauthorized access and privilege misuse.  
**Mitigation:**  
- Enforce least privilege principles  
- Perform regular access reviews and audits  
- Implement Role-Based Access Control (RBAC) where applicable  

**Best Practices**

- Maintain a centralized system for tracking all identified risks  
- Reassess controls after system changes or updates  
- Document configurations to support audits and repeatable deployments  
- Continuously update risk assessments to reflect evolving threats  

**Framework Alignment**

- Aligns with FFIEC Cybersecurity Assessment Tool guidance for financial institutions  
- Maps to NIST SP 800-30 (Risk Assessment) and NIST SP 800-53 (Security Controls)  
- Supports Identify and Protect functions of the NIST Cybersecurity Framework  
