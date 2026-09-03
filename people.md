---
layout: default
title: People
permalink: /people/
---
<h1>People</h1>

<h2>Principal Investigator</h2>
<div class="people people-single">
{% assign pi_members = site.data.people | where: 'category', 'principal_investigator' | sort: 'order' %}
{% for p in pi_members %}
<div class="person">
  {% if p.image %}<img class="photo" src="{{ p.image | relative_url }}" alt="{{ p.name }}">{% endif %}
  <div class="name">{{ p.name }}</div>
  <div>{{ p.role }}</div>
  <div class="meta">{{ p.affiliation }}</div>
  {% if p.email %}<div class="meta"><a href="mailto:{{ p.email }}">{{ p.email }}</a></div>{% endif %}
  <div class="social-links">
    {% if p.google_scholar and p.google_scholar != "" %}<a href="{{ p.google_scholar }}" target="_blank" rel="noopener">Google Scholar</a>{% endif %}
    {% if p.twitter and p.twitter != "" %}<a href="{{ p.twitter }}" target="_blank" rel="noopener">Twitter</a>{% endif %}
  </div>
</div>
{% endfor %}
</div>

<h2>Lab Members</h2>
<div class="people">
{% assign lab_members = site.data.people | where: 'category', 'lab_member' | sort: 'order' %}
{% for p in lab_members %}
<div class="person">
  {% if p.image %}<img class="photo" src="{{ p.image | relative_url }}" alt="{{ p.name }}">{% endif %}
  <div class="name">{{ p.name }}</div>
  <div>{{ p.role }}</div>
  <div class="meta">{{ p.affiliation }}</div>
  {% if p.email %}<div class="meta"><a href="mailto:{{ p.email }}">{{ p.email }}</a></div>{% endif %}
  <div class="social-links">
    {% if p.google_scholar and p.google_scholar != "" %}<a href="{{ p.google_scholar }}" target="_blank" rel="noopener">Google Scholar</a>{% endif %}
    {% if p.twitter and p.twitter != "" %}<a href="{{ p.twitter }}" target="_blank" rel="noopener">Twitter</a>{% endif %}
  </div>
</div>
{% endfor %}
</div>

<h2>Alumni</h2>
<div class="alumni">
{% assign alumni = site.data.people | where: 'category', 'alumni' | sort: 'name' %}
{% for p in alumni %}
<div><b>{{ p.name }}</b><br><span class="meta">{{ p.role }} · {{ p.affiliation }}</span></div>
{% endfor %}
</div>
