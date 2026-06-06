---
title: "REPORT – Network Service Auditing and Hardening – v1.0.0"
date: 2026-06-04
author: Eldon Gabriel
categories: [Infrastructure Security]
tags: [Linux, Hardening, Network Security, Access Control, Security Hardening, System Administration]
excerpt: "Technical implementation of network service auditing and the disabling of insecure legacy protocols to reduce system attack surface."
image:
  path: /assets/images/posts/network-hardening.png
  thumbnail: /assets/images/posts/network-hardening.png
---

# 0.0 Executive Summary

This report documents an authorized security hardening project on a Linux system. The goal was to find and disable insecure network services that could allow unauthorized access to the system. 

The assessment focused on the Ubuntu Server 24.04 environment. The system was used to test network auditing and service management control. The process involved reviewing active network ports and turning off outdated services, such as FTP and Telnet.

The results show that these insecure services were successfully blocked from running. This demonstrates the importance of reducing the network footprint to maintain system security.

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

# 1.0 Network Service Auditing and Hardening

## 1.1 Project Description

The purpose of this task was to develop Linux administration and security auditing skills.

The work included:

* Checking the system for open network ports
* Identifying insecure and outdated network services
* Disabling the File Transfer Protocol (FTP) service
* Disabling Samba file-sharing services
* Disabling the super-server that runs Telnet and Rlogin

This process helps administrators to close unnecessary network openings before attackers can find them.

## 1.2 Technical Task / Troubleshooting Process

The assessment focused on reviewing active network connections and shutting down legacy services.

Key Actions and Observations
* Checked the Linux system for all active network ports and the listening services.
* Stopped and disabled the FTP service to prevent unencrypted file transfers.
* Samba file-sharing services were stopped and disabled.
* Telnet and Rlogin were still running after attempting to stop them directly.
* System controls were used to shut down the parent service that managed Telnet and Rlogin.
* Verified that all targeted services were fully stopped.

**Root Cause:** Telnet and Rlogin were managed by a parent service instead of running independently. Shutting down the parent service successfully closed these ports.

## 1.3 Resolution and Validation

The system was tested to confirm that the insecure network services were no longer active.

| Parameter | Configuration Value |
|---|---|
| Assessment Tool | Network Statistics and System Controls |
| Target Assets | Active Network Ports |
| Assessment Type | Security Hardening |
| Operating System | Ubuntu Server 24.04 |
| Disabled Services | FTP, Samba, Telnet, Rlogin |
| File Protection | Service Deactivation |

**Validation Steps**

1. The FTP port was verified to be closed and no longer accepting connections.
2. Samba file-sharing ports were closed.
3. Telnet and Rlogin were successfully disabled.
4. The system boot settings were checked to ensure that the services would not restart after a reboot.
5. Network statistics were reviewed to ensure that the system footprint was fully minimized.

# 2.0 CONCLUSION

## 2.1 Key Takeaways

* System hardening requires closing unnecessary network ports to reduce security risks.
* Simply stopping a service is insufficient; it must be disabled to prevent it from starting after a reboot.
* Legacy protocols send data in plaintext, making them unsafe for modern networks.
* Some services run under the parent framework and require different shutdown methods.

## 2.2 Security Implications and Recommendations

**Risk: Active Legacy Protocols**

Insecure services such as FTP and Telnet send passwords in plain text, increasing the risk of network interception.

**Recommendation:** Disable all cleartext protocols and replace them with secure alternatives like SSH.

**Risk: Improper Service Shutdowns**

Stopping a service without disabling it allows the service to return after a system restart, thereby leaving the system vulnerable.

**Recommendation:** Always update the system boot settings to permanently disable unneeded services.

**Best Practices**

* Regularly audit network ports to identify unauthorized services.
* Establish a secure baseline image for all the new servers.
* Disable all software that is not required for the server to function properly.
* Check the system logs to ensure that the disabled services remain inactive.

**Framework Alignment**

* Supports PCI-DSS and CIS Benchmark network security requirements.
* Aligns with standard access control and attack-surface reduction practices.

