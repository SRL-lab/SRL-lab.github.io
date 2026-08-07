---
layout: page
permalink: /people/
title: People
description: members of SRLab
nav: true
nav_order: 7
---

<div class="team">

<h2>Principal Investigator</h2>
<div class="row row-cols-1 row-cols-md-3">
  {% assign pi = site.data.team.principal_investigator %}
  <div class="col">
    <a href="{{ pi.link }}">
      <div class="card h-100 hoverable">
        {% if pi.image %}
          <img class="card-img-top" src="{{ '/assets/img/' | append: pi.image | relative_url }}" alt="{{ pi.name }}">
        {% endif %}
        <div class="card-body">
          <h3 class="card-title">{{ pi.name }}</h3>
          <p class="card-text">{{ pi.title }}<br>{{ pi.affiliation }}</p>
        </div>
      </div>
    </a>
  </div>
</div>

{% if site.data.team.members and site.data.team.members.size > 0 %}
<h2>Team Members</h2>
<div class="row row-cols-1 row-cols-md-3">
  {% for member in site.data.team.members %}
  <div class="col">
    <a href="{{ member.link }}">
      <div class="card h-100 hoverable">
        {% if member.image %}
          <img class="card-img-top" src="{{ '/assets/img/' | append: member.image | relative_url }}" alt="{{ member.name }}">
        {% endif %}
        <div class="card-body">
          <h3 class="card-title">{{ member.name }}</h3>
          <p class="card-text">{{ member.title }}<br>{{ member.affiliation }}</p>
        </div>
      </div>
    </a>
  </div>
  {% endfor %}
</div>
{% endif %}


<h2>Collaborators</h2>
<ul>
  {% for collaborator in site.data.team.collaborators %}
  <li>
    <a href="{{ collaborator.link }}">{{ collaborator.name }}</a> — {{ collaborator.title }}, {{ collaborator.affiliation }}
  </li>
  {% endfor %}
</ul>

</div>
