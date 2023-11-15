---
title: Archive of posts
layout: base
---

Posts by tag:
<ul>
{% for tag in site.tags %}
  {% assign t = tag | first %}
  <li><a href="tag/{{ t | slugify }}/">{{ t }}</a></li>
{% endfor %}
</ul>

Posts by category:
<ul>
{% for category in site.categories %}
  {% assign c = category | first %}
  <li><a href="category/{{ c | slugify }}/">{{ c }}</a></li>
{% endfor %}
</ul>
