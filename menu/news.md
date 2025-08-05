---
layout: default
title: News
permalink: /news/
---

<h1 class="news-title">News</h1>

<div class="news-container">
{% for post in site.posts %}  
	{{ post.content }}
	<hr class="post-divider">
{% endfor %}
</div>