---
layout: page
title: Research
permalink: /research/
description:
nav: true
nav_order: 3
---

<div class="research">

<p class="lead">We use ultrafast laser spectroscopy to watch what happens in materials in the first trillionths of a second after light is absorbed: how energy moves, how charges and the lattice push on each other, and how quantum coherence survives at room temperature. We work on hybrid perovskites and plasmonic–molecular hybrids, and develop new measurement tools including spectroscopy that uses entangled photons instead of classical laser light.</p>

---

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
