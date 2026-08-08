---
layout: page
title: Research
permalink: /research/
description:
nav: true
nav_order: 3
---

<div class="research">

#<p class="lead">A one- or two-line summary of your lab's overall research mission goes here.</p>

{% for topic in site.data.research %}
<hr>

<h3>#{{ forloop.index }} {{ topic.title }}</h3>

<div class="row align-items-center">
  {% if topic.image %}
  <div class="col-md-4 mb-3 mb-md-0">
    <img src="{{ '/assets/img/' | append: topic.image | relative_url }}" class="img-fluid rounded" alt="{{ topic.title }}">
  </div>
  <div class="col-md-8">
    {{ topic.text | markdownify }}
  </div>
  {% else %}
  <div class="col-12">
    {{ topic.text | markdownify }}
  </div>
  {% endif %}
</div>

{% if topic.links and topic.links.size > 0 %}
<p>
  <strong>Related Materials:</strong>
  {% for link in topic.links %}
    <a href="{{ link.url }}">[{{ link.label }}]</a>{% unless forloop.last %} |{% endunless %}
  {% endfor %}
</p>
{% endif %}

{% endfor %}

</div>
