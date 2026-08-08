---
title: Teaching
permalink: /teaching/
layout: default
page_title: Teaching
description: Details about teaching activities
nav: true
nav_order: 4
---

<style>
.course-link {
  font-size: 1.2rem;
  color: var(--global-theme-color);
  text-decoration: none;
}
.course-sem {
  font-size: 0.95rem;
  color: var(--global-text-color-light);
  margin-left: 0.4rem;
}
.selfml-card {
  border: 1px solid var(--global-divider-color);
  border-radius: 10px;
  background: var(--global-card-bg-color);
  padding: 1rem 1.25rem;
  margin-top: 1rem;
}
.selfml-head { display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 0.5rem; }
.selfml-title { font-weight: 600; font-size: 1.05rem; color: var(--global-theme-color); }
.selfml-btn {
  font-size: 0.85rem; font-weight: 500;
  color: var(--global-hover-text-color); background: var(--global-theme-color);
  border-radius: 6px; padding: 5px 13px; text-decoration: none;
}
.selfml-btn:hover { background: var(--global-hover-color); color: var(--global-hover-text-color); text-decoration: none; }
.selfml-desc { font-size: 0.95rem; color: var(--global-text-color); line-height: 1.55; margin: 0.7rem 0 0; }
</style>

#### Current Courses
{% assign current_courses = site.teaching | where: "status", "current" %}
<ul>
  {% for course in current_courses %}
    <li><a class="course-link" href="{{ course.url }}">{{ course.title }}</a>{% if course.semester %}<span class="course-sem">{{ course.semester }}</span>{% endif %}</li>
  {% endfor %}
</ul>

<div style="margin-top: 2rem;"></div>  <!-- Spacer -->

