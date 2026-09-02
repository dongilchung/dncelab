---
layout: default
title: People
permalink: /people/
---
<h1>People</h1>

<h2>Lab Members</h2>
<div class="people">
{% assign members = site.data.people | sort: 'order' %}
{% for p in members %}
<div class="person">
  <img class="photo" src="{{ p.image | relative_url }}" alt="{{ p.name }}">
  <div class="name">{{ p.name }}</div>
  <div>{{ p.role }}</div>
  <div class="meta">{{ p.affiliation }}</div>
  {% if p.email %}<div class="meta">{{ p.email }}</div>{% endif %}
</div>
{% endfor %}
</div>
