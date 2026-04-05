---
title: "REPORT – Linux File Permissions Management – v1.0.2"
date: 2025-02-18
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Linux, File Permissions, Access Control, Security Hardening, Bash]
excerpt: "Implementation of the Principle of Least Privilege (PoLP) by managing Linux file and directory permissions to protect sensitive data."
image:
  path: /assets/images/posts/linux-file-permissions.png
  thumbnail: /assets/images/posts/linux-file-permissions.png
---

# 0.0 Executive Summary

This report describes how file and directory permissions were configured on a Linux system to improve security.

The goal was to reduce the risk of unauthorized access and accidental changes by applying proper permissions to users, groups, and others.

The issue was that default permissions allowed too much access to sensitive files. This was corrected by using standard Linux tools such as `chmod` and `chown` to enforce stricter access rules. As a result, only authorized users can now read or modify protected data.

 

# 1.0 Linux File Permissions Management

## 1.1 Project Description

The goal of this task was to apply secure file permissions in a Linux environment to protect sensitive research data.

The work focused on:
- Reviewing current permissions on files and directories  
- Removing unnecessary access rights  
- Ensuring only authorized users could read or modify data  
- Documenting permission changes for tracking and audits  

This helps prevent unauthorized access and reduces the chance of accidental data modification.

 

## 1.2 Technical Task / Troubleshooting Process

This process focused on identifying weak permission settings and correcting them using Linux command-line tools.

**Key Actions & Observations**

* Reviewed file permissions using `ls -la` and found that some files allowed access to all users.  

* Identified that certain sensitive files had overly permissive settings such as write access for "others".  

* Used Bash commands to update permissions:
  - `chmod` to change file and directory access  
  - `chown` to adjust ownership where needed  

* Applied stricter permissions to:
  - Restrict the `.project_x.txt` file to read-only access for authorized users  
  - Limit access to the `drafts` directory so only the primary user could access it  

* Verified:
  - Correct user and group ownership  
  - Permissions applied to nested files and directories  

* Documented all changes for future review and repeatability  

**Root Cause:** Default Linux permission settings can sometimes allow broad access (such as 775 or 777). This creates unnecessary exposure. The issue was resolved by applying stricter permission rules using `chmod` and ownership controls.

 

## 1.3 Resolution and Validation

The updated permissions were tested to confirm they worked as expected.

| Parameter | Configuration Value |
| :--- | :--- |
| **Management Tool** | Bash (chmod / chown) |
| **Control State** | Enforced |
| **Security Mode** | Principle of Least Privilege (PoLP) |
| **Scope** | Projects and Research Directories |

**Validation Steps**

1. Attempted to modify a restricted file using an unauthorized user account.  

2. Verified the system denied access with a "Permission denied" error.  

3. Confirmed authorized users could still access their required files and directories without issues.  

4. Ensured no unintended permission changes affected system stability or usability.  

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

* Default file permissions can expose sensitive data if not properly configured.  

* Applying the Principle of Least Privilege reduces unnecessary access.  

* Linux tools like `chmod` and `chown` provide full control over file access.  

* Testing permissions after changes is necessary to confirm proper enforcement.  

 

## 2.2 Security Implications & Recommendations

**Risk: Unauthorized Data Modification**  
If write access is too broad, users may change or delete important files.  

**Mitigation:** Apply strict permissions and regularly check for overly permissive settings such as `777`.

**Risk: Execution of Unauthorized Scripts**  
Executable permissions on the wrong files can allow malicious code to run.  

**Mitigation:** Remove execute permissions where they are not needed and control directory access carefully.

**Best Practices**

* Use `600` for files and `700` for directories when possible.  
* Set a default permission policy using `umask`.  
* Review hidden files to ensure they follow the same permission rules.  
* Keep documentation of permission changes for audits and troubleshooting.  

**Framework Alignment**

* Aligns with CIS Linux Benchmarks for system hardening  
* Supports NIST SP 800-53 (Access Control – AC-6)  
* Supports NIST CSF Protect function by securing data at the operating system level  
