---
layout: page
permalink: /gallery/
title: Gallery
description:  
nav: true
nav_order: 8
---


<!-- Photo Collage with Arrows, Auto Transition, and Caption -->
<div style="position: relative; max-width: 600px; margin: 0 auto 30px;">

  <div
    id="collage"
    style="
      position: relative;
      border: 2px solid #ccc;
      border-radius: 8px;
      overflow: hidden;
      height: 360px;
    "
  >
    <!-- Photo 1 -->
    <img
      src="../assets/img/MSEC_2026-1.jpeg"
      alt="MSEC/NAMRC-54 Conference Photo 1"
      style="
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        top: 0;
        left: 0;
        opacity: 1;
        transition: opacity 0.6s ease;
      "
    />
    <!-- Photo 2 -->
    <img
      src="../assets/img/MSEC_2026-2.jpg"
      alt="MSEC/NAMRC-54 Conference Photo 2"
      style="
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        top: 0;
        left: 0;
        opacity: 0;
        transition: opacity 0.6s ease;
      "
    />
    <!-- Photo 3 -->
    <img
      src="../assets/img/MSEC_2026-3.jpg"
      alt="MSEC/NAMRC-54 Conference Photo 3"
      style="
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        top: 0;
        left: 0;
        opacity: 0;
        transition: opacity 0.6s ease;
      "
    />
    <!-- Photo 4 -->
    <img
      src="../assets/img/MSEC_2026-4.jpg"
      alt="MSEC/NAMRC-54 Conference Photo 4"
      style="
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        top: 0;
        left: 0;
        opacity: 0;
        transition: opacity 0.6s ease;
      "
    />
    <!-- Photo 5 -->
    <img
      src="../assets/img/MSEC_2026-5.jpg"
      alt="MSEC/NAMRC-54 Conference Photo 5"
      style="
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        top: 0;
        left: 0;
        opacity: 0;
        transition: opacity 0.6s ease;
      "
    />
    <!-- Previous Arrow -->
    <button
      id="prev"
      type="button"
      style="
        position: absolute;
        top: 50%;
        left: 10px;
        transform: translateY(-50%);
        z-index: 10;
        background: rgba(0,0,0,0.5);
        color: white;
        border: none;
        border-radius: 50%;
        width: 40px;
        height: 40px;
        cursor: pointer;
        font-size: 22px;
      "
    >
      &#10094;
    </button>
    <!-- Next Arrow -->
    <button
      id="next"
      type="button"
      style="
        position: absolute;
        top: 50%;
        right: 10px;
        transform: translateY(-50%);
        z-index: 10;
        background: rgba(0,0,0,0.5);
        color: white;
        border: none;
        border-radius: 50%;
        width: 40px;
        height: 40px;
        cursor: pointer;
        font-size: 22px;
      "
    >
      &#10095;
    </button>

  </div>
  
  <!-- Caption -->
  <div
    id="caption"
    style="
      text-align: center;
      font-style: italic;
      font-size: 1rem;
      color: #555;
      margin-top: 10px;
    "
  >
    Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026).
  </div>

</div>

<script>
document.addEventListener("DOMContentLoaded", function () {

  const collage = document.getElementById("collage");
  const images = collage.querySelectorAll("img");
  const caption = document.getElementById("caption");
  const prevButton = document.getElementById("prev");
  const nextButton = document.getElementById("next");

  const captions = [
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026).",
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026).",
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026).",
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026).",
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026)."
  ];

  let currentIndex = 0;
  let intervalId;

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
    currentIndex =
      (currentIndex - 1 + images.length) % images.length;

    showImage(currentIndex);
  }

  function startAutoSlide() {
    clearInterval(intervalId);

    if (images.length > 1) {
      intervalId = setInterval(nextImage, 4000);
    }
  }

  if (prevButton) {
    prevButton.addEventListener("click", function () {
      prevImage();
      startAutoSlide();
    });
  }

  if (nextButton) {
    nextButton.addEventListener("click", function () {
      nextImage();
      startAutoSlide();
    });
  }

  if (images.length > 0) {
    showImage(currentIndex);
    startAutoSlide();
  }

});
</script>

<!-- KOREAN VISITOR TO RPI -->

<!-- Photo Collage with Manual Arrows and Caption -->

