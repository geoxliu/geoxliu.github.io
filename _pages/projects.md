---
layout: page
title: Research
permalink: /research/
description: A growing collection of cool projects.
nav: true
display_categories: [Sustainability, China and the World]
horizontal: false
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


### Research projects
* 2020-now    Co-PI, “Ecogovernmentality, Ecocivilization, and China's Green Belt and Road Initiative” (funded by HKU seed fund for basic research)
* 2018-2019  Participant, “The Geopolitics of International Rivers: A Case Study of Lancang-Mekong Transboundary Water Governance” (funded by national science foundation of China)
* 2017-2019  Participant, “Inter-Basin Cooperation and Symbiotic Governance System of the ‘Golden Quadrilateral’ of China-Myanmar-Thailand-Laos” (funded by major research plan of national social science foundation of China)
* 2016-2018   Participant, “Transboundary Water Governance under Lancang-Mekong Cooperation: A Perspective of International NGOs” (funded by Ministry of Education)
* 2013-2015   PI, “Representational Space in Beijing: A Study Based on Local Literature” (funded by Beijing college students research action Plan, awarded excellent project)

