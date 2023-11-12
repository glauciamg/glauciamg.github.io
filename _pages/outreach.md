---
layout: page
title: Outreach
permalink: /outreach/
description: 
nav: true
nav_order: 3
display_categories: [work]
horizontal: false
---



<h4> Links and information on blog posts and general outreach content:<h4>

&nbsp;
<!-- wp:heading -->
<h4><strong><span style="color: var(--global-theme-color)">Podcast O Q Quântico</span>(more info coming soon)</strong></h4>
<!-- /wp:heading -->

  <h5>  
Currently in the production phase, the podcast ‘O Q Quântico’  aims at introducing
basic concepts of quantum theory to the general public while confronting misinformation and
pseudo-science. We also aim at bringing visibility to the quantum information community in
Brazil by interviewing researchers from different universities in the podcast. The project is developed in collaboration
with Leonardo Guerini, from Universidade Federal de Santa Maria, and Revista Arco, also
from Universidade Federal de Santa Maria, and is supported by the INCT de Informação Quântica and the Cluster of Excellence Matter and Light for Quantum Computing.<h5>



&nbsp;

<!-- wp:heading -->
<h4><span style="color: var(--global-theme-color)">Unsere Forschung im Dialog|Quantum Cryptography:</span></h4>
<!-- /wp:heading -->

<h5> Check out this <a href="https://www.youtube.com/watch?v=oSAPe_pfqzE&ab_channel=ML4QClusterofExcellence">video</a>, where, together with colleagues and the ML4Q, we try to explain our recent findings on Quantum Cryptography in four levels of difficulty!</h5>

&nbsp;

<!-- wp:heading -->
<h4><span style="color: var(--global-theme-color)">Playing cards with quantum entanglement:</span></h4>
<!-- /wp:heading -->

<h5> Here you can find the blog post I wrote for <a href="https://blog.qutech.nl/index.php/2017/02/10/playing-card-with-quantum-entanglement/">Bits of Quantum - A blog by QuTech</a>.</h5>

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "outreach", category -%}
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

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
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
{%- endif -%}
</div>
