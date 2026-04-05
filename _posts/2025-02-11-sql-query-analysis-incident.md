---
title: "REPORT – SQL Query Analysis Incident – v1.0.2"
date: 2025-02-11
author: Eldon Gabriel
categories: [Security Operations]
tags: [SQL, Data Analysis, Incident Response, Access Control, Security Monitoring]
excerpt: "Use of SQL queries to investigate failed login attempts, geographic anomalies, and access patterns for security auditing."
image:
  path: /assets/images/posts/sql-query-analysis.png
  thumbnail: /assets/images/posts/sql-query-analysis.png
---

# 0.0 Executive Summary

This report documents the use of database-based security monitoring within an enterprise environment.

The objective was to reduce the risk of brute-force attacks and unauthorized access by analyzing authentication logs using structured SQL queries.

The result is an improved security posture achieved by replacing manual log review with repeatable and auditable SQL queries that highlight high-risk activity such as repeated failures, after-hours access, and geographic anomalies.

 

# 1.0 SQL Query Analysis Incident

## 1.1 Project Description

The goal of this task was to perform systematic log analysis using SQL to detect suspicious authentication activity.

SQL queries were used to:
- Identify repeated failed login attempts during non-business hours  
- Detect authentication attempts from unexpected geographic regions  
- Analyze user access based on departments and device identifiers  

This approach helps protect systems from identity-based attacks by providing clear and actionable insights from large datasets.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on improving visibility into authentication logs and using SQL queries to identify abnormal patterns.

**Key Actions & Observations**

* Reviewed system logs and identified that raw data made it difficult to detect brute-force patterns.  

* Wrote SQL queries to filter failed login attempts using `success = 0`.  

* Used logical operators such as `AND`, `OR`, and `NOT` to refine query results by time, department, and region.  

* Isolated login attempts occurring outside normal business hours (after 18:00).  

* Identified authentication attempts originating from unexpected geographic locations, such as outside Mexico.  

* Reviewed departmental access to identify potentially over-privileged accounts in groups such as Marketing.  

* Verified database integrity, including the `logins` and `employees` tables.  

* Confirmed timestamp consistency for accurate time-based analysis.  

* Documented queries to support repeatable investigations and audits.  

**Root Cause:** The system lacked automated detection for authentication anomalies. This allowed slow and repeated login attempts to go unnoticed. This was resolved by using targeted SQL queries to identify and isolate suspicious behavior.

 

## 1.3 Resolution and Validation

The monitoring process was validated through execution of the SQL queries and review of the results.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | SQL / Database Management System |
| **Control State** | Enforced |
| **Security Mode** | Continuous Monitoring / Audit |
| **Scope** | Enterprise Authentication Logs |

**Validation Steps**

1. Ran queries to identify failed login attempts after 18:00 and observed multiple repeated failures.  

2. Verified that queries successfully isolated suspicious login attempts from unexpected IP ranges.  

3. Confirmed that query results matched the current state of the database tables and returned consistent outputs.  

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* SQL queries can be used to detect hidden patterns in authentication data.  
* Regular log analysis helps identify brute-force and unauthorized access attempts.  
* Structured queries improve visibility compared to manual log reviews.  
* Focusing on high-risk anomalies helps reduce unnecessary alerts and improves efficiency.  

 

## 2.2 Security Implications & Recommendations

**Risk: Brute-Force and Credential Stuffing**  
Repeated failed login attempts, especially outside business hours, may indicate automated attacks.  

**Mitigation:** Apply account lockout policies and monitor failed login thresholds over time.

**Risk: Geographic Anomalies**  
Logins from unexpected regions may indicate compromised credentials or unauthorized access.  

**Mitigation:** Use geolocation-based access controls and enforce Multi-Factor Authentication (MFA).

**Best Practices**

* Apply least privilege by aligning user access with departmental roles  
* Automate SQL-based monitoring queries using scheduled jobs  
* Validate queries after schema changes to ensure continued accuracy  
* Maintain documentation to support audits and compliance requirements such as PCI DSS and SOC 2  

**Framework Alignment**

* Supports NIST SP 800-53 (Audit and Accountability)  
* Aligns with ISO 27001 (A.12.4.1) for logging and monitoring  
* Supports the NIST CSF Detect function by enabling identification of security events through log analysis  
