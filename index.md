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


