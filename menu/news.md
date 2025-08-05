---
layout: default
title: News
permalink: /news/
---

<h1 class="news-title">News</h1>

<div class="news-container">
  {% for post in site.posts %}
    {% case post.format %}
      {% when "side_carousel" %}
        {% include news/side_carousel.html post=post %}
      {% when "text" %}
        {% include news/text.html post=post %}
      {% else %}
        {% include news/text.html post=post %}
    {% endcase %}
    <hr class="post-divider">
  {% endfor %}
</div>