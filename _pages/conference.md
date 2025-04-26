---
layout: page
permalink: /conference/
title: Conference Papers
description: 
nav: false
nav_order: 
---

<!-- _pages/conference.md -->

<!-- Type-to-Filter Bar at the top -->
<div style="margin-bottom: 20px;">
  <input type="text" id="filterInput" placeholder="Type to filter..." style="width: 200px; padding: 10px; font-size: 16px; display: block;">
</div>

<!-- Style for year headings -->
<style>
  .year {
    text-align: right;
    font-size: 1.8em;
    margin-bottom: 5px;
    text-decoration: underline;
  }
</style>

<!-- Wrap ALL content inside pubList -->
<div id="pubList">

  <div class="year">2024</div>

  <p>13. YW. Kim, <u>S. Akin</u>, MBG. Jun, J. Sutherland, “Cold spray-produced functional surfaces for triboelectric nanogenerators”, 
    <i>ASME International Mechanical Engineering Congress & Exposition, (IMECE)</i>, 2024. 
    <span style="float: right; font-size: 17px; color: red; font-weight: bold;">-Best Paper Award-</span>
  </p>

  <p>12. J. Lee, <u>S. Akin</u>, Y.Kim, E. Kim, J. Nam, K. Song, MBG. Jun, “A stethoscope-guided interpretable deep learning framework for powder flow diagnosis in cold spray additive manufacturing”, 
    <i>North American Manufacturing Research Conference (NAMRC-52)</i>, 2024.
  </p>

  <div class="year">2023</div>

  <p>11. JT. Tsai, <u>S. Akin</u>, DF. Bahr, MBG. Jun, “A predictive modeling for cold spray deposition and the resulting microstructure toward additive manufacturing using polymeric templates”, 
    <i>International Thin Films Conference (TACT-2023)</i>, 2023.
  </p>

  <!-- (Continue adding all your entries here, similar format) -->

</div> <!-- End of pubList -->

<!-- Filtering Script -->
<script>
document.addEventListener('DOMContentLoaded', function () {
  var filterInput = document.getElementById('filterInput');
  filterInput.addEventListener('keyup', function() {
    var filter = filterInput.value.toLowerCase();
    var pubList = document.getElementById('pubList');
    var items = pubList.querySelectorAll('p, .year');

    items.forEach(function(item) {
      var text = item.textContent.toLowerCase();
      if (text.includes(filter)) {
        item.style.display = '';
      } else {
        item.style.display = 'none';
      }
    });
  });
});
</script>
