---
layout: page
title: Projects
permalink: /projects/
description: Projects available for MSc thesis and interships.
nav: false
nav_order: 0
horizontal: false
---

This page contains a number of proposals for Bachelor- and Master thesis topics. If you are interested in any of these projects (or in any of our research directions more generally), feel free to send us an email!

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


## Ongoing projects:

<div class="projects">
<h2 class="category" id="ongoing">ongoing</h2>
</div>

<div class="news">
  <div class="table-responsive">
    <table class="table table-sm table-borderless">
    {%- assign thesis_ongoing = site.data.thesis | where: "year", nil -%}
    {% for thesis in thesis_ongoing %}
        <tr>
          {% if forloop.first %}
          <th scope="row"></th>
            {% else %}
          <th scope="row"></th>
          {% endif %}
          <td>
          <ul><li>
          {% if thesis.url %}
              <a class="news-title" href="{{ thesis.url | relative_url }}">
                {{ thesis.title }}
              </a>
            {% else %}
                {{ thesis.title }}
          {% endif %}
              <br>
              {{ thesis.author }}
          </li></ul>
          </td>
        </tr>
    {%- endfor %}
    </table>
  </div>
</div>

## Previously completed projects:

<div class="projects">
<h2 class="category" id="complete">complete</h2>
</div>

<div class="news">
  <div class="table-responsive">
    <table class="table table-sm table-borderless">
    {%- assign thesis_complete = site.data.thesis | where_exp:"item", "item.year != nil" | group_by: "year" -%}
    {% for group in thesis_complete %}
      {% for thesis in group.items %}
        <tr>
          {% if forloop.first %}
          <th scope="row">{{ group.name }}</th>
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
