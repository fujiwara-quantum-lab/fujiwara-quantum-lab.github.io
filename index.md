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

<link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.min.css" />

<style>
  .carousel-wrapper {
    width: 50%;
    max-width: 800px;
    margin: 2rem auto;
    position: relative;
  }

  .swiper {
    border-radius: 12px;
    overflow: hidden;
  }

  .swiper-slide img {
    width: 100%;
    height: auto;
    display: block;
    object-fit: contain;
  }

  /* Tighten arrow placement */
  .swiper-button-next,
  .swiper-button-prev {
    color: #333;
    top: 50%;
    width: 30px;
    height: 30px;
    margin-top: -15px;
    transform: scale(0.75);
  }

  /* Center dots below image */
  .swiper-pagination {
    bottom: 10px !important;
    text-align: center;
  }

  .swiper-pagination-bullets {
    display: flex;
    justify-content: center;
    padding-top: 10px;
  }

  .swiper-pagination-bullet {
    background: #333;
    opacity: 0.4;
  }

  .swiper-pagination-bullet-active {
    opacity: 1;
  }
</style>

<div class="carousel-wrapper">
  <div class="swiper">
    <div class="swiper-wrapper" id="swiper-wrapper">
      <!-- Slides will be injected below -->
    </div>
    <!-- Navigation arrows -->
    <div class="swiper-button-next"></div>
    <div class="swiper-button-prev"></div>
    <!-- Dots -->
    <div class="swiper-pagination"></div>
  </div>
</div>

<!-- Swiper JS -->
<script src="https://unpkg.com/swiper/swiper-bundle.min.js"></script>

<script>
  // Image filenames from /assets/img/gallery_1/
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
  new Swiper('.swiper', {
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
