---
layout: page
title: people
permalink: /people/
description: List of members.
nav: true
nav_order: 1
positions: [Faculty, Postdoc, PhD, ELLIS Excellence Fellow, Former Member]
---

<!-- pages/member.md -->
<div class="people">
  {%- for position in page.positions %}
  <h2 class="category">{{ position }}</h2>
  {%- if position == "Former Member" %}
    {%- assign categorized_members = site.data.members | where_exp:"item", "item.former != nil" -%}
    {%- assign sorted_members = categorized_members | sort: "exit_year" | reverse %}
  {%- else -%}
    {%- assign categorized_members = site.data.members | where: "position", position | where: "former", nil -%}
    {%- assign sorted_members = categorized_members | sort: "lastname"  %}
  {%- endif -%}
    {%- for member in sorted_members -%}
      {% include members.html %}
    {%- endfor %}
  {% endfor %}
</div>