---
layout: page
permalink: /teaching/
title: teaching
description: Course materials, schedules, and resources for classes taught.
nav: true
nav_order: 6
---

{% assign courses_by_year = site.teachings | sort: 'year' | reverse | group_by: 'year' %}

{% for year_group in courses_by_year %}
<h2>{{ year_group.name }}</h2>
<ul class="teaching-list">
  {% assign year_courses = year_group.items | sort: 'term' %}
  {% for course in year_courses %}
  <li>
    <a href="{{ course.url | relative_url }}"><strong>{{ course.title }}</strong></a>
    {% if course.term %} — {{ course.term }}{% endif %}
  </li>
  {% endfor %}
</ul>
{% endfor %}
