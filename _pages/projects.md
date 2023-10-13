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
        {% if loop.index == 1 %}  <!-- Add this condition to target the first column -->
          <div class="col-first"> <!-- Assign a custom class to the first column -->
            {% include projects_horizontal.html %}
          </div>
        {% else %}
          <div class="col">
            {% include projects_horizontal.html %}
          </div>
        {% endif %}
      {%- endfor %}
    </div>
  </div>

  {%- else -%}

  <div class="grid">
    {%- for project in sorted_projects -%}
      {% if loop.index == 1 %}  <!-- Add this condition to target the first column -->
        <div class="col-first"> <!-- Assign a custom class to the first column -->
          {% include projects.html %}
        </div>
      {% else %}
        <div class="col">
          {% include projects.html %}
        </div>
      {% endif %}
    {%- endfor %}
  </div>

  {%- endif -%}
  <!-- End Generate cards for each project -->
  
  {%- endfor %}
</div>