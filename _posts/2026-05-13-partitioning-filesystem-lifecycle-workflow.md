---
title: "REPORT – Linux Admin: Partitioning and Filesystem Lifecycle Workflow – v1.0.0"
date: 2026-05-13
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Linux, Storage Management, fdisk, ext4, Filesystem Expansion, System Administration]
excerpt: "Technical implementation of disk partitioning and non-destructive filesystem expansion."
image:
  path: /assets/images/posts/partitioning.png
  thumbnail: /assets/images/posts/partitioning.png
---

# 0.0 Executive Summary

This report documents disk partitioning and filesystem expansion on an Ubuntu system. The objective was to expand the storage without data loss.

The process follows a layered approach: physical disk → partition → filesystem. The key operations include partition creation, ext4 filesystem initialization, and non-destructive expansion using existing filesystem signatures.

The result is a repeatable workflow for safely scaling storage while preserving the data integrity.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 Partitioning and Filesystem Expansion

## 1.1 Project Description

The goal of this task was to develop practical skills in Linux storage management, specifically resizing volumes to meet the increased storage requirements.

This implementation demonstrates the following:

- **Disk lifecycle management:** cleaning, partitioning, and formatting  
- **Non-destructive scaling:** expanding a partition while preserving data  
- **Filesystem integrity enforcement:** validating with `e2fsck` before resizing  
- **Layered architecture awareness:** separating disk, partition, and filesystem operations  

## 1.2 Technical Execution and Troubleshooting

### Issue

The partition size was increased, but the filesystem remained at its original size, resulting in an unused disk space.

### 1.2.1 Disk Preparation and Partitioning

- **Wiping signatures:**  
  `sudo wipefs -a /dev/sdb` used to reset the disk to a clean state  

- **Creating partition:**  
  `fdisk` used to create a 1GB primary partition  

- **Filesystem creation:**  
  `sudo mkfs.ext4 /dev/sdb1` initialized the filesystem  

### 1.2.2 Non-Destructive Expansion

- **Unmounting:**  
  `sudo umount /mnt/data1` to prevent active writes  

- **Partition modification:**  
  Deleted and recreated partition using the SAME starting sector while extending the end sector  

- **Signature preservation:**  
  When prompted:  
  *“Partition contains an ext4 signature. Remove?”* → **Selected No**  

- **Filesystem expansion:**  
  `sudo resize2fs /dev/sdb1` extended filesystem to match partition size  

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

### Key Insight

Expanding a partition does not increase usable storage until the filesystem is resized.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

### Troubleshooting Highlights

- **Unused Space Issue:**  
  Partition expansion alone does not update filesystem capacity  

- **Filesystem Integrity Requirement:**  
  `resize2fs` required a clean filesystem → resolved with  
  `sudo e2fsck -f /dev/sdb1`  

## 1.3 Resolution and Validation

### Validation Steps

1. **Layer verification:**  
   `lsblk -f` confirmed partition structure and ext4 signature  

2. **Capacity validation:**  
   `df -h` confirmed expanded usable space  

3. **Mount integrity:**  
   Verified `/mnt/data1` remained accessible with intact data  

### Tool Mapping

| Layer        | Tool Used        |
|-------------|-----------------|
| Partition   | fdisk           |
| Filesystem  | resize2fs       |
| Validation  | lsblk, df       |


# 2.0 CONCLUSION

## 2.1 Key Takeaways

- Partition changes do not affect the filesystem until resized  
- Preserving filesystem signatures prevents data loss  
- Correct sequence is critical:  
  **Unmount → Modify → Resize → Remount**  
- Validation must confirm alignment between partition and filesystem  


## 2.2 Security Implications and Recommendations

**Risk:** Data Loss During Partition Changes

Incorrect handling of filesystem signatures can result in permanent losses of data.

**Mitigation:**
- Perform backups before modification  
- Run `e2fsck -f` before resizing  


**Risk:** Unauthorized Disk Operations

Improper access to disk utilities can lead to system compromise and data destruction.

**Mitigation:**
- Restrict access to `fdisk`, `wipefs`, and `mkfs`  
- Monitor system logs for disk modification activity  


**Best Practices**

- Use full device paths (e.g. `/dev/sdb1`)  
- Do not modify mounted partitions  
- Inspect signatures before changes using `wipefs`  
- Maintain records of partition changes for recovery  


**Framework Alignment**

- **NIST SP 800-53 (CP-9):** Backup and storage management  
- **CIS Control 3:** Data protection  
- **ISO 27001 (A.12.1.3):** Capacity management  
