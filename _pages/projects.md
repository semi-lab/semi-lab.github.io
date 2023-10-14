---
layout: page
title: Research
permalink: /research/
description: 
nav: true
nav_order: 2
display_categories: [Polymer Metallization, Printed Flexible Electronics, Energy Devices, Spray Modeling]
horizontal: true
---

<div class="projects">
  <!-- Display categorized projects -->
  <h2 class="category">Polymer Metallization</h2>
  <!-- Generate cards for each project -->
  <div class="container">
    <!-- Change the layout of horizontal cards: 1x1 vs. 1x2 per row -->
    <!-- <div class="row row-cols-2"> -->
    <div class="row row-cols-1">
<div class="card-item col">
<a href="/semi-lab/projects/2_project/"><div class="card hoverable">
      <div class="row g-0">
<div class="card-img col-md-4">
          <figure>

  <picture>    
    <source class="responsive-img-srcset" media="(max-width: 480px)" srcset="/assets/img/ACS_cover1.jpg"></source>
    <source class="responsive-img-srcset" media="(max-width: 800px)" srcset="/NanoX/assets/img/hetero-ai-800.webp"></source>
    <source class="responsive-img-srcset" media="(max-width: 1400px)" srcset="/NanoX/assets/img/hetero-ai-1400.webp"></source>
    <!-- Fallback to the original file -->
    <img src="/assets/img/ACS_cover1.jpg" width="auto" height="auto" alt="project thumbnail" onerror="this.onerror=null; $('.responsive-img-srcset').remove();">

  </picture>

</figure>















<!-- pages/projects.md -->
<div class="projects">
  {%- if site.enable_project_categories and page.display_categories %}
    <!-- Display categorized projects -->
    {%- for category in page.display_categories %}
    <h2 class="category">{{ category }}</h2>
    {%- assign categorized_projects = site.projects | where: "category", category -%}
    {%- assign sorted_projects = categorized_projects | sort: "importance" %}
    <!-- Generate cards for each project -->    
    <div class="container">
      <div class="row row-cols-1">    
        {%- for project in sorted_projects -%}
          <div class="{% if forloop.first %}col-first{% else %}col{% endif %}"> <!-- Adjust the class for the first and other columns -->
            {% include projects_horizontal.html %}
          </div>
        {%- endfor %}
      </div>
    </div>    
    <!-- End Generate cards for each project -->    
    {%- endfor %}
  {%- endif -%}
</div>