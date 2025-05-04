---
---
layout: page
permalink: /publications/
title: Publications
description: Ordered by most recent († indicates equal contribution).
nav: false
nav_order: 4
---
<div class="publications">
  <!-- Filter bar -->
  <input type="text" id="pubFilter" placeholder="Filter by keyword, year, or author..." style="margin-bottom: 1em; padding: 0.5em; width: 100%; max-width: 400px; border-radius: 5px; border: 1px solid #ccc;">

  <!-- Bibliography list -->
  <div id="pubList">
    {% bibliography --file {{ site.scholar.bibliography }} %}
  </div>

</div>

<script>
  document.addEventListener('DOMContentLoaded', function () {
    const filterInput = document.getElementById('pubFilter');
    const pubList = document.getElementById('pubList');
    const publications = pubList.querySelectorAll('div');

    filterInput.addEventListener('input', function () {
      const filter = this.value.toLowerCase();

      publications.forEach(pub => {
        if (pub.textContent.toLowerCase().includes(filter)) {
          pub.style.display = '';
        } else {
          pub.style.display = 'none';
        }
      });
    });
  });
</script>
