---
title: "GUIDE – UTM Kali Linux Shared Folder Configuration – v1.0.0"
date: 2025-10-17
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Cybersecurity, Virtualization, Linux, UTM, SystemAdministration]
excerpt: "Implementation of a persistent shared folder between macOS and Kali Linux using the 9p protocol within the UTM hypervisor."
image:
  path: "/assets/images/posts/utm_kali_shared_folder.png"
  thumbnail: "/assets/images/posts/utm_kali_shared_folder.png"
---

# 0.0 Executive Summary
This report documents the configuration of a persistent shared folder between a macOS host and a Kali Linux virtual machine using the UTM hypervisor. The project addressed initial mounting failures associated with the VirtIO-FS protocol by implementing a technical fallback to the 9p virtio protocol. The final result established a reliable, automated file-sharing channel between the host and guest systems, validated through fstab persistence and permission audits.



# 1.0 UTM Kali Linux Shared Folder Configuration

## 1.1 Project Description
The objective of this task was to enable seamless data transfer between a macOS host and a Kali Linux VM to facilitate the movement of tools, reports, and evidence. The project aimed to overcome filesystem protocol incompatibilities within the UTM environment. The task required configuring kernel-level mount points and ensuring that the shared directory remained accessible across system reboots without manual intervention.
 
## 1.2 Technical Task / Troubleshooting Process
The process focused on diagnosing mounting errors and establishing a persistent filesystem link.

**Key Actions & Observations**
* **Protocol Analysis:** Identified that the default VirtIO-FS method failed to mount correctly, requiring a transition to the 9p protocol.

* **Manual Mounting:** Utilized the `mount` command with specific `9p` versioning and transport arguments to establish the initial connection.

* **Persistence Configuration:** Modified the `/etc/fstab` file to automate the mounting process during the system boot sequence.

* **Permission Audit:** Verified file ownership and read/write capabilities within the `test_folder` directory to ensure operational access.

**Root Cause:** Initial mounting failures were caused by incompatibilities between the guest kernel and the VirtIO-FS protocol, necessitating a fallback to the more compatible 9p virtio filesystem.

## 1.3 Resolution and Validation
A stable and persistent shared environment was achieved through specific mount arguments and fstab automation.

| Parameter | Configuration Value |
| :--- | :--- |
| **Hypervisor** | UTM |
| **Protocol** | 9p (virtio) |
| **Version** | 9p2000.L |
| **Mount Options** | rw, nofail |

**Validation Steps**
1. **Boot Test:** Confirmed the shared folder mounted automatically upon system restart without errors.
2. **Transfer Test:** Verified successful bidirectional file transfers between the macOS host and the Kali Linux guest.
3. **Integrity Check:** Validated that file permissions (chmod/chown) were correctly maintained within the mounted directory.



# 2.0: CONCLUSION

## 2.1 Key Takeaways
* **Protocol Versatility:** In virtualized environments, understanding secondary filesystem protocols like 9p is essential when primary protocols fail.

* **Persistence is Vital:** Manual mounts are insufficient for operational workflows; fstab integration is required for reliability.

* **Kernel Compatibility:** Successful virtualization management depends on aligning guest kernel capabilities with hypervisor-provided drivers.

## 2.2 Security Implications & Recommendations

**Risk: Unauthorized Data Exposure** Shared folders can become a vector for malware or unauthorized data access if permissions are overly permissive.  

**Mitigation:** Limit access to the shared directory using strict `chmod` and `chown` permissions and disable the share when not actively required.

**Risk: Sensitive Information Leakage** Transferring confidential data across unencrypted shared folders may expose it to unauthorized host-level processes.  
**Mitigation:** Utilize encrypted archives for sensitive data transfers and regularly audit the contents of the shared directory.
