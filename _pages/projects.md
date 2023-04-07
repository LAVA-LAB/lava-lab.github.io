---
layout: page
title: projects
permalink: /projects/
description: Projects available for MSc thesis and interships.
nav: false
nav_order: 0
display_categories: [open]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category" id="{{- category -}}">{{ category }}</h2>
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


<div class="projects">
<h2 class="category" id="past">past</h2>
</div>

<div class="news">
  <div class="table-responsive">
    <table class="table table-sm table-borderless">
    {% for thesis_year in site.data.thesis %}
      {% for thesis in thesis_year[1] %}
        <tr>
          {% if forloop.first %}
          <th scope="row">{{ thesis.year }}</th>
            {% else %}
          <th scope="row"></th>
          {% endif %}
          <td>
          {% if thesis.url %}
              <a class="news-title" href="{{ thesis.url | relative_url }}">
                {{ thesis.title }}
              </a>
            {% else %}
                {{ thesis.title }}
          {% endif %}
              <br>
              {{ thesis.author }}
          </td>
        </tr>
      {%- endfor %}
    {%- endfor %}
    </table>
  </div>
</div>
