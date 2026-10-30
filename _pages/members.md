---
layout: page
title: members
permalink: /members/
description: members of the unit 
nav: true
nav_order: 3
display_categories: [unit leaders, senior staff, postdocs, PhD candidates, guest researchers, other, alumini]
horizontal: false
---

<style>
  .projects.members img {
    display: block;
    width: 180px;
    height: 180px;
    max-width: 100%;
    object-fit: cover;
    object-position: center;
    border-radius: 50%;
    margin: 1rem auto 0;
  }
</style>

<!-- pages/projects.md -->
<div class="projects members">

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
