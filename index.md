---
layout: default
title: Home
permalink: /
---
# Welcome!
We are a new experimental atomic physics group in the Physics Department at Lehigh University. 
We utilize the exquisite precision and control of atomic systems to sythesize gases of ultracold bosonic and fermionic atoms in order to investigate exotic behavior in 
 quantum many-body systems.

**We are currently looking for motivated undergraduate, graduate, and postdocs to join us in constructing the laboratory
and participate in cutting edge research.** See [openings]({/openings}) for more details.


<!-- Swiper CSS -->
<link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.min.css" />

<style>
  .swiper-container {
    width: 50%;
    max-width: 800px;
    margin: auto;
  }
  .swiper-slide img {
    width: 100%;
    height: auto;
    display: block;
    border-radius: 10px;
  }
</style>

<!-- Swiper Carousel -->
<div class="swiper-container">
  <div class="swiper-wrapper" id="swiper-wrapper">
    <!-- Slides will be inserted here -->
  </div>
  <!-- Pagination (dots) -->
  <div class="swiper-pagination"></div>
  <!-- Navigation arrows -->
  <div class="swiper-button-next"></div>
  <div class="swiper-button-prev"></div>
</div>

<!-- Swiper JS -->
<script src="https://unpkg.com/swiper/swiper-bundle.min.js"></script>

<script>
  // Image filenames located in /assets/img/gallery_1/
  const imageFilenames = [
    "lehigh.webp",
    "lewis_lab_2.jpg"
  ];

  // Sort alphabetically
  imageFilenames.sort();

  const wrapper = document.getElementById('swiper-wrapper');
  imageFilenames.forEach(filename => {
    const slide = document.createElement('div');
    slide.className = 'swiper-slide';
    slide.innerHTML = `<img src="/assets/img/gallery_1/${filename}" alt="${filename}" />`;
    wrapper.appendChild(slide);
  });

  // Initialize Swiper
  new Swiper('.swiper-container', {
    loop: true,
    slidesPerView: 1,
    spaceBetween: 10,
    pagination: {
      el: '.swiper-pagination',
      clickable: true
    },
    navigation: {
      nextEl: '.swiper-button-next',
      prevEl: '.swiper-button-prev'
    }
  });
</script>

### key research topics, themes, and ideas :
ultracold atoms, bose condensation, degenerate fermi gases, optical lattices, quantum simulation,
non-equilibirum physics, quantum thermalization, floquet engineering, disordered system, laser cooling
