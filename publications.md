---
layout: default
title: Publications
permalink: /publications/
---
<h1>Publications</h1>{% assign pubs=site.publications|sort:'year'|reverse %}{% assign y='' %}{% for p in pubs %}{% if p.year != y %}{% assign y=p.year %}<h2>{{y}}</h2>{% endif %}<article class="pub"><div class="pubtitle"><a href="{{p.link}}" target="_blank" rel="noopener">{{p.title}}</a></div><div>{{p.authors}}</div><div class="meta">{{p.venue}}{% if p.doi %} · <a href="https://doi.org/{{p.doi}}" target="_blank">doi:{{p.doi}}</a>{% endif %}</div></article>{% endfor %}
