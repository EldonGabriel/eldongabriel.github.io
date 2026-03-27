---
title: "Active Directory Disaster Recovery with Bare Metal Restore"
date: 2026-02-12
author: Eldon Gabriel
tags: [Active Directory, Windows Server, Disaster Recovery, BMR, DSRM, System Administration, Cybersecurity]
excerpt: "Simulating a full Active Directory failure and restoring identity services using Bare Metal Recovery."
image:
  path: /assets/images/posts/active-directory.png
  thumbnail: /assets/images/posts/active-directory.png
---

<div style="text-align:center; margin-bottom:20px;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:6px; margin:0;">
    Exercise Core Function
  </h1>
</div>

<div style="display:grid; grid-template-columns:1fr; gap:20px; margin-bottom:40px; max-width:900px; margin-left:auto; margin-right:auto;">

  <div style="background:rgba(255,255,255,0.05); padding:20px; border-radius:8px; border:1px solid rgba(255,255,255,0.1);">
    
    <h3 style="text-align:center; margin-bottom:15px;">
            SOP – Active Directory Disaster Recovery & BMR – v1.0.1
    </h3>

    <!-- Responsive Video Wrapper -->
    <div style="position:relative; width:100%; padding-bottom:56.25%; height:0;">
      <iframe 
        src="https://www.youtube.com/embed/HjuZvKC1FSk?si=5-EhGvJkhdxyIJcP"
        style="position:absolute; top:0; left:0; width:100%; height:100%; border-radius:6px;"
        frameborder="0"
        allowfullscreen>
      </iframe>
    </div>

  </div>

</div>
This project shows how to recover an Active Directory (AD) environment after a full system failure. The system was restored on new hardware using Windows Server 2016. The goal was to restore domain services and system state to a fully operational condition.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Studied</h1>
</div>

This project focused on testing a full disaster recovery process for a Domain Controller (DC). It included creating a backup, simulating a failure, and restoring the system using Directory Services Restore Mode (DSRM).

The main focus was to ensure that Active Directory data and the SYSVOL folder were restored correctly and ready for use.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">What I Learned</h1>
</div>

**Full System Recovery with BMR**  

I used Bare Metal Recovery (BMR) to restore the entire system, including the operating system and Active Directory.

**Using DSRM for Safe Recovery**  

DSRM was used to restore the system without causing conflicts with other domain controllers.

**Restoring Critical Data**  

The System State was restored to recover important system data such as the registry, system files, and boot settings.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Why It Matters</h1>
</div>

If a Domain Controller fails, users cannot log in or access systems. A tested recovery plan ensures that services can be restored quickly.

Bare Metal Recovery allows the system to be rebuilt with all data intact, reducing downtime and preventing major disruptions.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">How It Maps to the Job / Framework</h1>
</div>

**System Administration Skills**  

This project builds skills in backup, recovery, and system restoration.

**Cybersecurity Practices**  

It supports disaster recovery planning and protection against threats like ransomware.

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Key Takeaways</h1>
</div>

1. **BMR Restores Everything:** Bare Metal Recovery restores the full system in one process.

2. **DSRM is Required for AD Recovery:** It allows safe recovery without interference from running services.

4. **Always Verify the System:** Check that DNS, Netlogon, and AD services are working after recovery.

6. **Test Before You Need It:** A recovery plan is only useful if it has been tested.

---

<div style="text-align:center;">
<h2 style="text-align:center; font-size:2.5em; margin-bottom:40px;">
Related Projects</h2>
</div>

<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap;">

<div style="max-width:500px; margin:0 auto; background:rgba(255,255,255,0.05); padding:12px; border-radius:10px; border:1px solid rgba(255,255,255,0.15); text-align:center;">

<iframe
src="{{ '/assets/guides/SOP – AD Disaster Recovery & Identity Restoration – v1.0.2.pdf' | relative_url }}"
width="100%"
height="680"
style="border:1px solid #333; border-radius:8px;">
</iframe>

<p style="margin-top:8px; color:#aaa; font-size:0.9em;">
<strong>SOP – AD Disaster Recovery & Identity Restoration – v1.0.2</strong>
</p>

</div>

</div>

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Technical Skills Demonstrated</h1>
</div>

- Active Directory backup and recovery  
- Windows Server administration (2016)  
- Bare Metal Recovery (BMR)  
- Directory Services Restore Mode (DSRM)  
- System State restoration  
- Disaster recovery planning and validation  

---

<div style="text-align:center;">
  <h1 style="display:inline-block; border-bottom:3px solid #fff; padding-bottom:4px;">Conclusion</h1>
</div>

This project showed how to recover a full Active Directory environment after a system failure. It improved my understanding of disaster recovery and system restoration.

It also showed that recovery is not complete until services are tested and confirmed to be working correctly.
