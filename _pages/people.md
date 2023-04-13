---
layout: page
title: people
permalink: /people/
description: List of members.
nav: true
nav_order: 1
member_categories: [Faculty, Postdoc, PhD, ELLIS Excellence Fellow, Former Member]
---

<!-- pages/member.md -->
<div class="people">
  {%- for category in page.member_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_members = site.data.members | where: "category", category -%}
  {%- if category == "Former" %}
    {%- assign sorting = "exit_year" -%}
  {%- else -%}
    {%- assign sorting = "lastname" -%}
  {%- endif -%}
  {%- assign sorted_members = categorized_members | sort: sorting  %}
    {%- for member in sorted_members -%}
      {% include members.html %}
    {%- endfor %}
  {% endfor %}
</div>
