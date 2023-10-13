---
layout: page
title: Research
permalink: /research/
description: 
nav: true
nav_order: 2
display_categories: [Polymer Metallization, Printed Flexible Electronics, Energy Devices, Spray Modeling, Deneme]
horizontal: true
---

<style>
  /* Custom CSS to adjust the width of the first column */
  .col-first {
    width: 10%; /* Width for the first column */
    height: 100px; /* Height for the first column */
  }

  /* CSS for other columns (optional) */
  .col {
    width: 40%; /* Width for other columns */
    height: 100px; /* Height for other columns */
  }
</style>

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