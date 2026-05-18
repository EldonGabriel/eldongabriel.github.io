---
title: "REPORT – Linux Admin: Network Routing Fundamentals – v1.0.0"
date: 2026-05-17
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Networking, Linux, Routing, Troubleshooting, System Administration]
excerpt: "Technical implementation of host-based network routing, including gateway configuration and communication restrictions."
image:
  path: /assets/images/posts/lnrf.png
  thumbnail: /assets/images/posts/lnrf.png
---

# 0.0 Executive Summary

This report documents the configuration and management of network routing tables on a Linux system. Testing was performed in a controlled laboratory environment using systems within a `172.16.0.0/24` subnet. The objective was to modify the traffic flow to restrict outbound communication to a specific host while maintaining external connectivity via a default gateway.

The process involved auditing the existing routing table, configuring a default gateway for outbound traffic, and implementing a "reject" route. While the legacy `route` command was used for this exercise, modern Linux administration replaces these utilities with the `ip route` command (from the `iproute2` package).

The result is a validated network configuration in which outbound communication to a specific host is restricted at the kernel level. Traffic is rejected locally at the routing layer before the transmission. This demonstrates a lightweight traffic control method that reduces the attack surface for lateral movement and complements the firewall-based enforcement.

---

## 1.2 Technical Execution

### 1.2.1 Auditing the Network Path

- **Viewing the Table:** The command `route -n` displays the current routes. The `-n` flag prevents delays caused by DNS resolution.

- **Table Analysis:** The routing table reflected active flags, including
    - `UG` (Route is up and uses a gateway)
    - `!H` (Host is unreachable or explicitly rejected)

### 1.2.2 Modifying Traffic Flow

- **Restricting a Host:**
```bash
sudo route add -host 172.16.0.10 reject
````

This command enforces a local rule that drops the outbound traffic to the specified host.

* **Setting the Default Gateway:**

```bash
sudo route add default gw 172.16.0.1
```

This defines the primary route for traffic destined to locations outside the local subnet.

### Key Insight

Routing tables determine the next hop for outbound packets that leave the system. These changes are **temporary** and do not persist after rebooting. Persistent routes must be configured through network interface settings or services such as **Netplan** or **NetworkManager**.

---

## 1.3 Validation and Testing

A structured troubleshooting approach (Observation → Analysis → Action → Validation) was used.

1. **Table Verification:** `route -n`
   It was confirmed that both the default gateway and reject route were present in the kernel routing table.

2. **Rejection Validation:** `ping -c 4 172.16.0.10`
   Returned an **ICMP "Destination Unreachable"** response, confirming that the traffic was blocked locally.

3. **External Connectivity:** `ping -c 4 8.8.8.8`
   Successful replies confirmed that the outbound traffic was correctly routed through the default gateway.

---

## 1.4 Troubleshooting Highlights

* **Scope Limitation:** This control applies only to outbound traffic from the host and does not block inbound connections.
* **Performance Optimization:** DNS lookup delays were avoided using the `-n` flag for numerical output.

### Tool Mapping

| Function      | Legacy Tool | Modern Equivalent (iproute2) |
| ------------- | ----------- | ---------------------------- |
| View Routes   | `route -n`  | `ip route show`              |
| Modify Routes | `route add` | `ip route add`               |
| Verification  | `ping`      | `ping`                       |

---

## 2.2 Security Implications and Recommendations

**Risk: Unauthorized Lateral Movement**
Attackers often attempt to move between systems after gaining initial access.

**Mitigation:**

* Use reject routes to limit communication with sensitive or high-risk host systems.
* **Constraint:** This is a host-level control and should complement, not replace, firewall enforcement (e.g., `iptables`, `nftables`).

**Risk: Connectivity Disruption**
Incorrect routing entries can block legitimate traffic.

**Mitigation:**

* Verify routing tables immediately after the changes.
* Follow formal **change control** procedures and document configurations before and after modification.

**Best Practices**

* Use the `-n` flag for faster diagnosis.
* Validate connectivity after each change using `ping`.
* Ensure that critical routes are configured persistently to survive reboots.

**Framework Alignment**

* **NIST CSF (PR.AC):** Access control and traffic flow management
* **CIS Control 12:** Network infrastructure management
* **ISO 27001 (A.13):** Network service security
