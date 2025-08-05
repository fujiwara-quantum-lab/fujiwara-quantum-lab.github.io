---
layout: default
title: News
permalink: /news/
---

# All News

{% for post in site.posts %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
  <hr>
{% endfor %}