<div style="position: relative; max-width: 600px; margin: 0 auto 30px;">

  <!-- Photo Container -->
  <div
    id="collage"
    style="
      position: relative;
      border: 2px solid #ccc;
      border-radius: 8px;
      overflow: hidden;
      height: 360px;
    "
    >
    <!-- Photo 1 -->
    <img
      src="../assets/img/Korea-1.jpeg"
      alt="KITECH and KIMM Visit Photo 1"
      style="
        pointer-events: none;
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        top: 0;
        left: 0;
        opacity: 1;
        transition: opacity 0.6s ease;
      "
    />
    <!-- Photo 2 -->
    <img
      src="../assets/img/Korea-2.jpeg"
      alt="KITECH and KIMM Visit Photo 2"
      style="
        pointer-events: none;
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        top: 0;
        left: 0;
        opacity: 0;
        transition: opacity 0.6s ease;
      "
    />
    <!-- Photo 3 -->
    <img
      src="../assets/img/Korea-3.jpeg"
      alt="KITECH and KIMM Visit Photo 3"
      style="
        pointer-events: none;
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        top: 0;
        left: 0;
        opacity: 0;
        transition: opacity 0.6s ease;
      "
    />
    <!-- Previous Arrow -->
    <div
      id="prev"
      role="button"
      aria-label="Previous photo"
      style="
        position: absolute;
        top: 50%;
        left: 10px;
        transform: translateY(-50%);
        font-size: 2rem;
        color: white;
        background: rgba(0, 0, 0, 0.4);
        padding: 5px 10px;
        border-radius: 5px;
        cursor: pointer;
        z-index: 5;
        user-select: none;
      "
    >
      &#10094;
    </div>
    <!-- Next Arrow -->
    <div
      id="next"
      role="button"
      aria-label="Next photo"
      style="
        position: absolute;
        top: 50%;
        right: 10px;
        transform: translateY(-50%);
        font-size: 2rem;
        color: white;
        background: rgba(0, 0, 0, 0.4);
        padding: 5px 10px;
        border-radius: 5px;
        cursor: pointer;
        z-index: 5;
        user-select: none;
      "
    >
      &#10095;
    </div>

  </div>
  <!-- Caption -->
  <div
    id="caption"
    style="
      text-align: center;
      font-style: italic;
      font-size: 1rem;
      color: #555;
      margin-top: 10px;
    "
  >
    SEMI-LAB hosted visitors from the Korea Institute of Industrial Technology
    (KITECH) (Dr. Jungso Nam &amp; Dr. Kyeongeun Song) and the Korea Institute
    of Machinery &amp; Materials (KIMM) (Dr. Jungsub Kim &amp; Dr. Gyuho Kim)
    (June 2026).
  </div>

</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const images = document.querySelectorAll("#collage img");
    const prevButton = document.getElementById("prev");
    const nextButton = document.getElementById("next");

    let currentIndex = 0;

    function showImage(index) {
      images.forEach((img, i) => {
        img.style.opacity = i === index ? "1" : "0";
      });
    }

    nextButton.addEventListener("click", function () {
      currentIndex = (currentIndex + 1) % images.length;
      showImage(currentIndex);
    });

    prevButton.addEventListener("click", function () {
      currentIndex = (currentIndex - 1 + images.length) % images.length;
      showImage(currentIndex);
    });
  });
</script>

<script>
document.addEventListener("DOMContentLoaded", function () {

  const collage = document.getElementById("collage");
  const images = collage.querySelectorAll("img");
  const caption = document.getElementById("caption");
  const prevButton = document.getElementById("prev");
  const nextButton = document.getElementById("next");

  const captions = [
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026).",
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026).",
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026).",
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026).",
    "Our group attended the ASME MSEC/SME NAMRC-54 Conference at Penn State University (June 2026)."
  ];

  let currentIndex = 0;
  let intervalId;

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
    currentIndex =
      (currentIndex - 1 + images.length) % images.length;

    showImage(currentIndex);
  }

  function startAutoSlide() {
    clearInterval(intervalId);

    if (images.length > 1) {
      intervalId = setInterval(nextImage, 4000);
    }
  }

  if (prevButton) {
    prevButton.addEventListener("click", function () {
      prevImage();
      startAutoSlide();
    });
  }

  if (nextButton) {
    nextButton.addEventListener("click", function () {
      nextImage();
      startAutoSlide();
    });
  }

  if (images.length > 0) {
    showImage(currentIndex);
    startAutoSlide();
  }

});
</script>


<div class="table-responsive">
    <table class="table table-sm table-borderless">
      <tr>
        <th scope="row" style="white-space: nowrap;">Feb 16, 2026</th>
        <td> We celebrated our group’s recent publications with a lunch accompanied by Turkish tea!</td>
      </tr>
      <tr>
        <td colspan="2" style="text-align: center;">
          <figure>
            <img src="../assets/img/Lavenza.jpeg" alt="SEMI-Lab Lunch with PhD Students" style="width:70%; max-width:500px;">                      
          </figure>
        </td>
      </tr>
      <tr>


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
