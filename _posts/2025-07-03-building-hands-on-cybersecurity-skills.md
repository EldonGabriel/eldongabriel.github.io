---
title: "Building Hands-On Cybersecurity Skills: From MICS to MSAF with MCSI"
date: 2025-07-03
author: Eldon Gabriel
tags: [cybersecurity, MICS, MSAF, portfolio, hands-on, training]
excerpt: "MCSI labs provide scenario-based exercises that bridge IT fundamentals with advanced cybersecurity practices, building a portfolio of applied skills."
image:
  path: "/assets/images/msaf.png"
  thumbnail: "/assets/images/msaf.png"
--- 
My cybersecurity journey began with a mindset: don’t just collect theory—build skills that work in the real world.
That’s exactly what I found when I enrolled in the **MICS – Introduction to Cyber Security** course through Mossé Cyber Security Institute. After completing **_39 practical exercises_**, I’ve officially earned:

### My Certifications

<div class="slideshow-container">

  <!-- Slide 1 -->
  <div class="mySlides fade">
    <div class="numbertext">1 / 3</div>
    <img src="{{ '/assets/certifications/level1.png' | relative_url }}" style="width:100%">
    <div class="text">Figure 1: Cybersecurity Learner - Level 1. 2025. www.mosse-institute.com</div>
  </div>

  <!-- Slide 2 -->
  <div class="mySlides fade">
    <div class="numbertext">2 / 3</div>
    <img src="{{ '/assets/certifications/level2.png' | relative_url }}" style="width:100%">
    <div class="text">Figure 2: Cybersecurity Learner - Level 2. 2025. www.mosse-institute.com</div>
  </div>

  <!-- Slide 3 -->
  <div class="mySlides fade">
    <div class="numbertext">3 / 3</div>
    <img src="{{ '/assets/certifications/level3.png' | relative_url }}" style="width:100%">
    <div class="text">Figure 3: Cybersecurity Learner - Level 3. 2025. www.mosse-institute.com</div>
  </div>

</div>

<br>

<!-- Dots navigation -->
<div style="text-align:center">
  <span class="dot"></span> 
  <span class="dot"></span> 
  <span class="dot"></span> 
</div>

<style>
* {box-sizing: border-box;}
.mySlides {display: none;}
img {vertical-align: middle;}

/* Slideshow container */
.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
  border: 1px solid #ccc;
}

/* Caption text */
.text {
  color: #000;
  background: rgba(255, 255, 255, 0.8);
  font-size: 14px;
  padding: 8px 12px;
  position: absolute;
  bottom: 0;
  width: 100%;
  text-align: center;
}

/* Number text (1/3 etc) */
.numbertext {
  color: #000;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

/* The dots/bullets/indicators */
.dot {
  height: 12px;
  width: 12px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active {
  background-color: #717171;
}

/* Fading animation */
.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}
</style>

<script>
let slideIndex = 0;
showSlides();

function showSlides() {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  slideIndex++;
  if (slideIndex > slides.length) {slideIndex = 1}    
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
  setTimeout(showSlides, 3000); // Change image every 3 seconds
}
</script>


These certificates are more than titles—they’re earned through real labs, real tools, and real problem-solving. The MICS course helped me build foundational skills across multiple domains of cybersecurity and gave me the confidence to move into more advanced operations and system-level thinking.

<center><h2>What I Gained from MICS</h2></center>

The MICS experience was a one-of-a-kind **realistic cyber training** program. There were no pre-written answers—just open source curriculum and hands-on trial-and-error learning. This approach helped me develop real-world practical skills in key areas like:

### OSINT & Reconnaissance
- Created covert accounts and mindmaps from social media data  
- Used `dnsdumpster.com`, Shodan, and `dnstwist.py` to detect asset exposure and phishing campaigns  

### Vulnerability & Penetration Testing
- Performed **TCP/UDP** scans using **Nmap**  
- Ran web app scans using **Burp Suite Spider** and **Intruder**  
- Used **OpenVAS** to identify vulnerabilities in a virtual environment  

### Threat Hunting & Malware Detection
- Built **custom YARA rules** for identifying binaries and strings  
- Documented and tested rules to match professional standards  

### Digital Forensics
- Used **Dumpzilla** to analyze browser artifacts  
- Performed static malware analysis using **PEStudio** 

These exercises were supported by a focus on **professional writing and technical research**, sharpening both my technical and communication skills—critical for any analyst or engineer in the field.

<center><h2>Why I Chose to Enroll in MSAF</h2></center>

After earning my Level 3 certification and completing the MICS course, I knew it was time to dive deeper. That’s why I enrolled in **MSAF – System Administration Fundamentals**, a course designed to build mastery in the systems that power and secure enterprise environments.

I’ve attached my official **Confirmation of Enrolment** from Mossé Cyber Security Institute, verifying that I’m actively enrolled and progressing through the course.

<figure>
  <iframe src="{{ '/assets/certifications/msaf-confirmation-of-enrolment.pdf' | relative_url }}" 
          width="100%" 
          height="600px" 
          style="border:1px solid #ccc;">
  </iframe>
  <figcaption style="text-align:center;">Figure 4: MSAF - Confirmation of Enrolment. 2025. www.mosse-institute.com</figcaption>
</figure>

<center><h2>What MSAF Will Help Me Master</h2></center>

The MSAF course goes beyond concepts—it teaches how to **build, secure, and recover real systems**. Here’s a preview of what I’m working on:

### Virtualization
- Deploying virtual machines (VMs) in VirtualBox, VMware, GCP, and AWS  
- Creating snapshots and restoring safe system states  
- Installing and configuring VMware ESXi and managing via vSphere  

### Windows & Linux Hardening
- Creating and deploying GPOs to enforce password policies, exploit protection, UAC, and patch management  
- Locking down user rights, folders, and remote access  
- Securing _Windows Defender_ and configuring SMB and WinRM  

### Network Security & Firewalls
- Designing network architectures in Draw.io and Cisco Packet Tracer  
- Creating and testing firewall rules with pfSense  
- Secure VPN tunneling and traffic filtering  

### Backup & Recovery
- Using Duplicati and Windows tools to build backup and restoration workflows  
- Backing up and restoring Active Directory  
- Simulating server migrations from on-prem to cloud  

All of this work contributes to my **public portfolio**, showcasing not just theory—but evidence of capability.

<center><h2>Why This Matters</h2></center>

The cyber workforce doesn’t need more paper certs—it needs people who can **solve problems under pressure**.
By completing MICS and enrolling in MSAF, I’m reinforcing a **portfolio-first mindset** backed by tools, techniques, and repeatable results. 

From **YARA rules** to **GPO enforcement**, every step I take is documented and demonstrated for employers, collaborators, and mentors to see.
Whether I’m threat hunting, writing policy, or hardening a Windows server, my goal is the same: **deliver real, tested value**.


<center><h2>Final Thoughts</h2></center>

MCSI’s approach to cybersecurity training is unlike anything I’ve experienced. With every lab and report, I’m building the skills that matter in the field.

If you’re curious about how to level up in cybersecurity through hands-on work, feel free to connect—or check out my portfolio below.

<center><a href="https://students.mosse-institute.com/student/SB6kNYfrf4Z9gg4Zz8T5LixXI832" target="_blank">View My MCSI Portfolio</a></center>
