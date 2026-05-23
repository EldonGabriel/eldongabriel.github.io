---
title: "REPORT – Linux Admin: Network File System (NFS) Deployment – v1.0.0"
date: 2026-05-22
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Linux, NFS, Storage Management, Network Security, System Administration]
excerpt: "Technical deployment and hardening of a cross-network Network File System (NFS) architecture."
image:
  path: /assets/images/posts/NFS.png
  thumbnail: /assets/images/posts/NFS.png
---

# 0.0 Executive Summary

This report documents the secure deployment, configuration, and validation of a cross-network Network File System (NFS) architecture between a dedicated server and remote client. The primary objective was to establish a boot-persistent network share while validating the system-level access controls and user identity mappings.

The implementation involved configuring host-based access control lists through `/etc/exports`, aligning server-side filesystem permissions with anonymous network mappings, and defining static mounts within the system file table. Administrative identity protection was enforced using the default kernel `root_squash` mechanism.

The result was a fully operational, high-throughput network share. Testing confirmed that the remote client could perform persistent read/write operations without bypassing the administrative isolation controls. This deployment establishes a repeatable and secure framework for managing decentralized storage assets within enterprise networks.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 Network File System (NFS) Deployment

## 1.1 Project Description

The goal of this task was to develop technical proficiency in network storage architectures by implementing isolated file shares. The design ensures controlled storage synchronization between the discrete enterprise hosts.

This implementation demonstrates the following:

* **NFS Architecture Deployment:** Install and manage kernel-level NFS server and client services.
* **Identity Enforcement:** Implement default `root_squash` protections to restrict remote root access.
* **Persistent Mount Configuration:** Securely configure boot-persistent mounts using `/etc/fstab`.
* **Egress Access Management:** Restrict export permissions exclusively to approved client IP addresses.


## 1.2 Technical Execution

### 1.2.1 Environment and Initial Configuration

* **Infrastructure Scope:** Configuration executed across an isolated subnet:
  * **Storage Server:** `192.168.50.10` hosting `/mnt/nfs_share`
  * **Remote Client:** `192.168.50.20` mounting `/mnt/nfs_client_share`

* **Export Policy Enforcement:** Applied restricted host-based access rules within `/etc/exports`.

### 1.2.2 Directory Privileges and Mount Routing

* **Filesystem Initialization:** Created and prepared mount directories on both systems.
* **Privilege Alignment:** Applied temporary permissions using `sudo chmod 777 /mnt/nfs_share` to support write access for the anonymous account mapping enforced by `root_squash`.
* **Rule Synchronization:** Applied live export rules using `sudo exportfs -a` and refreshed client-side service definitions with `sudo systemctl daemon-reload`.

**Note:** Temporary write permissions were applied during validation testing to confirm correct NFS identity mappings. In production environments, ownership-based access controls and least-privilege permissions should be enforced instead of broad write-access permissions.
{: .notice}

```bash
# Example NFS export rule structure inside /etc/exports
/mnt/nfs_share 192.168.50.20(rw,sync,no_subtree_check)

# Persistent entry configured inside client /etc/fstab
192.168.50.10:/mnt/nfs_share /mnt/nfs_client_share nfs defaults 0 0

### Key Insight

NFS mounts require alignment between network export policies and the underlying filesystem permissions. Because the default `root_squash` security feature maps remote root operations to the anonymous `nobody:nogroup` identity, client write operations fail unless server-side permissions explicitly allow access to that unprivileged context.

## 1.3 Validation and Testing

A structured validation process confirmed correct rule enforcement and operational behavior across the network link:

- **Service Verification:** Used `sudo exportfs -v` to validate active export parameters (`rw`, `sync`, `no_subtree_check`).
- **Mount Verification:** Executed `sudo mount -a` to confirm `/etc/fstab` integrity and boot persistence before restarting the test.
- **Write Verification:** Created `/mnt/nfs_client_share/client_data` directly from the client system.
- **Identity Tracking:** Verified ownership mappings with `ls -l`, confirming that files were created under the expected `nobody:nogroup` identity.

## 1.4 Troubleshooting Highlights

- **Root Privilege Barrier:** Initial client write operations returned `"Permission denied"` errors despite using `sudo`. Root cause analysis confirmed that `root_squash` was functioning correctly. This issue was resolved by aligning the server-side file system permissions with the anonymous account context.
- **Mount Loop Prevention:** Prevented boot-time mount failures by validating `/etc/fstab` entries using `mount -a` before reboot-testing.

### Tool Mapping

| Function | Native Command / Path | Verification Indicator |
|---|---|---|
| **Export Policy Definition** | `/etc/exports` | Scoped single-IP client binding |
| **Live Rule Broadcast** | `sudo exportfs -a` | Updates active kernel export table |
| **Persistent Mapping Table** | `/etc/fstab` | Static mount configuration |
| **System Cache Refresh** | `sudo systemctl daemon-reload` | Reloads service configuration |
| **Live Mount Verification** | `mount -a` / `df -h` | Confirms active mounted state |

# 2.0 CONCLUSION

## 2.1 Key Takeaways

- NFS functionality depends on the alignment between network export rules and filesystem permissions.
- Default identity-squashing protections help prevent remote administrative escalation.
- Mount validation routines reduce reboot failures caused by invalid-storage configurations.
- Performance options such as `sync` and `no_subtree_check` improve operational efficiency and consistency.

## 2.2 Security Implications and Recommendations

### Risk: Unauthorized Lateral Movement via Over-Permissive Exports
Broad subnet exports or disabled identity protection can allow unauthorized hosts to access or modify shared storage.

### Mitigation:

- Restrict exports to approved IP addresses, whenever possible.
- Avoid using `no_root_squash` in production environments.

### Risk: Data Exposure in Transit
Standard NFS traffic is unencrypted and vulnerable to interception on untrusted networks. Humanity really looked at plaintext network storage and said, “ship it.”

### Mitigation:

- Isolate the storage traffic within secured network segments.
- Use Kerberos-based authentication (`sec=krb5`) when handling sensitive data.

### Best Practices

- Validate mount configurations using `mount -a` before rebooting the systems.
- Separate storage shares from privileged administrative accounts.
- Regularly review access logs for abnormal connection activity or unauthorized access attempts.

### Framework Alignment

- **NIST CSF (PR.DS-1):** Protection of data at rest and in transit.
- **CIS Control 3:** Data protection and access control enforcement.
- **ISO 27001 Annex A:** Security controls for storage access and network isolation.
