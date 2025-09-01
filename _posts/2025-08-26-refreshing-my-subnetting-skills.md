---
title: "Refreshing My Subnetting Skills: From Handwritten Notes to a Full Class C Subnet Report"
date: 2025-08-26
author: Eldon Gabriel
tags: [Subnetting, Networking, Cybersecurity, ISC2]
excerpt: "Turning my old handwritten subnet notes into a complete Class C subnet report and a useful reference for labs and exercises."
image:
  path: "/assets/images/subnetting.png"
  thumbnail: "/assets/images/subnetting.png"
---

While reviewing my old handwritten notes from my ISC² CC exam prep, I found a section where I had written out subnet ranges for Class C networks. It reminded me of late-night study sessions and the challenge of memorizing network and host address ranges.

I realized this was a good chance to refresh my memory and practice subnetting in a hands-on way. I decided to turn those notes into a full, structured report—a reference I could use for future labs, exercises, and real-world projects.

---

## <center>From Handwritten Notes to Subnet Reference</center>

**Focus:** Class C subnets /25–/29  

My report includes a complete table of subnet addresses, usable hosts, and broadcast addresses for the `192.168.1.0/24` network. The math follows standard formulas:

- **Subnet increment** = 2<sup>n</sup>  
- **Usable hosts per subnet** = 2<sup>n</sup> – 2
- **Note:** _n_ = number of host bits

Each subnet now has a network address, first and last usable hosts, and broadcast address—making it easy to reference when designing networks or completing exercises.

---

## <center> Handwritten Notes</center>

I wanted to include my original ISC² CC exam prep notes. These images show how I manually calculated and wrote out the subnets.  

<table>
  <thead>
    <tr>
      <th style="text-align:center;">Screenshot</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center;">
        <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/subnetting-and-cidr-notation-1..JPG" alt="Subnetting Notes" width="200"><br>
        <strong>Figure 1</strong>
      </td>
      <td>Subnetting and CIDR Notation Notes screenshot. 2025.</td>
    </tr>
    <tr>
      <td style="text-align:center;">
        <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/private-ip-address-ranges-binary-conversion_2.JPG" alt="Private IP Notes" width="200"><br>
        <strong>Figure 2</strong>
      </td>
      <td>Private IP Address Ranges Notes screenshot. 2025.</td>
    </tr>
    <tr>
      <td style="text-align:center;">
        <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/subnetting-breakdown-reference-table-3.JPG" alt="Subnet Table Notes" width="200"><br>
        <strong>Figure 3</strong>
      </td>
      <td>Subnetting Breakdown Reference Table Notes screenshot. 2025.</td>
    </tr>
    <tr>
      <td style="text-align:center;">
        <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/25-26-subnet-calculations-4.JPG" alt="/25 and /26 Notes" width="200"><br>
        <strong>Figure 4</strong>
      </td>
      <td>/25 and /26 Subnet Calculations Notes screenshot. 2025.</td>
    </tr>
    <tr>
      <td style="text-align:center;">
        <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/26-subnet-address-ranges-5.jpg" alt="/26 Notes" width="200"><br>
        <strong>Figure 5</strong>
      </td>
      <td>/26 Subnet Address Ranges Notes screenshot. 2025.</td>
    </tr>
    <tr>
      <td style="text-align:center;">
        <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/27-subnet-address-ranges-6.JPG" alt="/27 Notes" width="200"><br>
        <strong>Figure 6</strong>
      </td>
      <td>/27 Subnet Address Ranges Notes screenshot. 2025.</td>
    </tr>
    <tr>
      <td style="text-align:center;">
        <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/28-subnet-address-ranges-7.JPG" alt="/28 Notes" width="200"><br>
        <strong>Figure 7</strong>
      </td>
      <td>/28 Subnet Address Ranges Notes screenshot. 2025.</td>
    </tr>
    <tr>
      <td style="text-align:center;">
        <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/29-subnet-address-ranges-8.JPG" alt="/29 Notes" width="200"><br>
        <strong>Figure 8</strong>
      </td>
      <td>/29 Subnet Address Ranges Notes screenshot. 2025.</td>
    </tr>
    <tr>
      <td style="text-align:center;">
        <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/key-subnetting-takeaways-9.jpg" alt="Key Takeaways Notes" width="200"><br>
        <strong>Figure 9</strong>
      </td>
      <td>Key Subnetting Takeaways Notes screenshot. 2025.</td>
    </tr>
  </tbody>
</table>

