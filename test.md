---
title: "Operational Approach"
layout: home
title: Security Systems Specialist
permalink: /test/
image:
  path: /assets/images/banner.png
---

## 1.0: pfSense WebGUI Access Failure and Recovery

### 1.1 Project Description

This report documents a network accessibility issue where the pfSense WebGUI became unreachable from the Windows management host.

The objective of this task was to identify the root cause of the connectivity failure, restore administrative access, and validate proper network communication within a VirtualBox Internal Network lab environment.

The issue highlights the importance of correct IP configuration, interface management, and validation of Layer 3 and Layer 4 connectivity in a segmented lab network.

---

### 1.2 Network Troubleshooting and Access Restoration

The troubleshooting process focused on identifying why the pfSense management interface was no longer accessible.

Key actions performed:

<ul>
  <li>Verified Windows host IP configuration</li>
  <li>Observed APIPA address assignment (169.254.x.x), indicating DHCP failure or misconfiguration</li>
  <li>Identified that the management interface lacked a valid static IP assignment</li>
  <li>Confirmed pfSense services were running:
    <ul>
      <li>Web service (HTTPS on port 443 / 8443)</li>
      <li>Packet filtering (pf)</li>
    </ul>
  </li>
  <li>Checked firewall and service status using:
    <ul>
      <li>sockstat for listening services</li>
      <li>pfctl for firewall rules</li>
    </ul>
  </li>
  <li>Attempted connectivity tests using Test-NetConnection to validate Layer 4 reachability</li>
  <li>Reviewed VirtualBox Internal Network configuration to ensure correct lab segmentation</li>
</ul>

The root issue was determined to be incorrect client-side IP configuration, causing the Windows host to lose proper network alignment with the pfSense interface.

---

### 1.3 Network Reconfiguration and Validation

To restore connectivity, the following steps were performed:

<ul>
  <li>Reconfigured the Windows host network adapter using PowerShell</li>
  <li>Assigned a static IP address:
    <ul>
      <li><strong>IP:</strong> 172.16.0.10</li>
      <li><strong>Subnet:</strong> /24</li>
    </ul>
  </li>
  <li>Ensured alignment with the pfSense LAN interface within the same subnet</li>
  <li>Re-tested connectivity using Test-NetConnection for port 8443</li>
  <li>Verified HTTPS access through browser connection to the pfSense WebGUI</li>
  <li>Confirmed successful administrative login via the management interface</li>
  <li>Validated optional SSH access over the internal network</li>
</ul>

---

### 1.4 Optional Deep Dive / Special Case

During troubleshooting, the presence of an APIPA address indicated that the Windows interface attempted DHCP but failed to obtain a lease.

This typically occurs when:

<ul>
  <li>DHCP is unavailable on the network</li>
  <li>Static configuration conflicts with automatic settings</li>
  <li>Virtual network adapters are misconfigured or mismatched</li>
</ul>

The VirtualBox Internal Network requires consistent manual IP configuration since it does not inherently provide DHCP services unless explicitly configured within pfSense.

---

### 1.5 Additional or Supporting Work

Supporting validation steps included:

<ul>
  <li>Verification of listening services on pfSense</li>
  <li>Confirmation of firewall rules allowing HTTPS traffic</li>
  <li>Cross-checking interface assignment and subnet consistency</li>
  <li>Network isolation validation within the VirtualBox Internal Network (LabNet)</li>
  <li>Connectivity testing across Layer 3 (IP reachability) and Layer 4 (TCP port access)</li>
</ul>

---

## 2.0: CONCLUSION

### 2.1 Key Takeaways

<ul>
  <li>Incorrect or missing IP configuration can break administrative access even when services are functioning correctly</li>
  <li>APIPA addressing is a strong indicator of network misconfiguration or DHCP failure</li>
  <li>Layered troubleshooting (Layer 3 and Layer 4 validation) is essential in diagnosing connectivity issues</li>
  <li>Static IP consistency is critical in isolated lab environments such as VirtualBox Internal Networks</li>
  <li>Verification tools like Test-NetConnection, sockstat, and pfctl are effective for confirming service availability and firewall status</li>
</ul>

---

### 2.2 Security Implications and Recommendations

This incident highlights several security and operational considerations:

**Risk: Loss of Administrative Access**  
Misconfiguration of management interfaces can result in denial of access to critical infrastructure.  
**Mitigation:** Maintain documented network configurations and static addressing schemes for management systems.

**Risk: Misaligned Network Segmentation**  
Incorrect interface configuration can unintentionally isolate systems.  
**Mitigation:** Enforce consistent IP schema across lab and production environments.

**Risk: Service Exposure and Validation Gaps**  
Without validating listening services and firewall rules, administrators may incorrectly assume service failure.  
**Mitigation:** Regularly verify services using diagnostic tools such as sockstat and firewall inspection commands.

---

### Best Practices

<ul>
  <li>Implement strict IP addressing standards for management networks</li>
  <li>Use controlled DHCP only where appropriate and expected</li>
  <li>Validate connectivity using both Layer 3 and Layer 4 tests during troubleshooting</li>
  <li>Maintain separation of management and user traffic in segmented networks</li>
  <li>Apply least privilege principles to firewall rules governing administrative access</li>
</ul>

---

### Framework Alignment

This work aligns with general network configuration management and access control principles consistent with structured security frameworks. It supports secure system administration practices by enforcing predictable and auditable network states.

---

## Appendix

**Figures**
<ul>
  <li>**Figure 1:** Windows host IP configuration showing APIPA address assignment</li>
  <li>**Figure 2:** pfSense interface and service validation outputs</li>
  <li>**Figure 3:** Successful WebGUI access via HTTPS on port 8443</li>
</ul>

**Supporting Evidence**
<ul>
  <li>PowerShell connectivity tests (Test-NetConnection)</li>
  <li>pfSense service checks (sockstat)</li>
  <li>Firewall inspection (pfctl)</li>
  <li>VirtualBox network configuration (Internal Network: LabNet)</li>
</ul>
