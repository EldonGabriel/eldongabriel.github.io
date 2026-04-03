---
title: "Operational Approach"
layout: home
title: Security Systems Specialist
permalink: /test/
image:
  path: /assets/images/banner.png
---

# 0.0 Executive Summary
This report documents a restoration of administrative access to a pfSense firewall after a Windows management host lost connectivity due to an APIPA address assignment.

# 1.0: pfSense Access Failure and Recovery

## 1.1 Project Description
The objective of this task was to identify the root cause of the connectivity failure and restore access within a **VirtualBox Internal Network** lab environment. This scenario highlights the critical nature of Layer 3 (IP) alignment in segmented networks.

---

## 1.2 Technical Task / Troubleshooting Process
The process focused on diagnosing why the WebGUI was unreachable despite services running on the pfSense instance.

**Key Actions & Observations:**
* **Identified APIPA:** Windows host was showing `169.254.x.x`, confirming a DHCP failure.
* **Service Verification:** Confirmed HTTPS (Port 8443) and `pf` (Packet Filter) were active on pfSense using `sockstat`.
* **Rule Inspection:** Used `pfctl` to ensure the firewall wasn't dropping management traffic.
* **Segment Review:** Confirmed the VirtualBox adapter was correctly set to the "Internal Network" (LabNet).

**Root Cause:** The Windows host reverted to APIPA because it lacked a static IP to match the pfSense LAN subnet.

---

## 1.3 Resolution and Validation
Access was restored by manually aligning the host with the pfSense management subnet.

| Parameter | Configuration Value |
| :--- | :--- |
| **Static IP** | 172.16.0.10 |
| **Subnet Mask** | 255.255.255.0 (/24) |
| **Target Port** | 8443 (HTTPS) |

**Validation Steps:**
1.  **PowerShell:** Ran `Test-NetConnection -ComputerName 172.16.0.1 -Port 8443`.
2.  **Browser:** Successfully loaded the WebGUI and authenticated.
3.  **Service:** Confirmed SSH connectivity over the internal network.

---

## 2.0: CONCLUSION

### 2.1 Key Takeaways
* **APIPA is a red flag:** Always check for `169.254` when connectivity drops in a lab.
* **Layered Testing:** Validating Layer 3 (Ping) vs Layer 4 (Port check) prevents "ghost hunting" service failures.
* **Internal Networks:** VirtualBox Internal Networks require manual IP discipline since they lack a default DHCP server.

---

## 2.2 Security Implications & Recommendations

**Risk: Management Lockout** Misconfiguration of the LAN interface can lead to a total denial of service for administrators.  
**Mitigation:** Document all static assignments and maintain an out-of-band access method (Console/Serial).

**Risk: Validation Gaps** Assuming a service is "down" when the network is actually "misaligned" leads to wasted uptime.  
**Mitigation:** Use `sockstat` and `pfctl` locally on the appliance to verify service health before troubleshooting the wire.

---

## Appendix & Evidence
* **Figure 1:** Windows IP Config (APIPA Symptom)
* **Figure 2:** `sockstat` output confirming listeners
* **Figure 3:** Successful WebGUI login screen
