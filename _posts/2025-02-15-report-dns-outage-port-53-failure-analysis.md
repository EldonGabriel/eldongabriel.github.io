---
title: "REPORT – DNS Outage and Port 53 Failure Analysis – v1.0.1"
date: 2025-02-15
author: Eldon Gabriel
categories: [Networking]
tags: [Networking, DNS, Troubleshooting, ICMP, Incident Response]
excerpt: "Investigation of a DNS outage caused by UDP port 53 failure and ICMP error responses."
image:
  path: /assets/images/posts/dns-outage.png
  thumbnail: /assets/images/posts/dns-outage.png
---

# 0.0 Executive Summary

This report investigates a DNS outage affecting the public domain `www.yummyrecipesforme.com`. The goal was to find out why users could not access the website. The issue caused “destination port unreachable” errors when systems tried to contact the DNS server at `203.0.113.2`.

The result showed that UDP port 53 was not responding. Packet analysis and ICMP errors confirmed that the DNS service was not running or was blocked. This report recommends using backup DNS servers and monitoring tools to prevent future outages.

 

# 1.0 DNS Failure Investigation

## 1.1 Project Description

The goal of this task was to identify why DNS resolution failed and to understand how it impacted system access.

The approach used network traffic analysis to:

- **Understand how DNS works** by reviewing how queries use UDP port 53
- **Find the failure point** by checking for missing responses and error messages
- **Improve monitoring** by documenting the issue for future alerting

This ensures that systems depending on DNS, like websites, remain available and can be monitored properly.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on finding where the DNS request failed using packet-level analysis.

**Key Actions & Observations**

* **Traffic Monitoring:**
  - Used tools like `tcpdump` to capture traffic going to `203.0.113.2`

* **Error Identification:**
  - Found repeated **ICMP Type 3 Code 3 (Port Unreachable)** messages
  - This showed the server was reachable, but the DNS service was not running on UDP port 53

* **Impact Analysis:**
  - DNS requests failed, so users could not reach the website
  - Even if the web server was online, it could not be found without DNS

* **Root Cause:**
  - DNS service likely crashed, was misconfigured, or blocked by a firewall
  - The server rejected requests instead of ignoring them

 

## 1.3 Resolution and Validation

The issue was confirmed through testing and packet analysis.

| Parameter | Value |
| :--- | :--- |
| Primary DNS IP | 203.0.113.2 |
| Service Port | UDP 53 |
| Error Type | ICMP Port Unreachable |
| Scope | Public DNS Resolution |

**Validation Steps**

1. **DNS Testing:**
   - Used `dig` and `nslookup`
   - No DNS records were returned

2. **Packet Analysis:**
   - Every DNS request triggered an ICMP error
   - Confirmed the port was actively rejecting traffic

3. **Configuration Review:**
   - Found no backup DNS server configured
   - This made the outage worse

 

# 2.0: CONCLUSION

## 2.1 Key Takeaways

- DNS must be available for websites to work; if port 53 fails, access is lost
- ICMP errors help identify if a service is down or just unreachable
- Tools like `dig` and packet capture are critical for troubleshooting
- Backup DNS servers are required to prevent total outages

 

## 2.2 Security Implications & Recommendations

**Risk: Single Point of Failure in DNS**  
Using only one DNS server means a single failure causes full outage.  
**Mitigation:** Use multiple DNS servers in different locations.

**Risk: No Monitoring on DNS Services**  
DNS failures may go unnoticed until users report issues.  
**Mitigation:** Set up real-time monitoring and alerts for port 53.

**Best Practices**

- Test DNS regularly using automated tools
- Use centralized control for DNS configurations
- Check firewall rules to ensure port 53 is open
- Keep logs and packet captures for incident review

**Framework Alignment**

- Supports **NIST CSF PR.DS (Data Security and Availability)**
- Supports **DE.CM (Continuous Monitoring)**
- Aligns with best practices for maintaining critical network services
