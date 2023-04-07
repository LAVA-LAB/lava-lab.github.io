---
layout: page
title: talks
permalink: /talks/
description: Presentations given by members of the group.
nav: true
nav_order: 4
display_categories: [open, past]
horizontal: false
---

<!-- pages/talks.md -->


  <div class="news">
    {% for talks_of_the_year in site.data.talks %}  
    <h2 class="category" id="{{- talks_of_the_year[0] -}}">{{ talks_of_the_year[0] }}</h2>
    <div class="table-responsive">
      <table class="table table-sm table-borderless">
      {%- assign talks_sorted = talks_of_the_year[1] | sort: "date" | reverse -%}
      {% for talk in talks_sorted %} 
        <tr>
          <th scope="row">{{ talk.date | date: "%b %-d" }}</th>
          <td>
            {% if talk.url %}
              <a class="news-title" href="{{ talk.url | relative_url }}">
                {{ talk.title }}
              </a>
            {% else %}
                {{ talk.title }}
            {% endif %}
              <br>
              {{ talk.location }}
          </td>
        </tr>
      {%- endfor %} 
      </table>
    </div>
    {%- endfor %} 
  </div>

