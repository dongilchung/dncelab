---
layout: default
title: People
permalink: /people/
---
<h1>People</h1><h2>Lab Members</h2><div class="people">{% assign members=site.people|where:'status','current'|sort:'order' %}{% for p in members %}<div class="person">{% if p.image %}<img class="photo" src="{{p.image|relative_url}}" alt="{{p.name}}">{% else %}<div class="photo"></div>{% endif %}<div class="name"><a href="{{p.url|relative_url}}">{{p.name}}</a></div><div>{{p.role}}</div><div class="meta">{{p.affiliation}}</div>{% if p.email %}<div class="meta">{{p.email}}</div>{% endif %}</div>{% endfor %}</div><h2>Alumni</h2><div class="alumni">{% assign alumni=site.people|where:'status','alumni'|sort:'name' %}{% for p in alumni %}<div><b>{{p.name}}</b><br><span class="meta">{{p.role}} · {{p.affiliation}}</span></div>{% endfor %}</div>
