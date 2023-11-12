---
layout: page
title: Research
permalink: /research/
description: 
nav: true
nav_order: 1
display_categories: [work]
horizontal: false
---

<!-- wp:heading -->
<h4><span style="color: var(--global-theme-color)">Research interests</span></h4>
<!-- /wp:heading -->

<!-- wp:list -->
<ul>
<li><h5>Quantum communication and cryptography</h5></li>
<li><h5>Foundations of quantum mechanics</h5></li>
<li><h5>Network protocols</h5></li>
<li><h5>Quantum correlations: entanglement and nonlocality</h5></li>
</ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h4><span style="color: var(--global-theme-color)">Research topics</span></h4>
<!-- /wp:heading -->

<h5>(Page under construction)</h5>

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
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}


