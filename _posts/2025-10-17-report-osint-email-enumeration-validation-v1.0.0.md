---
title: "REPORT – OSINT Email Enumeration & Validation – v1.0.1"
date: 2025-10-17
author: Eldon Gabriel
tags: [Cybersecurity, OSINT, EmailEnumeration, MCSI, Verification, EthicalHacking]
excerpt: "Execution of email reconnaissance and validation techniques to identify organizational naming conventions and verify active communication channels."
image:
  path: "/assets/images/posts/osint_email_enum.png"
  thumbnail: "/assets/images/posts/osint_email_enum.png"
---

# 0.0 Executive Summary
This report documents an Open-Source Intelligence (OSINT) exercise focused on the enumeration and validation of organizational email addresses. The project successfully identified internal naming conventions through the analysis of publicly exposed documents and metadata. By utilizing a combination of pattern analysis and SMTP validation tools, the investigation verified active email accounts without direct contact. The final result demonstrates a low-cost, high-impact methodology for initial reconnaissance while highlighting the critical need for organizational metadata redaction and the use of generic aliases.

 

# 1.0 OSINT Email Enumeration & Validation

## 1.1 Project Description
The objective of this task was to perform non-intrusive reconnaissance to identify and verify potential email addresses associated with a target organization. The project aimed to leverage public data sources to reverse-engineer naming patterns and validate those guesses using third-party verification tools. The environment focused on maintaining ethical boundaries and operational security, ensuring that verified addresses were never contacted or used for social engineering, but rather documented as potential vulnerabilities.
 
## 1.2 Technical Task / Troubleshooting Process
The process involved a structured workflow from initial reconnaissance to technical validation of candidate email addresses.

**Key Actions & Observations**
* **Document Reconnaissance:** Analyzed publicly accessible PDFs and files to extract employee names and contact details, establishing a baseline for naming conventions.

* **Pattern Analysis:** Identified a predictable and uniform naming structure (e.g., firstname.lastname@domain.com) based on gathered intelligence.

* **Guess Generation:** Produced a list of candidate email addresses by applying the identified pattern to known organizational personnel.

* **Technical Verification:** Utilized verification tools to perform MX record checks and SMTP handshakes to confirm the validity of the generated addresses.

**Root Cause:** Predictable naming conventions and a lack of metadata redaction in public-facing documents allow for the rapid and accurate enumeration of internal email structures.

## 1.3 Resolution and Validation
Confirmation of valid communication channels was achieved through multi-tool verification and pattern consistency.

| Parameter | Configuration Value |
| :--- | :--- |
| **Methodology** | Passive OSINT / Enumeration |
| **Verification Level** | SMTP / MX Validation |
| **Naming Convention** | Predictable / Uniform |
| **Tool Accuracy** | Variable (Tier-dependent) |

**Validation Steps**
1. **Response Audit:** Confirmed at least one candidate address returned a definitive "valid" response across all utilized verification platforms.
2. **Convention Match:** Verified that identified patterns remained consistent across multiple departments and seniority levels.
3. **Redaction Check:** Evaluated the ease of data harvesting from public documents to justify security recommendations.



# 2.0: CONCLUSION

## 2.1 Key Takeaways
* **Metadata Exposure:** Publicly exposed PDFs are primary intelligence sources for identifying internal organizational structures.

* **Low-Cost Recon:** Email enumeration is an effective and accessible initial step in OSINT investigations that requires minimal resources.

* **Methodology Impact:** The accuracy of validation depends heavily on the specific methodology of the tool, ranging from simple MX checks to full SMTP validation.

## 2.2 Security Implications & Recommendations

**Risk: Automated Data Harvesting** Predictable email patterns enable attackers to quickly build targeted lists for phishing or credential stuffing attacks.  

**Mitigation:** Implement strict policies to audit and redact sensitive employee contact information from all publicly accessible digital assets.

**Risk: Social Engineering Vulnerability** Verified direct staff emails increase the likelihood of successful spear-phishing attempts.  

**Mitigation:** Replace direct individual contact details with generic aliases (e.g., info@, support@) in public-facing materials to obscure internal identity structures.
