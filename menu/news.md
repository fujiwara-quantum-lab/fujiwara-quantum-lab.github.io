---
layout: default
title: News
permalink: /news/
---

# All News

<ul class="news-list">
  {% for post in site.posts %}
    <li class="news-item">
      <h2>{{ post.title }}</h2>
      <div class="news-content">
        {{ post.content }}
      </div>
    </li>
  {% endfor %}
</ul>