---
layout: default
title: "We are here!"
author: "Cora Fujiwara"
categories: journal
image: Admissions-VirtualTour-Hero.jpg
---

 <div class="news-post">
      <h2 class="post-title">{{ page.title }}</h2>
      <div class="post-meta">{{ page.date | date: "%B %d, %Y" }}</div>
      {% if page.description %}
        <p class="post-description">{{ page.description }}</p>
      {% endif %}
      {% if page.images %}
        <div class="post-images">
          {% for image in page.images %}
            <img src="{{ image }}" alt="{{ page.title }} image">
          {% endfor %}
        </div>
      {% endif %}
    </div>

	

Cora is getting situated at Lehigh, and research activities will begin soon! Lab renovations are underway and 
a temporary lab space has been acquired. 

The group is actively recruiting personnel at the undergraduate, graduate, and postdoc level. If you are interested 
in joining the group to help build the lab and do cutting edge research please email Cora directly.  More information about openings may be found on the openings page and the recruitment pages for the university.