---
title: "Detecting System Anomalies with SAR"
date: 2026-01-28
author: Eldon Gabriel
tags: [Linux, System Monitoring, SAR, Sysstat, Performance Analysis]
excerpt: "A field note on using SAR to monitor system performance, establish baselines, and detect anomalies across CPU, memory, disk, and network resources."
image:
  path: /assets/images/posts/sar-monitoring.png
  thumbnail: /assets/images/posts/sar-monitoring.png
---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>

This exercise focused on using the System Activity Reporter (SAR) to monitor and analyze system performance on an Ubuntu 24.04.3 LTS server. The goal was to establish a performance baseline and understand how system resources behave under normal conditions.

**Tools & Commands:**  
`apt install sysstat`, `systemctl enable --now sysstat`, `sar -u`, `sar -r`, `sar -d`, `sar -n DEV`

**Key Concepts:**  
Performance baselining, real-time vs. historical monitoring, resource utilization, and bottleneck identification.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>

**Configuration Matters:**  
Installing `sysstat` is not enough. Historical data collection must be enabled in `/etc/default/sysstat` for SAR to provide meaningful insights.

**Resource Correlation:**  
High usage alone does not indicate a problem. CPU, memory, disk, and network metrics must be analyzed together to identify true bottlenecks.

**Behavior Over Time:**  
Historical SAR data is more useful than real-time snapshots when identifying trends, anomalies, and gradual system degradation.

**Operational Insight:**  
Resource spikes only become meaningful when analyzed in context with other system metrics.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>

In an enterprise environment, system monitoring is critical for both performance management and security visibility.

- Unexpected spikes in CPU or network activity may indicate malicious behavior such as cryptomining or data exfiltration.  
- Without monitoring, performance issues are often detected only after users are impacted.  
- SAR acts like a flight recorder, capturing system behavior over time for analysis before and after incidents.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job / Framework</h1>
</div>

**NICE Framework – System Administrator (SP-SYS-001):**  
Supports continuous system monitoring, performance tuning, and proactive issue detection.

**ASD Cyber Skills Framework – Systems Installation and Decommissioning (HSIN):**  
Reinforces establishing performance baselines and monitoring Linux system health.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>

- Historical data is more valuable than real-time output for detecting trends and anomalies.  
- Always correlate CPU, memory, disk, and network metrics before identifying bottlenecks.  
- Performance monitoring supports both system stability and security detection.  
- Establishing a baseline is essential for recognizing abnormal behavior.  

---

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<div style="max-width:500px; margin:0 auto; background:rgba(255,255,255,0.05); padding:12px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/guides/GUIDE – SAR Performance Monitoring on Ubuntu – v1.0.1.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:8px; color:#aaa; font-size:0.9em;">
<strong>REPORT – SAR Performance Monitoring on Ubuntu – v1.0.1</strong>
</p>

</div>

</div>
