---
layout: default
title: Home
permalink: /
---
# Welcome to the Fujiwara Lab!

{% assign images = site.data.gallery_1 %}

{% capture home_text %}
We are a new experimental atomic physics group in the Physics Department at Lehigh University.  
We utilize the exquisite precision and control of atomic systems to synthesize gases of ultracold bosonic and fermionic atoms in order to investigate exotic behavior in quantum many-body systems.

<ins>**We have multiple openings for highly motivated undergraduates, graduates, and postdocs to join us in constructing the laboratory and participate in cutting-edge research.**</ins> See [openings](/openings/) for more details.

### Key research topics, themes, and ideas
ultracold atoms, Bose condensation, degenerate Fermi gases, optical lattices, quantum simulation, non-equilibrium physics, quantum thermalization, Floquet engineering, disordered systems, laser cooling
{% endcapture %}

{% include carousel.html
   images=images
   folder="gallery_1"
   id="home-carousel"
   text_position="left"
   max_width="600px"
   max_height="400px"
   text=home_text
%}
## Want to learn more?

Our group is part of AMO group and the thriving research community at large at Lehigh University. For more cold atoms at Lehigh, please see the [**Sommer lab**](https://sites.google.com/lehigh.edu/sommerlab/home){: .link-blue target="_blank"} . And for a more complete listing please see the [**Department of Physics**](https://physics.cas.lehigh.edu/research){: .link-blue target="_blank"} website.

Please explore this website to learn more about what we do.  If you are new the field and/or group, you may find the Resources section particularly helpful.


## Recent News

<div class="home-news">
{% for post in site.posts limit:10 %}
  <div class="home-news-item">
    <a class="home-news-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="home-news-date">({{ post.date | date: "%B %d, %Y" }})</span>
  </div>
{% endfor %}
</div>

<p><a href="{{ '/news/' | relative_url }}">More news →</a></p>