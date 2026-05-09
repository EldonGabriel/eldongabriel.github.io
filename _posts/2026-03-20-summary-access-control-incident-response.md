---
title: "SUMMARY – Identity & Access Management: Access Control Incident Response – v1.0.0"
date: 2026-03-20
author: Eldon Gabriel
categories: [Identity & Access Management]
tags: [Access Control, Least Privilege, NIST SP 800-53, AC-6, Incident Response]
excerpt: "Analysis of a data exposure incident caused by weak access controls and lack of enforced security policies."
image:
  path: /assets/images/posts/access-control.png
  thumbnail: /assets/images/posts/access-control.png
--- 
 
# 0.0 Executive Summary

This report analyzes a data exposure incident where sensitive internal design materials were unintentionally shared outside the organization due to weak access control configurations and reliance on trust-based policies instead of technical enforcement. The incident resulted in unauthorized exposure of multiple internal documents to external parties.

The root issue was traced to insufficient enforcement of least privilege and lack of automated controls governing file sharing. The resolution focused on implementing system-enforced restrictions such as default internal-only access and automated link expiration, aligned with NIST SP 800-53 AC-6 (Least Privilege).


# 1.0 AC Incident Analysis & NIST Alignment

## 1.1 Project Description

The scope of this task involved investigating a data exposure incident in which sensitive product development files and customer analytics data were unintentionally disclosed. The environment consisted of a controlled organizational file-sharing system used by internal teams.

The objective was to identify the root cause of the access control failure, map the issue to relevant NIST SP 800-53 controls, and implement corrective measures to prevent recurrence within the system.

## 1.2 Technical Task / Troubleshooting Process

The investigation focused on evaluating user permissions, sharing configurations, and access boundaries to determine how unauthorized exposure occurred.

**Key Actions & Observations**

* **Incident Review:** A sales manager shared an internal folder with their team but did not revoke access after the intended use.
* **Observation:** A team member shared a folder link externally instead of isolating specific files intended for sharing.
* **Control Mapping:** The issue aligns with the NIST Cybersecurity Framework (CSF) Protect function, specifically PR.DS-5 (Data is managed based on classification and sensitivity).
* **NIST Analysis:** The system did not enforce Principle of Least Privilege as defined in NIST SP 800-53 AC-6.

**Root Cause:** The failure stemmed from reliance on manual user behavior and trust-based policies without technical enforcement mechanisms to restrict external sharing.

## 1.3 Resolution and Validation

Technical safeguards were implemented to enforce access control policies and reduce reliance on manual processes.

| Parameter             | Configuration Value    |
| :-------------------- | :--------------------- |
| **Primary Framework** | NIST SP 800-53 Rev. 5  |
| **Core Control**      | AC-6 (Least Privilege) |
| **Default Sharing**   | Internal Only          |
| **Link Security**     | Automatic Expiration   |

**Validation Steps**

1. Policy enforcement verified by restricting external domain sharing by default.

2. Access audit performed to review and revoke unnecessary external links.

3. Staff training conducted to reinforce secure file handling and proper sharing procedures.


# 2.0: Conclusion

## 2.1 Key Takeaways

* Technical enforcement of access policies is required to prevent reliance on user discretion.
* Least privilege must be continuously maintained through regular audits and controls.
* Most data exposure incidents result from misconfiguration and human error rather than malicious intent.

## 2.2 Security Implications & Recommendations

**Risk: Unauthorized Data Exposure**
Over-permissioned access and uncontrolled sharing mechanisms can lead to unintended disclosure of sensitive organizational data.

**Mitigation:** Enforce default internal-only access, restrict external sharing to approved domains, and implement automated link expiration controls.

**Risk: Audit and Compliance Gaps**
Without regular reviews, excessive or orphaned permissions may persist and increase exposure risk.

**Mitigation:** Establish recurring access reviews, focusing on sensitive datasets such as product development and customer information, and align with NIST SP 800-53 access control auditing practices.
