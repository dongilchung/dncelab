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
<article class="publication-item">
  <div class="publication-thumb">
    {% if p.image and p.image != "" %}
    <a href="{{ p.url }}" target="_blank" rel="noopener">
      <img src="{{ '/assets/images/publication_images/' | append: p.image | relative_url }}" alt="Representative figure for {{ p.title }}">
    </a>
    {% endif %}
  </div>
  <div class="publication-info">
    <div class="pubtitle"><a href="{{ p.url }}" target="_blank" rel="noopener">{{ p.title }}</a></div>
    <div class="pubauthors">{{ p.authors }}</div>
    <div class="meta">{{ p.venue }}{% if p.doi and p.doi != "" %} · <a href="https://doi.org/{{ p.doi }}" target="_blank" rel="noopener">doi:{{ p.doi }}</a>{% endif %}</div>
  </div>
</article>
{% endfor %}
</div>
{% endfor %}

<p class="publication-note">To add a representative figure, upload the image to <code>assets/images/publication_images/</code> and enter only its filename in the corresponding <code>image</code> field in <code>_data/publications.yml</code>, for example <code>image: "my-paper.jpg"</code>. Leave the field empty when no figure is available.</p>
