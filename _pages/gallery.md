---
layout: page
permalink: /gallery/
title: Gallery
description:  
nav: true
nav_order: 8
---


<div class="news">

<!-- Photo Collage with Arrows, Auto Transition, and Caption -->
<div style="position: relative; max-width: 600px; margin: 0 auto 30px;">
  <div id="collage" style="position: relative; border: 2px solid #ccc; border-radius: 8px; overflow: hidden; height: 360px;">
    <!-- Images -->
    <img src="../assets/img/MSEC_1.JPG" alt="Photo 1" style="pointer-events: none; position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 1; transition: opacity 0.6s ease;" />
    <img src="../assets/img/MSEC_2.JPG" alt="Photo 2" style="pointer-events: none; position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />  
    <img src="../assets/img/MSEC_4.JPG" alt="Photo 4" style="pointer-events: none; position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
    <img src="../assets/img/MSEC_5.JPG" alt="Photo 5" style="pointer-events: none; position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
    <img src="../assets/img/MSEC_6.JPG" alt="Photo 6" style="pointer-events: none; position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />    
    <!-- Arrows -->
    <div id="prev" style="position: absolute; top: 50%; left: 10px; transform: translateY(-50%); font-size: 2rem; color: white; background: rgba(0,0,0,0.4); padding: 5px 10px; border-radius: 5px; cursor: pointer; z-index: 5;">&#10094;</div>
    <div id="next" style="position: absolute; top: 50%; right: 10px; transform: translateY(-50%); font-size: 2rem; color: white; background: rgba(0,0,0,0.4); padding: 5px 10px; border-radius: 5px; cursor: pointer; z-index: 5;">&#10095;</div>
  </div>

  <!-- Caption -->
  <div id="caption" style="text-align: center; font-style: italic; font-size: 1rem; color: #555; margin-top: 10px;">
    Our group attended the ASME MSEC/SME NAMRC-53 Conference in Greenville, SC (June 2025).
  </div>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const images = document.querySelectorAll('#collage img');
    const caption = document.getElementById('caption');
    const captions = [
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference in Greenville, SC (June 2025)",
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference",      
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference",
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference",
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference"
    ];

    let currentIndex = 0;
    let interval;

    function showImage(index) {
      images.forEach((img, i) => {
        img.style.opacity = i === index ? "1" : "0";
      });
      caption.textContent = captions[index] || "";
    }

    function nextImage() {
      currentIndex = (currentIndex + 1) % images.length;
      showImage(currentIndex);
    }

    function prevImage() {
      currentIndex = (currentIndex - 1 + images.length) % images.length;
      showImage(currentIndex);
    }

    function startAutoSlide() {
      interval = setInterval(nextImage, 4000); // 4 sec for better pacing
    }

    function resetAutoSlide() {
      clearInterval(interval);
      startAutoSlide();
    }

    document.getElementById('next').addEventListener('click', () => {
      nextImage();
      resetAutoSlide();
    });

    document.getElementById('prev').addEventListener('click', () => {
      prevImage();
      resetAutoSlide();
    });

    // Initialize
    showImage(currentIndex);
    startAutoSlide();
  });
</script>

<div class="table-responsive">
    <table class="table table-sm table-borderless">
      <tr>
        <th scope="row" style="white-space: nowrap;">Dec 19, 2025</th>
        <td>    Faydia has successfully completed her M.Eng. program and will be joining Sikorsky. Congrats, Faydia! </td>
      </tr>
      <tr>
        <td colspan="2" style="text-align: center;">
          <figure>
            <img src="../assets/img/faydia_graduate.png" alt="Faydia is presensing her research poster" style="width:50%; max-width:300px;">                        
          </figure>
        </td>
      </tr>
      <tr>


<div class="table-responsive">
    <table class="table table-sm table-borderless">
      <tr>
        <th scope="row" style="white-space: nowrap;">July 18, 2025</th>
        <td>    Our group participated in the NSF Engine milestone meeting as part of the RPI Team (from left to right: Prof. Akin, Prof. M. Stanley Whittingham (Nobel Laureate), Prof. Fudong Han). </td>
      </tr>
      <tr>
        <td colspan="2" style="text-align: center;">
          <figure>
            <img src="../assets/img/NSFe_engine2.jpg" alt="NSF Engine Milestone Meeting" style="width:80%; max-width:500px;">                        
          </figure>
        </td>
      </tr>
      <tr>

  <div class="table-responsive">
    <table class="table table-sm table-borderless">
      <tr>
        <th scope="row" style="white-space: nowrap;">May 1, 2025</th>
        <td>We celebrated the end of the Spring '25 semester and bid farewell to Hongfei and Hongru Liu, who are both heading to Carnegie Mellon University.</td>
      </tr>
      <tr>
        <td colspan="2" style="text-align: center;">
          <figure>
            <img src="../assets/img/Semi_Lab_Spring2025.jpg" alt="Spring 2025 Farewell" style="width:80%; max-width:500px;">                        
          </figure>
        </td>
      </tr>
      <tr>
        <th scope="row" style="white-space: nowrap;">October, 2024</th>
        <td>RPI Manufacturing Day - Blackhawk landing on campus.</td>
      </tr>
      <tr>
        <td colspan="2" style="text-align: center;">
          <figure>
            <img src="../assets/img/blackhawk.png" alt="Blackhawk landing" style="width:90%; max-width:500px; height:auto; max-height:1000px;">                        
          </figure>
        </td>
      </tr>
      <tr>
        <th scope="row" style="white-space: nowrap;">October, 2024</th>
        <td>We hosted Prof. Albert Shih (U-Mich) and Prof. Jianjun Shi (G-tech) at RPI.</td>
      </tr>
      <tr>
        <td colspan="2" style="text-align: center;">
          <figure>
            <img src="../assets/img/Alber_Shi.jpg" alt="Prof. Albert Shih Visit" style="width:80%; max-width:500px; height:auto; max-height:1000px;">                        
          </figure>
        </td>
      </tr>
      <tr>
        <th scope="row" style="white-space: nowrap;">Sep 27, 2024</th>
        <td>We hosted the DARPA SENSE program directors at RPI.</td>
      </tr>
      <tr>
        <td colspan="2" style="text-align: center;">
          <figure>
            <img src="../assets/img/DARPA_visit2.jpg" alt="DARPA Visit" style="width:80%; max-width:500px;">                        
          </figure>
        </td>
      </tr>
      <tr>
        <th scope="row" style="white-space: nowrap;">September 24, 2024</th>
        <td>We have successfully submitted our DARPA-SENSE project deliverables. <span class="star">&#128077;</span></td>
      </tr>
      <tr>
        <td colspan="2" style="text-align: center;">
          <figure>
            <img src="../assets/img/Darpa_dinner.jpg" alt="DARPA Dinner" style="width:60%; max-width:400px;">
          </figure>
        </td>
      </tr>
      <tr>
        <th scope="row" style="white-space: nowrap;">June 2024</th>
        <td>Dr. Akin attended the ASME Manufacturing Science and Engineering Conference (MSEC).</td>
      </tr>
      <tr>
        <td colspan="2" style="text-align: center;">
          <figure>
            <img src="../assets/img/martinjun_tim.jpg" alt="ASME MSEC Photo" style="width:60%; max-width:400px;">
          </figure>
          <i>From left to right: Dr. Semih Akin, Dr. Martin Jun (Purdue), Dr. Jung-Ting Tsai (Taiwan-Tech).</i>
        </td>
      </tr>  