<div class="slideshow-container">

  <!-- Slide 1 -->
  <div class="mySlides3 fade">
    <div class="numbertext">1 / 9</div>
    <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/subnetting-and-cidr-notation-1..JPG" 
         style="width:100%; height:400px; object-fit:contain;">
    <div class="text">Figure 1: Subnetting and CIDR Notation Notes screenshot. 2025.</div>
  </div>

  <!-- Slide 2 -->
  <div class="mySlides3 fade">
    <div class="numbertext">2 / 9</div>
    <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/private-ip-address-ranges-binary-conversion_2.JPG" 
         style="width:100%; height:400px; object-fit:contain;">
    <div class="text">Figure 2: Private IP Address Ranges Notes screenshot. 2025.</div>
  </div>

  <!-- Slide 3 -->
  <div class="mySlides3 fade">
    <div class="numbertext">3 / 9</div>
    <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/subnetting-breakdown-reference-table-3.JPG" 
         style="width:100%; height:400px; object-fit:contain;">
    <div class="text">Figure 3: Subnetting Breakdown Reference Table Notes screenshot. 2025.</div>
  </div>

  <!-- Slide 4 -->
  <div class="mySlides3 fade">
    <div class="numbertext">4 / 9</div>
    <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/25-26-subnet-calculations-4.JPG" 
         style="width:100%; height:400px; object-fit:contain;">
    <div class="text">Figure 4: /25 and /26 Subnet Calculations Notes screenshot. 2025.</div>
  </div>

  <!-- Slide 5 -->
  <div class="mySlides3 fade">
    <div class="numbertext">5 / 9</div>
    <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/26-subnet-address-ranges-5.jpg" 
         style="width:100%; height:400px; object-fit:contain;">
    <div class="text">Figure 5: /26 Subnet Address Ranges Notes screenshot. 2025.</div>
  </div>

  <!-- Slide 6 -->
  <div class="mySlides3 fade">
    <div class="numbertext">6 / 9</div>
    <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/27-subnet-address-ranges-6.JPG" 
         style="width:100%; height:400px; object-fit:contain;">
    <div class="text">Figure 6: /27 Subnet Address Ranges Notes screenshot. 2025.</div>
  </div>

  <!-- Slide 7 -->
  <div class="mySlides3 fade">
    <div class="numbertext">7 / 9</div>
    <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/28-subnet-address-ranges-7.JPG" 
         style="width:100%; height:400px; object-fit:contain;">
    <div class="text">Figure 7: /28 Subnet Address Ranges Notes screenshot. 2025.</div>
  </div>

  <!-- Slide 8 -->
  <div class="mySlides3 fade">
    <div class="numbertext">8 / 9</div>
    <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/29-subnet-address-ranges-8.JPG" 
         style="width:100%; height:400px; object-fit:contain;">
    <div class="text">Figure 8: /29 Subnet Address Ranges Notes screenshot. 2025.</div>
  </div>

  <!-- Slide 9 -->
  <div class="mySlides3 fade">
    <div class="numbertext">9 / 9</div>
    <img src="https://raw.githubusercontent.com/EldonGabriel/eldongabriel.github.io/main/assets/notes/key-subnetting-takeaways-9.jpg" 
         style="width:100%; height:400px; object-fit:contain;">
    <div class="text">Figure 9: Key Subnetting Takeaways Notes screenshot. 2025.</div>
  </div>

</div>

<br>

<div style="text-align:center">
  <span class="dot3"></span> 
  <span class="dot3"></span> 
  <span class="dot3"></span>
  <span class="dot3"></span>
  <span class="dot3"></span>
  <span class="dot3"></span>
  <span class="dot3"></span>
  <span class="dot3"></span>
  <span class="dot3"></span>
</div>

<style>
.mySlides3 {display: none;}
</style>

<script>
let slideIndex3 = 0;
showSlides3();

function showSlides3() {
  let i;
  let slides = document.getElementsByClassName("mySlides3");
  let dots = document.getElementsByClassName("dot3");
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  slideIndex3++;
  if (slideIndex3 > slides.length) {slideIndex3 = 1}    
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex3-1].style.display = "block";  
  dots[slideIndex3-1].className += " active";
  setTimeout(showSlides3, 3000); // Change every 3 seconds
}
</script>

## <center>Key Takeaways</center>

- Reviewing old notes can spark useful exercises and refresh critical skills.  
- Subnetting isn’t just memorization; structured practice helps reinforce understanding.  
- Creating formal documentation from practice exercises builds knowledge and portfolio assets.

<p align="center">
  <a href="https://github.com/EldonGabriel/eldongabriel.github.io/blob/main/assets/reports/REPORT%20%E2%80%93%20IP%20Subnetting%20Fundamentals%20%E2%80%93%20v1.0.0.pdf" target="_blank">
    Full Report: REPORT – IP Subnetting Fundamentals – v1.0.0
  </a>
