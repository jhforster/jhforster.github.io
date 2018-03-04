---
layout: base
title: Writing
tagline: Thoughts I felt compelled to express
---

{% for item in site.writing %}
  <h1><a href="{{ item.url }}">{{ item.title }}</a></h1>
  <p class="writing-description">{{ item.description }}</p>
{% endfor %}
