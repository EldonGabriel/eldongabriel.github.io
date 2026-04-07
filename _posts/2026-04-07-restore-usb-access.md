---
title: "REPORT – Restore USB Access on a Windows 10 VM – v1.0.0"
date: 2026-04-07
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Windows 10, Virtualization, VirtualBox, Hardware Passthrough, Troubleshooting, Filesystem Integrity]
excerpt: "Technical resolution of USB detection failures and volume locks within a virtualized environment, including filesystem repair and stable hardware filter configuration."
image:
  path: /assets/images/posts/restore-usb.png
  thumbnail: /assets/images/posts/restore-usb.png
---

## 0.0 Executive Summary

This report explains the steps taken to fix USB detection issues and improve USB passthrough for a Windows 10 virtual machine (VM).

The goal was to ensure external USB devices worked reliably and to reduce the risk of data corruption caused by unstable connections or conflicts on the host system.

The issue was resolved by using VirtualBox USB filters instead of manual USB connections. The fix was confirmed using `diskpart` to verify the drive was detected and `chkdsk` logs to confirm the file system was healthy and accessible.

 

## 1.0 Restoring USB Access and Volume Integrity

### 1.1 Project Description

The goal of this task was to fix an issue where the VM could not detect or use external USB devices.

A structured troubleshooting process was used to:

* Set up consistent hardware mapping using USB filters in VirtualBox
* Fix resource conflicts caused by open files or processes locking the USB device
* Check file system health using Windows Event Viewer logs

This ensures that data transfers using external storage happen on a stable and verified system.

 

### 1.2 Technical Task / Troubleshooting Process

The process focused on identifying where the failure occurred in the virtualization setup and applying fixes to restore access.

**Key Actions & Observations**

* **Infrastructure Check:** The host system detected the USB device, but the VM did not. This showed a passthrough configuration issue.

* **Hardware Mapping:** VirtualBox USB filters were configured using the device’s Vendor and Product ID so the VM could automatically detect the USB device.

* **Volume Remediation:** Errors such as “Cannot open volume for direct access” were fixed by closing any active handles and running: 'chkdsk E: /x /f /v'


This forced the drive to dismount and performed a full file system check.

* **Verification of Evidence:**

  * `diskpart` was used to confirm the volume was detected and assigned a drive letter
  * `wevtutil` was used to export `chkdsk` logs from the Event Viewer to confirm the file system was clean

**Root Cause:**
The issue was caused by missing VirtualBox USB filters combined with active file locks or processes on the host system. These prevented the VM from gaining proper access to the USB device.

 

### 1.3 Resolution and Validation

Access was restored by setting up USB filters and confirming the file system was working correctly.

| Parameter       | Configuration Value            |
| :-------------- | :----------------------------- |
| Management Tool | VirtualBox / diskpart / chkdsk |
| Device State    | Connected / Verified           |
| Access Mode     | VirtualBox USB passthrough     |
| Scope           | Windows 10 VM Hardware Access  |

**Validation Steps**

1. **Functional Test:** The USB device was reconnected and automatically detected by the VM through the USB filter.

2. **Volume Verification:** Running `diskpart list volume` confirmed the drive (E:) was visible and usable.

3. **Data Integrity Check:** A read and write test confirmed the drive worked correctly, and `chkdsk` completed without reporting errors.

 

## 2.0 Conclusion

### 2.1 Key Takeaways

* USB passthrough depends on correct configuration in the hypervisor layer
* Troubleshooting must address both hardware detection and software conflicts
* Event Viewer logs help confirm whether file system corruption occurred
* Following a step-by-step approach from detection to repair helps avoid misdiagnosing the issue

 
### 2.2 Operational Implications & Recommendations

**Risk: File System Corruption**  
Unstable or improper disconnection of USB devices can damage the file system, including the Master File Table (MFT).  

**Mitigation:** Run `chkdsk` after any passthrough failure.

**Risk: Resource Conflicts**  
Open files or processes on the host system can prevent the VM from accessing the USB device.  

**Mitigation:** Close all programs using the USB drive before connecting it to the VM.

**Best Practices**

* Use specific USB filters instead of manual connections  
* Check Event Viewer logs to confirm repair results  
* Avoid using the USB device on both host and VM at the same time  
* Follow standard troubleshooting steps to maintain system stability  

**Framework Alignment**

* Supports NIST Cybersecurity Framework **PR.DS-4 (Capacity and Availability)** by ensuring hardware is available and functioning properly  
* Helps maintain data integrity by verifying storage health before use 
