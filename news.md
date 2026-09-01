---
layout: default
title: News
permalink: /news/
---
<h1>News</h1>{% assign news=site.posts|sort:'date'|reverse %}{% for post in news %}<article class="news"><div class="date">{{post.date|date:'%Y.%m.%d'}}</div><h2><a href="{{post.url|relative_url}}">{{post.title}}</a></h2>{{post.content}}</article>{% endfor %}
