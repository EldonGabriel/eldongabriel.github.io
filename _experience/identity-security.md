---
title: "Identity Security"
layout: collection-item
slug: identity-security
collection: experience
collection_item: true
order: 9
permalink: /identity-security/
image:
  path: /assets/images/headers/section-header.png
  thumbnail: /assets/images/headers/section-header.png
  caption: "Identity & Access Management Labs"
---

### Lab Distribution Summary

| Category | Labs |
|--------|------|
| Identity & Access Management | 9 |
| **Total Identity Security Labs Documented** | **10** |

<hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

## Identity Security Laboratory Overview

<p style="line-height:1.6; font-size:1.05em;">
This section documents hands-on identity security labs that focus on access control, authentication hardening, and privilege management in Windows environments. Work includes implementing identity and access management (IAM) controls, such as least-privilege enforcement, credential protection, and secure administrative configuration.
</p>

<p style="line-height:1.6; font-size:1.05em;">
All labs focus on enforcing access control policies and reducing the risk of unauthorized access and privilege escalation.
</p>

## Identity Protection & Access Control

### 🔐 Access Control & Identity Protection

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>SOP – Securing Folder Access with Permissions – v1.0.1</h5>
<p>Configuring NTFS permissions to protect sensitive directories and enforce least-privilege access.</p>
<p><strong>Skills:</strong> NTFS Permissions · Access Control · Least Privilege</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/sop-securing-folder-access-permissions-v1.0.1/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – File Ownership Recovery – v1.0.0</h5>
<p>Recovering NTFS file ownership and restoring secure permission configurations.</p>
<p><strong>Skills:</strong> NTFS Permissions · Access Recovery</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-file-ownership-recovery/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>SOP – Password and Account Lockout GPO Hardening – v1.0.1</h5>
<p>Implementing password complexity and account lockout policies to reduce brute-force attack risk.</p>
<p><strong>Skills:</strong> Password Policy · GPO · Identity Security</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/sop-password-account-lockout-gpo-hardening-v1.0.1/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Deploy Local GPO for Windows Security Policies – v1.0.0</h5>
<p>Configuring Windows security policies to protect credential handling and system access.</p>
<p><strong>Skills:</strong> GPO Security · Credential Protection · Policy Enforcement</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-deploy-local-gpo-windows-security-policies-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Applying Local GPO for Session Lock Enforcement – v1.0.0</h5>
<p>Enforcing automatic session lock policies to reduce unauthorized access on unattended systems.</p>
<p><strong>Skills:</strong> GPO Configuration · Endpoint Security · Access Control</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-gpo-applying-local-gpo-session-lock-enforcement-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Hardening Windows User Rights via Local Group Policy – v1.0.0</h5>
<p>Restricting administrative privileges to enforce least-privilege access.</p>
<p><strong>Skills:</strong> Privilege Management · Access Control · GPO</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-hardening-windows-user-rights-local-group-policy-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Kerberos Authentication Protocol – v1.0.0</h5>
<p>Analyzing Kerberos authentication, including ticket-granting processes and secure identity verification in Active Directory.</p>
<p><strong>Skills:</strong> Kerberos · Active Directory · Authentication</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-kerberos-authentication-protocol-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Password Managers – v1.0.0</h5>
<p>Analyzing password manager technologies and their role in protecting credentials through encrypted storage.</p>
<p><strong>Skills:</strong> Credential Management · Encryption · Authentication</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-password-managers-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>SUMMARY – Identity & Access Management: Access Control Incident Response (NIST-Aligned) – v1.0.0</h5>
<p>Analysis of a real-world data leak caused by weak access controls, identifying control gaps and applying least privilege principles.</p>
<p><strong>Skills:</strong> Risk Assessment · Access Control · NIST Alignment</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/summary-access-control-incident-response/" target="_blank" style="padding:10px 20px; border:1px solid rgba(255,255,255,0.3); color:white; border-radius:5px; font-weight:bold; font-size:0.9em; text-decoration:none;">View Report</a>
</p>
</div>

</div>

<hr style="border:1px solid rgba(255,255,255,0.1); margin:40px 0;">

## Portfolio Documentation

This section presents the identity security work, including access control enforcement, credential protection, and privilege management within Windows environments.

The selected materials demonstrate core IAM capabilities, whereas additional configuration data and supporting documentation are maintained in a private archive.

Full documentation is available upon request for professional or technical review.
