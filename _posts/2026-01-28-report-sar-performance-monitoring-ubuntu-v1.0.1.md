---
title: "REPORT – SAR Performance Monitoring on Ubuntu – v1.0.1"
date: 2026-01-28
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Linux, System Monitoring, SAR, Sysstat, Performance Analysis]
excerpt: "Implementation and analysis of system performance monitoring on Ubuntu using the System Activity Reporter (SAR) to identify resource bottlenecks and abnormal activity."
image:
  path: /assets/images/posts/sar-monitoring.png
  thumbnail: /assets/images/posts/sar-monitoring.png
---

# 0.0 Executive Summary
This report documents the installation, configuration, and utilization of the System Activity Reporter (SAR) on Ubuntu 24.04.3 LTS. The project successfully enabled continuous performance data collection, allowing for the granular monitoring of CPU, memory, disk I/O, and network interfaces. By establishing these monitoring capabilities, the system is better equipped to distinguish between normal operational baselines and potential security incidents or hardware failures indicated by abnormal resource consumption.


# 1.0 SAR Performance Monitoring on Ubuntu

## 1.1 Project Description
The objective of this task was to implement a robust performance monitoring solution using the `sysstat` utilities in a Linux environment. The project focused on configuring the System Activity Data Collector to capture historical and real-time metrics across all major hardware subsystems. This environment provides the necessary visibility for system administrators to perform root cause analysis on performance degradation and detect early indicators of compromise, such as data exfiltration or unauthorized resource mining.
 
## 1.2 Technical Task / Troubleshooting Process

### Tools & Commands

| Tool / Command | Purpose |
|----------------|--------|
| `apt install sysstat` | Install the sysstat package (includes SAR) |
| `systemctl enable --now sysstat` | Enable and start system activity data collection |
| `sar -u` | Monitor CPU usage |
| `sar -r` | Monitor memory usage |
| `sar -d` | Monitor disk activity |
| `sar -n DEV` | Monitor network interface statistics |

**Key Concepts:** Performance baselining, real-time vs. historical monitoring, resource utilization, and bottleneck identification.

**Key Actions & Observations**
* **Service Initialization:** Installed the `sysstat` package and modified the configuration to enable the cron-based data collector.

* **CPU Audit:** Utilized `sar -u` and `sar -P ALL` to monitor overall and per-core utilization, identifying how workloads are distributed across the processor.

* **Memory Tracking:** Observed RAM and swap space utilization to identify potential memory leaks or exhausted physical resources.

* **I/O and Network Analysis:** Monitored disk transfer rates and network packet volume to identify storage bottlenecks and abnormal traffic patterns.

**Root Cause:** Inactive performance monitoring was identified as a gap in system visibility, which was resolved by enabling the persistent background collection of the `sysstat` engine.

## 1.3 Resolution and Validation
Full performance visibility was achieved by confirming the successful generation of daily activity reports.

| Parameter | Configuration Value |
| :--- | :--- |
| **Operating System** | Ubuntu 24.04.3 LTS |
| **Monitoring Tool** | SAR (sysstat 12.7.4) |
| **Collection Interval** | Standard (via Cron) |
| **Data Retention** | Local Binary Logs |

**Validation Steps**
1. **Collector Check:** Verified that the `sysstat` service was active and the `ENABLED="true"` flag was set in the configuration.
2. **Command Validation:** Successfully executed `sar` commands to retrieve live and historical data for CPU, Disk, and Network interfaces.
3. **Log Review:** Confirmed that performance data was being successfully written to `/var/log/sysstat/`.
 

# 2.0: CONCLUSION

## 2.1 Key Takeaways
* **Baseline Importance:** Without active monitoring like SAR, it is difficult to distinguish between normal system spikes and malicious activity.

* **Subsystem Granularity:** Monitoring must cover multiple areas (CPU, Memory, Disk, Network) to provide a complete picture of system health.

* **Tool Consistency:** SAR provides a standardized interface for monitoring both real-time performance and historical trends on Linux systems.

## 2.2 Security Implications & Recommendations

**Risk: Undetected Resource Exhaustion** Malicious processes or misconfigured services can consume system resources, leading to a denial of service (DoS).  
**Mitigation:** Use SAR to establish performance baselines and integrate monitoring with alerting tools to catch abnormal resource spikes early.

**Risk: Data Exfiltration Visibility** High volumes of outbound network traffic or unusual disk I/O may indicate that sensitive data is being moved or encrypted.  
**Mitigation:** Regularly review SAR network and disk statistics to identify traffic patterns that deviate from the established organizational baseline.
