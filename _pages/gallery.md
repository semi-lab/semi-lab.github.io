---
layout: page
permalink: /gallery/
title: Gallery
description:  
nav: true
nav_order: 7
---


<div class="news">

<!-- Photo Collage with Click Transition and Caption -->
<div id="collage" style="margin-bottom: 30px; max-width: 600px; margin-left: auto; margin-right: auto; cursor: pointer; border: 2px solid #ccc; border-radius: 8px; overflow: hidden; height: 360px; position: relative;">
  <img src="../assets/img/MSEC_1.JPG" alt="Photo 1" style="position: absolute; width: 70%; height: 60%; object-fit: cover; top: 0; left: 0; opacity: 1; transition: opacity 0.6s ease;" />
  <img src="../assets/img/MSEC_2.JPG" alt="Photo 2" style="position: absolute; width: 70%; height: 60%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
  <img src="../assets/img/MSEC_3.JPG" alt="Photo 3" style="position: absolute; width: 70%; height: 60%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
  <img src="../assets/img/MSEC_4.JPG" alt="Photo 4" style="position: absolute; width: 70%; height: 60%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
  <img src="../assets/img/MSEC_5.JPG" alt="Photo 5" style="position: absolute; width: 70%; height: 60%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
  <img src="../assets/img/MSEC_6.JPG" alt="Photo 6" style="position: absolute; width: 70%; height: 60%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
  <img src="../assets/img/MSEC_7.JPG" alt="Photo 7" style="position: absolute; width: 70%; height: 60%; object-fit: cover; top: 0; left: 0; opacity: 0; transition: opacity 0.6s ease;" />
</div>

<!-- Caption -->
<div id="caption" style="max-width: 600px; margin: 0 auto 30px; text-align: center; font-style: italic; font-size: 1rem; color: #555;">
  Caption for Photo 1
</div>

<script>
  const collage = document.getElementById('collage');
  const images = collage.querySelectorAll('img');
  const caption = document.getElementById('caption');
  const captions = [
    "Our group attended the ASME MSEC/SME NAMRC-53 Conference in Greenville, South Carolina."   
  ];
  let currentIndex = 0;

  collage.addEventListener('click', () => {
    images[currentIndex].style.opacity = 0;
    currentIndex = (currentIndex + 1) % images.length;
    images[currentIndex].style.opacity = 1;
    caption.textContent = captions[currentIndex];
  });
</script>


  <!-- Existing content below -->
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
      <!-- ... (rest of your existing table rows and images) ... -->
    </table>
  </div>
</div>

<script>
  // JavaScript for click transition on the collage
  const collage = document.getElementById('collage');
  const images = collage.querySelectorAll('img');
  let currentIndex = 0;

  collage.addEventListener('click', () => {
    images[currentIndex].style.opacity = 0;
    currentIndex = (currentIndex + 1) % images.length;
    images[currentIndex].style.opacity = 1;
  });
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