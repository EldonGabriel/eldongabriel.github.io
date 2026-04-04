---
title: "REPORT – IP Subnetting Fundamentals – v1.0.0" 
date: 2025-08-26
author: Eldon Gabriel
categories: [Networking]
tags: [Networking, Subnetting, IPv4, Security Hardening, Network Segmentation] 
excerpt: "Implementation of structured IP subnetting to enable network segmentation, reducing the attack surface and improving access control."
image:
  path: "/assets/images/subnetting.png"
  thumbnail: "/assets/images/subnetting.png"
---

## 0.0 Executive Summary

This report explains the setup and improvement of network addressing using IP subnetting on a Class C network.

The goal was to reduce security risks such as unauthorized access and lateral movement by dividing the network into smaller, controlled segments.

The result is a more secure network design. Instead of one large network where all devices can easily communicate, the network is divided into smaller subnets. This improves control, visibility, and overall security.

 

# 1.0 IP Subnetting Fundamentals

## 1.1 Project Description

The purpose of this task was to create logical network boundaries to control traffic and reduce the impact of a security breach.

Subnetting was used with binary-to-decimal calculations and CIDR notation to:

* Create separate subnets for different groups of devices
* Limit unnecessary communication between systems
* Make firewall rules easier to apply and manage
* Improve tracking and visibility of IP address usage

This approach helps protect important systems by isolating them from general user traffic and reducing exposure to threats.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on identifying weaknesses in a default /24 network and improving it by dividing the address space into smaller subnets.

**Key Actions & Observations**

* Reviewed the default flat network design and identified limited isolation between devices
* Configured IPv4 addressing and subnet masks using CIDR ranges such as /25 to /29

Calculated network details including:

  * Network address
  * Broadcast address
  * Gateway address
  
* Reduced the number of available hosts in sensitive areas to limit potential attack paths
* Verified calculations using binary-to-decimal conversion
* Ensured CIDR prefix lengths were applied consistently
* Documented the configuration for reuse in future network expansion or VLAN design

**Root Cause:**
Default network setups are often flat and easy to configure, but they allow unrestricted communication between devices. This creates a higher security risk because attackers can move laterally across the network. Subnetting was used to fix this by dividing the network into smaller, controlled segments.

 

## 1.3 Resolution and Validation

The network was secured by applying correctly calculated subnet boundaries.

| Parameter       | Configuration Value        |
| :-------------- | :------------------------- |
| Management Tool | Subnet Calculation Methods |
| Control State   | Enabled                    |
| Security Mode   | Network Segmentation       |
| Scope           | Class C (/24) Baseline     |

**Validation Steps**

1. Calculated a /26 subnet to understand address distribution (64 total addresses)

2. Confirmed correct identification of:

   * Network address (first address in the range)
   * Broadcast address (last address in the range)

3. Verified that host addresses fall within the expected usable range

4. Checked that no IP conflicts or overlaps occurred

5. Confirmed normal system and application behavior after applying the subnet design

 

# 2.0 CONCLUSION

## 2.1 Key Takeaways

* Flat networks increase security risk due to unrestricted communication
* Subnetting improves security by dividing networks into smaller sections
* Proper calculations ensure correct network, broadcast, and host ranges
* Testing is required to confirm that configurations work as expected
* Subnetting helps balance security needs with system usability

 

## 2.2 Security Implications and Recommendations

**Risk: Large Attack Surface**
Flat networks allow attackers to scan and reach many systems if one device is compromised.

**Mitigation:** Use subnetting to separate systems into smaller, isolated network segments.

**Risk: Limited Traffic Monitoring**
Large broadcast domains make it harder to monitor traffic effectively.

**Mitigation:** Use smaller subnets to improve firewall rules and monitoring accuracy.

**Best Practices**

* Apply least privilege by placing sensitive systems in restricted subnets
* Use centralized tools like DHCP and IPAM to manage IP address assignments
* Always validate subnet configurations to prevent overlaps
* Maintain clear documentation for auditing and incident response

**Framework Alignment**

* Supports network segmentation best practices from NIST guidance (micro-segmentation concepts)
* Aligns with ISO 27001 controls for network segregation and protection
* Supports the NIST Cybersecurity Framework (Protect function) by limiting the impact of potential incidents through isolation
