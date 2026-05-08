---
title: "REPORT – USB Passthrough Instability in VirtualBox (Kali Linux) – v1.0.0"
date: 2026-04-24
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Hardware Integrity, Virtualization, Kali Linux, I/O Troubleshooting, Linux Security]
excerpt: "Analysis of USB I/O failures during virtualization, with secure Linux filesystem configuration and execution control."
image:
  path: /assets/images/posts/usb-io-failure.png
  thumbnail: /assets/images/posts/usb-io-failure.png
---

# 0.0 Executive Summary

This report explains how repeated USB failures caused system crashes during a Kali Linux laboratory running in a virtual machine. The goal was to determine the cause of the connection drops and complete the task of setting up a secure Linux filesystem. This issue was traced to unstable communication between the Windows host and VirtualBox during the USB passthrough. This causes the USB device to disconnect during heavy write operations, such as formatting. 

The system was stabilized by adjusting the power settings and switching the virtual USB controller to a more reliable mode. Once stable, Linux security controls were applied using the `noexec` mount option and proper file ownership. This ensured that the USB could store data but could not run malicious files.

 

# 1.0 USB I/O Failure & Virtualization Instability Analysis

## 1.1 Project Description

The goal of this task was to fix USB instability in a virtual machine and safely manage external storage using the Linux operating system.

The work focused on:

- **Fixing Connection Issues:** Identify why the USB device disconnects during use  
- **Setting Up Filesystems:** Create and format partitions using Linux tools  
- **Improving Security:** Prevent files on the USB from being executed  
- **Managing Access:** Assign correct ownership so normal users can safely use the device  

This ensures that the USB device is both usable and secure inside a virtual environment.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on identifying the source of the failure and fixing it step by step.

### Key Actions & Observations

**1. Hardware Stabilization**
- USB disconnections happened during heavy write operations (like formatting)
- The issue was linked to host power settings and USB controller behavior
- Switching VirtualBox to **USB 2.0 (EHCI)** improved stability

**2. Filesystem Setup**
- Used `diskpart` to clean the drive on Windows
- Used `fdisk` and `mkfs.ext4` in Linux to create and format partitions
- Fixed “device busy” issues by unmounting active volumes

**3. Security Configuration**
- Mounted the USB with `noexec` to block file execution
- Tested by running a script (`test.sh`) which failed with “Permission Denied”
- Changed ownership using `chown` so the standard user could manage files safely

**4. Root Cause**

The failure was caused by an unstable USB passthrough between the host system and VirtualBox.  
This instability appeared during high disk activity and caused the device to be disconnected.

 

## 1.3 Resolution and Validation

The system was stabilized and secured using the following setup.

| Parameter | Configuration Value |
| :--- | :--- |
| Hypervisor Setting | USB 2.0 (EHCI) |
| Filesystem Type | EXT4 |
| Security Flag | noexec |
| Owner | kali:kali |

### Validation Steps

1. **Stable Connection**
   - USB remained connected during full formatting operations

2. **Correct Permissions**
   - Verified ownership using `ls -l`

3. **Security Enforcement**
   - Script execution failed even with execute permissions
   - Confirms `noexec` is working at the kernel level

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

- USB stability directly affects virtual machine performance  
- Host system settings can break virtualization even if the guest OS is correct  
- Linux mount options provide strong security controls  
- Testing should include attempts to break the system (negative testing)  

 

## 2.2 Security Implications & Recommendations

### Risks

**1. Malware Execution from USB:** USB devices can carry malicious scripts

**Fix:** Use `noexec` on all removable drives
 

**2. Improper Permissions:** Using root ownership increases risk of mistakes

**Fix:** Assign ownership to standard users using `chown`


### Best Practices

- Use stable USB controller settings (USB 2.0 if needed)
- Avoid relying on auto-mount for untrusted devices
- Always verify mount options using `mount` command
- Document outputs for validation and auditing

 
### Framework Alignment

- Supports **NIST CSF – Protect (PR)** through secure configuration  
- Aligns with **ISO 27001 A.12.6.2** (control of software execution)  
- Follows Linux security best practices for removable media
