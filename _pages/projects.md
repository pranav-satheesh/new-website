---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 2
horizontal: false
---

<!-- pages/projects.md -->
<div class="page-description mb-4">
  <p>My research focuses on supermassive black holes (SMBHs) and galaxy evolution. I use cosmological simulations to study the co-evolution of SMBHs and their host galaxies throughout cosmic time. I also focus on the dynamics of SMBHs and mergers which produce gravitational waves observable by <a href="https://www.esa.int/Science_Exploration/Space_Science/LISA" target="_blank">LISA</a> and <a href="https://ipta4gw.org/" target="_blank">pulsar timing array </a> experiments.</p>
  
  <p>For a detailed overview of my projects see below. You can checkout my relevant publications <a href="/publications/">here</a>.</p>
</div>

<div class="projects">
<!-- Display projects without categories -->
{% assign sorted_projects = site.projects | sort: "importance" %}

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
</div>
