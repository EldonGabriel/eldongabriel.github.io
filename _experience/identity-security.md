---
title: "Identity Security"
layout: collection-item
slug: identity-security
collection: experience
collection_item: true
order: 9
permalink: /identity-security/
image:
  path: /assets/images/headers/idsec.png
  thumbnail: /assets/images/headers/idsec.png
  caption: "Identity & Access Management Labs"
---

### Identity Security Lab Overview

Identity security focuses on protecting user identities, enforcing strong authentication controls, and ensuring that access to systems and sensitive resources is properly managed.

The labs and guides in this section demonstrate hands-on experience implementing identity and access management (IAM) controls, enforcing least-privilege access, and securing administrative configurations within Windows environments.

These exercises highlight how administrators enforce access restrictions, protect credentials, and monitor systems to detect unauthorized access and privilege misuse.

### Lab Distribution Summary

| Category | Labs |
|--------|------|
| Identity & Access Management | 8 |
| **Total Identity Security Labs Documented** | **8** |

---

# Identity & Access Management

Identity and Access Management (IAM) ensures that only authorized users can access systems and sensitive resources. These labs demonstrate how administrative controls, policy enforcement, and system configurations are used to protect identities and reduce unauthorized access risk.

## Identity Security Portfolio

### 🔐 Access Control & Identity Protection

<div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(320px,1fr)); gap:20px; margin-top:20px; margin-bottom:40px;">

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>SOP – Securing Folder Access with Permissions – v1.0.1</h5>
<p>Demonstrates how Windows NTFS permissions can be configured to protect sensitive directories and enforce least-privilege access controls.</p>
<p><strong>Skills:</strong> NTFS Permission Management · Access Control Enforcement · Least Privilege</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/sop-securing-folder-access-permissions-v1.0.1/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – File Ownership Recovery – v1.0.0</h5>
<p>Recovered NTFS file ownership and restored proper permission controls on secured systems.</p>
<p><strong>Skills:</strong> NTFS Permissions · Access Recovery</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-file-ownership-recovery/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>SOP – Password & Account Lockout GPO Hardening – v1.0.1</h5>
<p>Implemented enterprise-grade password complexity and lockout thresholds to mitigate brute-force attempts.</p>
<p><strong>Skills:</strong> Identity Security · Password Policy</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/sop-password-account-lockout-gpo-hardening-v1.0.1/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Deploy Local GPO for Windows Security Policies – v1.0.0</h5>
<p>Configured secure credential entry protections through Windows security policy controls.</p>
<p><strong>Skills:</strong> Credential Protection · GPO Security</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-deploy-local-gpo-windows-security-policies-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Applying a Local GPO for Session Lock Enforcement – v1.0.0</h5>
<p>Configured automatic session lock enforcement using Local Group Policy to reduce unauthorized access risk on unattended systems.</p>
<p><strong>Skills:</strong> Identity Security · GPO Configuration · Endpoint Hardening · Access Control</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-gpo-applying-local-gpo-session-lock-enforcement-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Hardening Windows User Rights via Local Group Policy – v1.0.0</h5>
<p>Restricted administrative privileges and enforced least-privilege access policies via GPO.</p>
<p><strong>Skills:</strong> Access Control · Privilege Hardening</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-hardening-windows-user-rights-local-group-policy-v1.0.0//" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a></p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Kerberos Authentication Protocol – v1.0.0</h5>
<p>Studied and documented the Kerberos authentication process, including ticket-granting mechanisms and secure authentication workflows used in Active Directory environments.</p>
<p><strong>Skills:</strong> Authentication Protocols · Active Directory · Identity Security · Ticket-Based Authentication</p>
<p align="center" style="margin-top:20px;"><a href="https://eldongabriel.github.io/report-kerberos-authentication-protocol-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

<div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
<h5>REPORT – Password Managers – v1.0.0</h5>
<p>Technical analysis of password manager technologies and their role in protecting user credentials through encrypted storage and zero-knowledge security models.</p>
<p><strong>Skills:</strong> Identity Security · Credential Management · Authentication Controls</p>
<p align="center" style="margin-top:20px;">
<a href="https://eldongabriel.github.io/report-password-managers-v1.0.0/" style="padding:10px 20px; border:1px solid #fff; color:#fff; text-decoration:none; border-radius:5px; font-weight:bold;">View Report</a>
</p>
</div>

</div>

---

# Portfolio Documentation

This section highlights applied identity security practices, including access control enforcement, credential protection, and privilege management within Windows environments.

These labs simulate real-world administrative scenarios where identity misuse, privilege escalation, and unauthorized access represent critical security risks.

Additional configuration notes, lab documentation, and supporting technical records are maintained within a private research archive.

Complete guides, blogs, and supporting technical materials are restricted and available upon request for professional or technical review.
