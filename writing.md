---
layout: base
title: Writing
---

{% assign writing = site.writing | reverse %}
{% for item in writing %}
  <h1><a href="{{ item.url }}">{{ item.title }}</a></h1>
  <p>{{ item.description }}</p>
{% endfor %}
