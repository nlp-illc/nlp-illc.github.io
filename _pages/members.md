---
layout: page
title: members
permalink: /members/
description: members of the unit 
image_circular: true # crops the image to make it circular
nav: true
nav_order: 3
display_categories: [unit leaders, senior staff, postdocs, PhD candidates, guest researchers, other, alumini]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">

  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.members | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "title" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

</div>
