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

<!-- pages/projects.md -->
<div class="projects">
  {%- if site.enable_project_categories and page.display_categories %}
    <!-- Display categorized projects -->
    {%- for category in page.display_categories %}
    <h2 class="category">{{ category }}</h2>
    {%- assign categorized_projects = site.projects | where: "category", category -%}
    {%- assign sorted_projects = categorized_projects | sort: "importance" %}
    <!-- Generate cards for each project -->
    
    {% if page.horizontal -%}
    
    <div class="container">
      <div class="row row-cols-1">    
        {%- for project in sorted_projects -%}
          <div class="col {% if forloop.first %}col-first{% endif %}"> <!-- Add a class for the first column -->
            {% include projects_horizontal.html %}
          </div>
        {%- endfor %}
      </div>
    </div>
    
    {%- else -%}
    
    <div class="grid">
      {%- for project in sorted_projects -%}
        <div class="col {% if forloop.first %}col-first{% endif %}"> <!-- Add a class for the first column -->
          {% include projects_horizontal.html %}
        </div>
      {%- endfor %}
    </div>
    {% endif -%} <!-- Close the "if" statement for page.horizontal -->
    <!-- End Generate cards for each project -->
    
    {%- endfor %}
  {%- endif -%}
</div>

<style>
  /* Custom CSS to adjust the width of the first column */
  .col-first {
    width: 30%; /* Adjust the width as needed */
  }

  /* CSS for other columns (optional) */
  .col {
    width: 70%; /* Adjust the width for other columns */
  }
</style>