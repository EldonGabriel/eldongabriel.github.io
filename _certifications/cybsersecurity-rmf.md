---
title: "Cybersecurity RMF"
layout: collection-item
slug: cybersecurity-rmf
collection: certifications
collection_item: true
order: 3
image:
  path: /assets/images/headers/section-header.png
  thumbnail: /assets/images/headers/section-header.png
  caption: "Mastering NIST Risk Management & Compliance"
---

<div class="certificate-carousel" style="text-align: center; margin: 20px auto; max-width: 600px;">

  <div class="carousel-slide">
    <img src="/assets/certifications/infosec-nist-cybersecurity-rmf.jpg"
         alt="Cybersecurity Risk Management Framework"
         style="width: 100%; height: auto; border-radius: 8px;">
    <p>Cybersecurity Risk Management Framework</p>
  </div>

  <div class="carousel-slide">
    <img src="/assets/certifications/infosec-nist-800-171.jpg"
         alt="NIST 800-171"
         style="width: 100%; height: auto; border-radius: 8px;">
    <p>NIST 800-171</p>
  </div>

  <div class="carousel-slide">
    <img src="/assets/certifications/infosec-nist-csf.jpg"
         alt="NIST Cybersecurity Framework"
         style="width: 100%; height: auto; border-radius: 8px;">
    <p>NIST Cybersecurity Framework</p>
  </div>

  <div class="carousel-slide">
    <img src="/assets/certifications/infosec-nist-doD-rmf.jpg"
         alt="NIST DoD Risk Management Framework"
         style="width: 100%; height: auto; border-radius: 8px;">
    <p>NIST DoD Risk Management Framework</p>
  </div>

  <button onclick="changeCertificate(-1)">&#10094;</button>
  <button onclick="changeCertificate(1)">&#10095;</button>

</div>

<script>
  let certificateIndex = 0;
  const certificates = document.querySelectorAll(".carousel-slide");

  function showCertificate(index) {
    certificates.forEach(slide => slide.style.display = "none");

    if (index >= certificates.length) {
      certificateIndex = 0;
    }

    if (index < 0) {
      certificateIndex = certificates.length - 1;
    }

    certificates[certificateIndex].style.display = "block";
  }

  function changeCertificate(direction) {
    certificateIndex += direction;
    showCertificate(certificateIndex);
  }

  showCertificate(certificateIndex);
</script>

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
