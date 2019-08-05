---
layout: base
title: Archive
---
# Most common tags

{% capture tags %}
  {% for tag in site.tags %}
    {{ tag[1].size | plus: 1000 }}#{{ tag[0] }}#{{ tag[1].size }}
  {% endfor %}
{% endcapture %}
{% assign sortedtags = tags | split:' ' | sort %}
{% for tag in sortedtags reversed %}
  {% assign tagitems = tag | split: '#' %}
  <div class="post-tag">
    <a href="#{{ tagitems[1] | slugify }}" class="tag-link">#{{ tagitems[1] }} ({{ tagitems[2] }})</a>
  </div>
{% endfor %}

<hr>

<!-- I should see if there is a way to nest this bottom loop above so I can get post count here too -->

{% for tag in site.tags %}
  <h3>#{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
  <hr>
{% endfor %}
