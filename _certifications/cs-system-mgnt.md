---
title: "Computer Security and Systems Management"
layout: collection-item
slug: cs-system-mgnt
collection: certifications
collection_item: true
order: 7
image:
  path: /assets/images/headers/uoc-cssms.png
  thumbnail: /assets/images/headers/uoc-cssms.png
  caption: "Enterprise Infrastructure & Security Engineering"
---

<div style="display: flex; justify-content: center;">

  <div class="carousel" style="position: relative; width: 100%; max-width: 800px; overflow: hidden;">
    
    <div class="slides" style="display: flex; transition: transform 0.5s ease;">

      <div class="slide" style="min-width: 100%; text-align: center;">
        <img src="/assets/certifications/UoC-Windows-Server-Management-Security.jpeg" alt="Slide 1" style="width: 100%; height: auto;">
        <p class="caption" style="margin-top: 8px; font-size: 0.9rem; opacity: 0.8;">
          UoC Windows System Management Security
        </p>
      </div>

      <div class="slide" style="min-width: 100%; text-align: center;">
        <img src="/assets/certifications/UoC-Enterprise-System-Management-Security.jpg" alt="Slide 2" style="width: 100%; height: auto;">
        <p class="caption" style="margin-top: 8px; font-size: 0.9rem; opacity: 0.8;">
          UoC Enterprise System Management Security
        </p>
      </div>

    </div>

    <div class="controls" style="position: absolute; top: 50%; width: 100%; display: flex; justify-content: space-between; transform: translateY(-50%);">
      <button onclick="prevSlide()" style="background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">‹</button>
      <button onclick="nextSlide()" style="background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">›</button>
    </div>

  </div>

</div>

<script>
let currentIndex = 0;

function showSlide(index) {
  const slides = document.querySelector(".slides");
  const totalSlides = document.querySelectorAll(".slide").length;

  if (index >= totalSlides) currentIndex = 0;
  else if (index < 0) currentIndex = totalSlides - 1;
  else currentIndex = index;

  slides.style.transform = `translateX(-${currentIndex * 100}%)`;
}

function nextSlide() {
  showSlide(currentIndex + 1);
}

function prevSlide() {
  showSlide(currentIndex - 1);
}
</script>

This specialization focuses on the high-level transition from home computing to **secure enterprise infrastructure**. My work in this program involves architecting, managing, and auditing complex systems to align with professional security standards and NIST-based best practices.

<p style="text-align:center; font-size: 1.1em; color: #fff; background: rgba(255,255,255,0.05); padding: 15px; border-radius: 8px;">
  <strong>Core Capabilities:</strong> Windows/Linux Server Hardening · Active Directory Security · Enterprise Auditing
</p>

#### **Professional Solutions & Value**
The competencies developed here allow me to deliver the following infrastructure services:
* **Infrastructure Design:** Architecting secure Windows and Linux server environments for business-critical operations.
* **Identity & Access Management:** Implementing robust Active Directory and GPO frameworks to enforce the Principle of Least Privilege.
* **Operational Integrity:** Developing automated patch management, system monitoring, and auditing workflows.
* **Resilience Planning:** Creating contingency and business continuity strategies to mitigate the impact of system failures.

#### **Technical Skill Summary**
* **Systems Administration:** Advanced management of Windows and Linux server fleets.
* **Network Architecture:** Engineering secure connectivity within virtualized environments.
* **Security Governance:** Aligning system configurations with organizational policies and compliance requirements.
* **Security Controls:** Deploying and auditing technical controls across diverse operating systems.

#### **Academic Progress**
<div style="background: rgba(255,255,255,0.02); padding: 20px; border-radius: 8px; border: 1px solid rgba(255,255,255,0.1);">
  <p><strong>Status:</strong> 2 of 4 Advanced Courses Completed</p>
  <ul style="list-style: none; padding-left: 0;">
    <li>✅ <strong>Enterprise System Management and Security</strong></li>
    <li>✅ <strong>Windows Server Management and Security</strong></li>
    <li>⏳ <strong>Linux Server Management and Security</strong> (In Progress)</li>
    <li>📅 <strong>Planning, Auditing, and Maintaining Enterprise Systems</strong> (Upcoming)</li>
  </ul>
</div>

***

#### **Operational Integration**
The expertise documented here directly informs my **System Hardening** and **Windows Administration** services. These standards ensure that every infrastructure project I handle is secure by design.

