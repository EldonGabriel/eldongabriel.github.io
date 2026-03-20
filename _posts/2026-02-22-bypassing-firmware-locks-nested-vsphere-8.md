---
title: "Bypassing Firmware Locks for Nested vSphere 8 on Ryzen 6000"
date: 2026-02-22
author: Eldon Gabriel
tags: [Virtualization, VMware, AMD, Troubleshooting, Infrastructure]
excerpt: "A technical deep-dive into enabling nested virtualization on restricted AMD mobile platforms by bypassing OEM firmware locks and Windows 11 VBS."
image:
  path: /assets/images/posts/vsphere-amd-lab.png
  thumbnail: /assets/images/posts/vsphere-amd-lab.png
---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Exercise Core Function</h1>
</div>

Modern AMD Ryzen 6000 laptops often ship with firmware that hides virtualization features from hypervisors. Although the CPU supports AMD-V (SVM), the system may not expose it properly. When this is combined with Windows 11 Virtualization-Based Security (VBS), running a nested ESXi 8.0U3e lab becomes very difficult.

### Key Technical Hurdles

* **Hidden BIOS Settings:** Standard F2 BIOS menus often hide SVM and SMM options on consumer laptops, such as the Acer Nitro V15.
* **Windows Hypervisor Conflict:** Windows VBS loads its own hypervisor. This prevents VMware Workstation from using AMD-V directly.
* **Driver Misalignment:** Default Windows drivers may not properly coordinate the AMD Platform Management Framework (PMF), which can cause unstable nested virtualization.

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">The Engineering Solution</h1>
</div>

By using a hidden UEFI key sequence (**Fn + Tab**) and disabling Credential Guard with the DG Readiness Tool, access to AMD-V was restored for VMware Workstation Pro 17.6. This enabled nested virtualization to function correctly.

> **Validation Logic:** Success was confirmed when `systeminfo.exe` showed **“Virtualization Enabled in Firmware: Yes”** and the output **did not** show “A hypervisor has been detected.” This confirmed that Windows no longer blocks VMware from accessing hardware virtualization.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Full Technical Guide (PDF)</h1>
</div>

The complete end-to-end procedure is documented in the full report. It includes:
* Firmware configuration steps
* OS-level changes
* Recovery procedures (CMOS/NVRAM Reset)
* Post-lab security restoration

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<!-- Project -->
<div style="flex:0 1 500px; background:rgba(255,255,255,0.05); padding:20px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/guides/GUIDE – Building a vSphere 8 Nested Lab on AMD Ryzen 6000 – v1.0.0.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:12px; color:#aaa;">
<strong>GUIDE – Building a vSphere 8 Nested Lab on AMD Ryzen 6000 – v1.0.0</strong>
</p>

</div>

</div>

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Technical Skills Demonstrated</h1>
</div>

* **Hardware:** UEFI configuration and SMM security changes.
* **Operating System:** Windows Boot Configuration Data (BCD) modification.
* **Hypervisor:** Nested ESXi configuration (vSphere 8.x).
* **Capacity Planning:** Designing a 32GB RAM allocation model to support stable VCSA deployment.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Conclusion</h1>
</div>

With the platform successfully de-provisioned of VBS and the AMD-V extensions reclaimed, the environment is now prepared for Level 2 operations, including cross-cloud migration testing with AWS MGN.
