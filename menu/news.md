---
layout: default
title: News
permalink: /news/
---

<h1 class="news-title">News</h1>

<div class="news-container">
  {% for post in site.posts %}
    <div class="news-post">
      <h2 class="post-title">{{ post.title }}</h2>
      <div class="post-meta">{{ post.date | date: "%B %d, %Y" }}</div>
      {% if post.description %}
        <p class="post-description">{{ post.description }}</p>
      {% endif %}
      {% if post.images %}
        <div class="post-images">
          {% for image in post.images %}
            <img src="{{ image }}" alt="{{ post.title }} image">
          {% endfor %}
        </div>
      {% endif %}
    </div>
    <hr class="post-divider">
  {% endfor %}
</div>