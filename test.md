---
title: "Operational Approach"
layout: home
title: Security Systems Specialist
permalink: /test/
image:
  path: /assets/images/banner.png
---

<div class="report-box">

## 1.0: pfSense WebGUI Access Failure and Recovery

### 1.1 Project Description

This report documents a network accessibility issue where the pfSense WebGUI became unreachable from the Windows management host.

The objective of this task was to identify the root cause of the connectivity failure, restore administrative access, and validate proper network communication within a VirtualBox Internal Network lab environment.

The issue highlights the importance of correct IP configuration, interface management, and validation of Layer 3 and Layer 4 connectivity in a segmented lab network.

---

### 1.2 Network Troubleshooting and Access Restoration

The troubleshooting process focused on identifying why the pfSense management interface was no longer accessible.

Key actions performed:

- Verified Windows host IP configuration  
- Observed APIPA address assignment (169.254.x.x), indicating DHCP failure or misconfiguration  
- Identified that the management interface lacked a valid static IP assignment  
- Confirmed pfSense services were running:
  - Web service (HTTPS on port 443 / 8443)
  - Packet filtering (pf)  
- Checked firewall and service status using:
  - sockstat for listening services  
  - pfctl for firewall rules  
- Attempted connectivity tests using Test-NetConnection to validate Layer 4 reachability  
- Reviewed VirtualBox Internal Network configuration to ensure correct lab segmentation  

The root issue was determined to be incorrect client-side IP configuration, causing the Windows host to lose proper network alignment with the pfSense interface.

---

### 1.3 Network Reconfiguration and Validation

To restore connectivity, the following steps were performed:

- Reconfigured the Windows host network adapter using PowerShell  
- Assigned a static IP address:
  - **IP:** 172.16.0.10  
  - **Subnet:** /24  
- Ensured alignment with the pfSense LAN interface within the same subnet  
- Re-tested connectivity using Test-NetConnection for port 8443  
- Verified HTTPS access through browser connection to the pfSense WebGUI  
- Confirmed successful administrative login via the management interface  
- Validated optional SSH access over the internal network  

</div>
