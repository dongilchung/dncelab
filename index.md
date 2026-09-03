---
layout: default
title: News
permalink: /
---
<div class="representation-news-wrap">
  <img class="representation-news" src="{{ '/assets/images/representation-news.jpg' | relative_url }}" alt="DNCE Lab">
</div>

<h1>News</h1>
<div class="news-list">
{% assign news = site.data.news | sort: 'date' | reverse %}
{% for item in news limit:3 %}
<article class="news">
  <div class="date">{{ item.date | date: '%Y.%m.%d' }}</div>
  <h2>{{ item.title }}</h2>
  <div class="news-content">{{ item.content | markdownify }}</div>
</article>
{% endfor %}
</div>
