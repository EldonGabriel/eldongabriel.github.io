---
title: "Computer Security and Systems Management"
layout: collection-item
slug: computer-security-systems-mgnt
collection: certifications
collection_item: true
order: 7
image:
  path: /assets/images/headers/section-header.png
  thumbnail: /assets/images/headers/section-header.png
  caption: "Enterprise Infrastructure & Security Engineering"
---

<div style="display: flex; justify-content: center;">

  <div class="carousel" style="position: relative; width: 100%; max-width: 800px; overflow: hidden;">
    
    <div class="slides" style="display: flex; transition: transform 0.5s ease;">

      <div class="slide" style="min-width: 100%; text-align: center;">
        <img src="/assets/certifications/UoC-Windows-Server-Management-Security.jpeg" alt="Windows Server Security" style="width: 100%; height: auto;">
      </div>

      <div class="slide" style="min-width: 100%; text-align: center;">
        <img src="/assets/certifications/UoC-Enterprise-System-Management-Security.jpg" alt="Enterprise System Security" style="width: 100%; height: auto;">
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

<hr style="border:1px solid rgba(255,255,255,0.0); margin:20px 0;">

<p>
  This specialization focuses on secure enterprise system administration across Windows and Linux environments, including infrastructure hardening, identity management, access control, and operational security practices used to support stable and secure business systems.
</p>

<p>
  Training emphasizes practical administration workflows, security-focused configuration management, and infrastructure governance aligned with enterprise’s operational requirements.
</p>

<p style="text-align:center; font-size: 1.1em; color: #fff; background: rgba(255,255,255,0.05); padding: 15px; border-radius: 8px;">
  <strong>Operational Capabilities:</strong> System Hardening · Identity Management · Enterprise Infrastructure Administration
</p>

<h4>Applied Capability</h4>
<ul>
  <li>Configured and secured Windows and Linux server environments within controlled lab infrastructures</li>
  <li>Implemented identity and access management concepts using Active Directory and group policy administration</li>
  <li>Applied security baselines and hardening practices across enterprise systems and services</li>
  <li>Performed configuration review and operational validation against security-focused administrative requirements</li>
</ul>

<h4>Operational Relevance</h4>
<p>
This certification supports infrastructure administration and security-focused operational support, including server configuration, access control, system hardening, and enterprise environment management. The skills developed through this training reinforce practical troubleshooting, secure administrative practices, and infrastructure reliability within business environments.
</p>
