---
title: "REPORT – Monitoring Linux System Resources (CPU & Memory) – v1.0.0"
date: 2026-05-06
author: Eldon Gabriel
categories: [Infrastructure and Systems]
tags: [Linux, Performance Monitoring, CPU, Memory, System Administration, Troubleshooting]
excerpt: "Technical implementation of Linux system resource monitoring using native command-line utilities to analyze CPU, memory, and swap usage."
image:
  path: /assets/images/posts/monitoring-linux-system.png
  thumbnail: /assets/images/posts/monitoring-linux-system.png
---

# 0.0 Executive Summary

This report documents the implementation and analysis of system resource monitoring on an Ubuntu Server environment.

The objective was to monitor CPU, memory, and swap usage using Linux command-line tools. The project focused on using native utilities to collect real-time performance information and validate system resource availability.

Several monitoring tools were tested in both interactive and logging modes to improve troubleshooting visibility and establish a baseline for normal system performance.

The result was a validated monitoring workflow that supports system administration, troubleshooting, capacity planning, and security monitoring.

 

# 1.0 Monitoring System Resources

## 1.1 Project Description

The goal of this task was to develop practical skills in monitoring Linux system performance and identifying resource-related issues before they affect system stability.

The implementation used multiple Linux monitoring tools to:

* Monitor CPU and memory usage in real time
* Identify processes consuming excessive resources
* Analyze system load averages
* Validate total available memory and swap space
* Generate readable outputs for troubleshooting and reporting

The project also demonstrated how monitoring tools can assist administrators during performance incidents and security investigations.

 

## 1.2 Technical Task / Troubleshooting Process

The process focused on collecting and validating system performance data using native Linux utilities.

### Key Actions and Observations

* **Memory Utilization Monitoring**
    * Used `free -h -t` to display human-readable memory statistics, including RAM and swap totals
    * Used `cat /proc/meminfo` to review raw kernel memory information for manual validation

* **CPU and Process Monitoring**
    * Used `top` to identify processes consuming high CPU and memory resources
    * Used `top -u` to filter processes by specific users
    * Used `top -b -n 1` to capture system snapshots and redirect output into `system_health.log`

* **Load Average Analysis**
    * Used `uptime` to analyze 1, 5, and 15-minute system load averages
    * Compared load values against available CPU cores to determine system stress levels

* **Virtual Memory Monitoring**
    * Used `vmstat -w` to review virtual memory statistics using wide-format output
    * Verified that wide mode prevented column formatting issues on larger terminal displays

* **Hardware Validation**
    * Used `lscpu` to confirm CPU architecture, available cores, and thread allocation

### Troubleshooting Highlights

* **Manual Calculation Complexity**
    * Raw values from `/proc/meminfo` were difficult to interpret quickly because memory values were displayed in kilobytes
    * This issue was resolved using `free -h -t`, which automatically converts values into human-readable units

* **Display Formatting Issues**
    * Standard `vmstat` output produced compressed columns on wider systems
    * This issue was corrected using the `-w` flag to improve readability

 

## 1.3 Resolution and Validation

The monitoring configuration was validated by checking command accuracy and confirming successful log generation.

| Parameter | Configuration Value |
| :--- | :--- |
| **Primary Monitoring Tools** | top / free |
| **Output Format** | Human-Readable (-h) |
| **Logging Configuration** | Batch Mode (-b) |
| **Monitoring Scope** | Real-Time System Performance |

### Validation Steps

1. **Memory Validation**
   * Verified that `free -h -t` correctly displayed RAM and swap totals
   * Compared results against values from `/proc/meminfo`

2. **Logging Validation**
   * Confirmed that `top -b -n 1` successfully generated a process snapshot inside `system_health.log`

3. **CPU Validation**
   * Verified using `lscpu` that the operating system correctly recognized assigned CPU cores and threads

4. **System Load Validation**
   * Compared load averages from `uptime` against active processes identified in `top`

 

# 2.0 CONCLUSION

## 2.1 Key Takeaways

* Human-readable flags such as `-h` improve the speed and accuracy of system analysis
* Batch mode (`-b`) is necessary for automated logging and historical monitoring
* Monitoring data should always be validated against known hardware specifications
* System monitoring must include both overall system load and individual process analysis
* Native Linux monitoring utilities provide sufficient visibility for most baseline troubleshooting tasks

 

## 2.2 Security Implications and Recommendations

### Risk: Resource Exhaustion (Denial of Service)

Unmonitored processes can consume excessive CPU or memory resources, causing system instability or service interruption.

**Mitigation**
* Configure automated monitoring snapshots using cron jobs
* Monitor swap usage and sustained high CPU utilization
* Establish baseline performance thresholds

### Risk: Compromised User Activity

Compromised accounts may execute unauthorized background processes such as cryptominers or resource abuse scripts.

**Mitigation**
* Use `top -u` and `ps -u` during routine audits
* Monitor unexpected spikes in per-user resource consumption
* Review long-running or hidden processes regularly

### Best Practices

* Use consistent measurement units during reporting and analysis
* Automate performance snapshots using scheduled tasks
* Establish baseline system performance values
* Validate hardware resource allocation after infrastructure changes
* Maintain historical monitoring logs for troubleshooting and incident response

### Framework Alignment

* **NIST CSF (DE.CM):** Continuous monitoring supports detection of abnormal system behavior
* **CIS Control 12:** Monitoring infrastructure performance improves system availability and operational awareness
* **ISO 27001 A.12.1.3:** Capacity management requires monitoring and adjustment of system resources
