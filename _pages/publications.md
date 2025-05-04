---
layout: page
permalink: /publications/
title: Publications
description: Ordered by most recent, († indicates equal contribution).
nav: false
nav_order: 4
---
<!-- _pages/publications.md -->
<div class="publications">


<!-- Bibliography list -->
<div id="pubList">
  {% bibliography -f {{ site.scholar.bibliography }} %}
</div>

</div>

<!-- Filtering Script -->
<script>
document.addEventListener('DOMContentLoaded', function () {
  const filterInput = document.getElementById('filterInput');
  const pubList = document.getElementById('pubList');

  filterInput.addEventListener('keyup', function() {
    const filter = filterInput.value.toLowerCase();
    const items = pubList.querySelectorAll('li, div.bibliography-entry'); // Adapt to your bibliography structure

    items.forEach(function(item) {
      const text = item.textContent || item.innerText;
      if (text.toLowerCase().indexOf(filter) > -1) {
        item.style.display = '';
      } else {
        item.style.display = 'none';
      }
    });
  });
});
</script>
