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

## want to learn more?

Our group is part of AMO group and the thriving research community at large at Lehigh University. For more cold atoms at Lehigh, please see the [**Sommer lab**](https://sites.google.com/lehigh.edu/sommerlab/home) . And for a more complete listing please see the [**department of physics**](https://physics.cas.lehigh.edu/research) website.

Please explore this website to learn more about what we do.  If you are new the field and/or group, you may find the Resources section particularly helpful.
