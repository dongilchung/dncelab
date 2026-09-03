---
layout: default
title: Publications
permalink: /publications/
---
<h1>Publications</h1>

{% assign pubs_by_year = site.data.publications | group_by: 'year' | sort: 'name' | reverse %}
{% for year in pubs_by_year %}
<h2 class="publication-year">{{ year.name }}</h2>
<div class="publication-list">
{% for p in year.items %}
<article class="publication-item{% if p.image and p.image != "" %} has-thumbnail{% endif %}">
  {% if p.image and p.image != "" %}
  <a class="publication-thumb" href="{{ p.url }}" target="_blank" rel="noopener">
    <img src="{{ p.image | relative_url }}" alt="Representative figure for {{ p.title }}">
  </a>
  {% endif %}
  <div class="publication-info">
    <div class="pubtitle"><a href="{{ p.url }}" target="_blank" rel="noopener">{{ p.title }}</a></div>
    <div class="pubauthors">{{ p.authors }}</div>
    <div class="meta">{{ p.venue }}{% if p.doi %} · <a href="https://doi.org/{{ p.doi }}" target="_blank" rel="noopener">doi:{{ p.doi }}</a>{% endif %}</div>
  </div>
</article>
{% endfor %}
</div>
{% endfor %}

<p class="publication-note">To add a representative figure, add an image path to the <code>image</code> field for the corresponding publication in <code>_data/publications.yml</code>. Publications without an image automatically use the text-only layout.</p>
