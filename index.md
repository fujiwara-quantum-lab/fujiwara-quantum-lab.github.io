---
layout: default
title: Home
permalink: /
---
# Welcome to the Fujiwara Lab!
{% assign images = site.data.gallery_1 %}
{% capture carousel_text %}
  {% include carousel_texts/home.md %}
{% endcapture %}

{% include carousel.html
   images=images
   folder="gallery_1"
   id="home-carousel"
   text_position="left"
   max_width="600px"
   max_height="400px"
   text=carousel_text
%}

<section class="recent-news-section">
  <h2>Recent News</h2>
  <div class="news-grid">
    {% assign recent_posts = site.posts | limit: 3 %}
    {% for post in recent_posts %}
      <article class="news-card">
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
        <a href="{{ post.url }}" class="read-more">Read More →</a>
      </article>
    {% endfor %}
  </div>
  <div class="more-news-button">
    <a href="{{ site.github.url }}/news/">More News</a>
  </div>
</section>

