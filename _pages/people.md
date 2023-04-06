---
layout: page
title: people
permalink: /people/
description: List of members.
nav: true
nav_order: 1
member_categories: [Head, PhD, Postdoc, ELLIS Excellence Fellow, Former]
horizontal: false
---

<!-- pages/member.md -->
<div class="projects">
{%- if page.member_categories %}
  <!-- Display categorized members -->
  {%- for category in page.member_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_members = site.data.members | where: "category", category -%}
  {%- if category == "Former" %}
    {%- assign sorting = "exit_year" -%}
  {%- else -%}
    {%- assign sorting = "lastname" -%}
  {%- endif -%}
  
  {%- assign sorted_members = categorized_members | sort: sorting  %}
  <!-- Generate cards for each project -->
  <div class="grid">
    {%- for member in sorted_members -%}
      {% include members.html %}
    {%- endfor %}
  </div>
  {% endfor %}

{%- else -%}
  {%- assign sorted_member = site.data.members | sort: "lastname"  -%}
  <!-- Generate cards for each project -->
  <div class="grid">
    {%- for member in sorted_member -%}
      {% include members.html %}
    {%- endfor %}
  </div>
{%- endif -%}
</div>
