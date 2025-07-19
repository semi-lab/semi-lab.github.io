---
layout: page
permalink: /gallery/
title: Gallery
description:  
nav: true
nav_order: 7
---


<div class="news">


<!-- Photo Collage with Arrows, Auto Transition, and Caption -->
<div style="position: relative; max-width: 600px; margin: 0 auto 30px;">
  <div id="collage" style="position: relative; border: 2px solid #ccc; border-radius: 8px; overflow: hidden; height: 360px;">
    <img src="../assets/img/MSEC_1.JPG" alt="Photo 1" style="position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 1; transition: opacity 0.6s ease;" />
    <img src="../assets/img/MSEC_2.JPG" alt="Photo 2" style="position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
    <img src="../assets/img/MSEC_33.JPG" alt="Photo 3" style="position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
    <img src="../assets/img/MSEC_4.JPG" alt="Photo 4" style="position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
    <img src="../assets/img/MSEC_5.JPG" alt="Photo 5" style="position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
    <img src="../assets/img/MSEC_6.JPG" alt="Photo 6" style="position: absolute; width: 100%; height: 100%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
           <!-- Left Arrow -->
    <div id="prev" style="position: absolute; top: 50%; left: 10px; transform: translateY(-50%); font-size: 2rem; color: white; background: rgba(0,0,0,0.4); padding: 5px 10px; border-radius: 5px; cursor: pointer;">&#10094;</div>
    <!-- Right Arrow -->
    <div id="next" style="position: absolute; top: 50%; right: 10px; transform: translateY(-50%); font-size: 2rem; color: white; background: rgba(0,0,0,0.4); padding: 5px 10px; border-radius: 5px; cursor: pointer;">&#10095;</div>
  </div>

  <!-- Caption -->
  <div id="caption" style="text-align: center; font-style: italic; font-size: 1rem; color: #555; margin-top: 10px;">
    Our group attended the ASME MSEC/SME NAMRC-53 Conference in Greenville, SC, (June 2025).
  </div>
</div>

<script>
  (function() {
    const images = document.querySelectorAll('#collage img');
    const caption = document.getElementById('caption');
    const captions = [
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference in Greenville, SC (June 2025)",
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference",
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference",
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference",
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference",
      "Our group attended the ASME MSEC/SME NAMRC-53 Conference",
      ];

    let currentIndex = 0;
    let interval;

    function showImage(index) {
      images.forEach((img, i) => {
        img.style.opacity = i === index ? 1 : 0;
      });
      caption.textContent = captions[index];
    }

    function nextImage() {
      currentIndex = (currentIndex + 1) % images.length;
      showImage(currentIndex);
    }

    function prevImage() {
      currentIndex = (currentIndex - 1 + images.length) % images.length;
      showImage(currentIndex);
    }

    // Manual controls
    document.getElementById('next').addEventListener('click', () => {
      nextImage();
      resetAutoSlide();
    });

    document.getElementById('prev').addEventListener('click', () => {
      prevImage();
      resetAutoSlide();
    });

    // Auto transition every 3 seconds
    function startAutoSlide() {
      interval = setInterval(nextImage, 3000);
    }

    function resetAutoSlide() {
      clearInterval(interval);
      startAutoSlide();
    }

    showImage(currentIndex);
    startAutoSlide();
  })();
</script>


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