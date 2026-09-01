---
layout: default
title: Publications
permalink: /publications/
---

<h1>Publications</h1>

{% assign pubs = site.publications | sort: "year" | reverse %}
{% assign current_year = "" %}

<div class="publication-list">
{% for publication in pubs %}
  {% if publication.year != current_year %}
    {% assign current_year = publication.year %}
    <section class="pub-year">
      <h2 class="year-heading">{{ current_year }}</h2>
  {% endif %}

      <article class="pub">
        <div class="pub-title"><a href="{{ publication.link }}" target="_blank" rel="noopener">{{ publication.title }}</a></div>
        <div class="pub-authors">{{ publication.authors }}</div>
        <div class="pub-meta">{{ publication.venue }}{% if publication.doi %} · <a href="https://doi.org/{{ publication.doi }}" target="_blank" rel="noopener">doi:{{ publication.doi }}</a>{% endif %}</div>
      </article>

  {% assign next_index = forloop.index0 | plus: 1 %}
  {% assign next_pub = pubs[next_index] %}
  {% if next_pub.year != current_year or forloop.last %}
    </section>
  {% endif %}
{% endfor %}
</div>
