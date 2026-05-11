---
title: "REPORT – USN Journal Analysis – v1.0.0"
date: 2026-04-08
author: Eldon Gabriel
categories: [Security Operations]
tags: [Windows Forensics, NTFS, USN Journal, Incident Response, File Integrity]
excerpt: "Analysis of the NTFS USN Journal for tracking file activity and building forensic timelines."
image:
  path: /assets/images/posts/usn-journal.png
  thumbnail: /assets/images/posts/usn-journal.png
---

# 0.0 Executive Summary

This report explains how the NTFS USN Journal works and how it can be used in forensic investigations. The goal was to improve the visibility of file activity on a Windows system. Using the `fsutil` tool, this project shows how Windows records file changes, such as create, delete, and modify events.

The result is a clear method for tracking file activity. This helps in detecting attacks, such as timestomping and unauthorized file access. It also improves the system’s ability to support the investigations.

 

# 1.0 USN Journal Architecture and Forensic Analysis

## 1.1 Project Description

The goal of this task was to understand how the USN Journal tracks file changes and how it can prevent missing evidence during investigations.

The `fsutil` tool was used to:

- Check if the USN Journal is enabled and working on system drives  
- Identify “Reason Codes” that show what type of file change happened  
- Track file activity in order using USN records  

This ensures that file changes are recorded in a way that cannot be easily faked by changing the timestamps.

 

## 1.2 Technical Task / Troubleshooting Process

This process focused on how NTFS tracks file changes and collects useful forensic data.

### Key Actions & Observations

- Reviewed how the USN Journal records file and folder changes before they are written to the Master File Table (MFT)  

The following ‘fsutil` commands were used:

  - `fsutil usn queryjournal` to view journal details like size and next record  
  - `fsutil usn readjournal` to read file change events and reason codes  

Performed analysis to:

  - Detect gaps in records that may show tampering  
  - Rebuild timelines using file references and USN values  

The system conditions were checked as follows:

  - Confirmed the journal is enabled  
  - Reviewed how it grows and removes old data  

- Documented all steps to allow repeat use in future investigations  

**Root Cause:** File timestamps can be changed by attackers to hide activity.  

**Resolution:** The USN Journal provides a sequential record of changes that is harder to modify, making it more reliable for investigations.

 

## 1.3 Resolution and Validation

The system was checked to confirm that the USN Journal was active and that the data were recorded correctly.

| Parameter        | Configuration Value              |
|-----------------|--------------------------------|
| Management Tool | fsutil / Windows API           |
| Data Source     | $Extend\$UsnJrnl:$J            |
| Security Mode   | Integrity Monitoring / Timeline Tracking |
| Scope           | Windows NTFS Volumes           |

### Validation Steps

1. Created, renamed, and deleted a test file to generate activity  
2. Confirmed that `fsutil` showed correct USN records for each action  
3. Verified that records were logged in order without gaps  
4. Checked that journal size settings balance performance and data retention  

 

# 2.0 Conclusion

## 2.1 Key Takeaways

- File system monitoring is important for detecting advanced attacks  
- The USN Journal helps track file activity even if timestamps are changed  
- Proper journal size settings help keep enough history for investigations  
- Testing is needed to confirm logs are accurate and complete  

 

## 2.2 Security Implications & Recommendations

**Risk** Timestomping (Fake Timestamps)
Attackers can change the file timestamps to hide their activities.  

**Mitigation:** Use the USN Journal to verify the real order of file events during investigations.

 

**Risk:** Journal Overwrite (Loss of Evidence)
High system activity can delete older records.  

**Mitigation:** Increase the journal size (`MaxSize`) on important systems to keep more history.

 

**Best Practices**

- Limit access to tools like `fsutil` to authorized users only  
- Monitor for deletion of the USN Journal, which may indicate an attack  
- Recheck settings after updates to ensure logging is still active  
- Document all commands and findings for repeatable investigations  

 

**Framework Alignment**

- Supports forensic practices from NIST SP 800-86  
- Aligns with ISO 27001 logging and monitoring requirements  
- Strengthens the Detect and Respond functions of the NIST CSF  
