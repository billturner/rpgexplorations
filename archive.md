---
title: Archive of posts
layout: base
---

<h2>Posts by Category<h2>

{% for category in site.categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %}
  <h3 id="posts-{{ category_name | slugify }}">{{ category_name }}</h3>
  <ul>
    {% for post in site.categories[category_name] %}
      <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%b. %-d, %Y" }})</li>
    {% endfor %}
  </ul>
{% endfor %}

<h2>Posts by Tag<h2>

{% for tag in site.tags %}
  {% capture tag_name %}{{ tag | first }}{% endcapture %}
  <h3 id="posts-{{ tag_name | slugify }}">#{{ tag_name }}</h3>
  <ul>
    {% for post in site.tags[tag_name] %}
      <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%b. %-d, %Y" }})</li>
    {% endfor %}
  </ul>
{% endfor %}

<h2>Posts by Published Date</h2>

<ul>
  {% for post in site.posts %}
    <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%b. %-d, %Y" }})</li>
  {% endfor %}
</ul>
