---
title: "Cybersecurity Risk Management Framework"
layout: collection-item
slug: cybersecurity-risk-management-framework
collection: certifications
collection_item: true
order: 3
image:
  path: /assets/images/headers/section-header.png
  thumbnail: /assets/images/headers/section-header.png
  caption: "Mastering NIST Risk Management & Compliance"
---

<div style="display: flex; justify-content: center;">

  <div class="carousel" style="position: relative; width: 100%; max-width: 800px; overflow: hidden;">
    
    <div class="slides" style="display: flex; transition: transform 0.5s ease;">

      <div class="slide" style="min-width: 100%; text-align: center;">
        <img src="/assets/certifications/infosec-nist-cybersecurity-rmf.jpg"
             alt="Cybersecurity Risk Management Framework"
             style="width: 100%; height: auto;">
      </div>

      <div class="slide" style="min-width: 100%; text-align: center;">
        <img src="/assets/certifications/infosec-nist-800-171.jpg"
             alt="NIST 800-171"
             style="width: 100%; height: auto;">
      </div>

      <div class="slide" style="min-width: 100%; text-align: center;">
        <img src="/assets/certifications/infosec-nist-csf.jpg"
             alt="NIST Cybersecurity Framework"
             style="width: 100%; height: auto;">
      </div>

      <div class="slide" style="min-width: 100%; text-align: center;">
        <img src="/assets/certifications/infosec-nist-dod-rmf.jpg"
             alt="NIST DoD Risk Management Framework"
             style="width: 100%; height: auto;">
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

<p style="font-size:1.2em; line-height:1.6;">
  This specialization focuses on the NIST Risk Management Framework (RMF) and Cybersecurity Framework (CSF), emphasizing how governance and compliance requirements translate into practical security controls in operational environments.
</p>

<p style="font-size:1.2em; line-height:1.6;">
  Training reinforces structured risk analysis, security documentation, control validation, and security-focused decision-making, which are aligned with organizational risk management objectives.
</p>

<p style="text-align:center; font-size: 1.1em; color: #fff; background: rgba(255,255,255,0.05); padding: 15px; border-radius: 8px;">
  <strong>Operational Capabilities:</strong> Risk Assessment · Security Control Mapping · Compliance Support
</p>

<h4>Applied Capability</h4>
<ul>
  <li>Mapped technical and administrative safeguards to NIST 800-53 control families</li>
  <li>Performed structured risk assessments across systems and operational environments</li>
  <li>Developed compliance-oriented documentation aligned with RMF lifecycle processes</li>
  <li>Translated governance and policy requirements into practical security control considerations</li>
</ul>

<h4>Operational Relevance</h4>
<p>
This certification supports governance, risk, and compliance workflows involving security assessments, policy alignments, control implementations, and operational risk evaluations. The skills developed through this training strengthen security-focused decision-making and structured documentation practices across business and infrastructure environments.
</p>
