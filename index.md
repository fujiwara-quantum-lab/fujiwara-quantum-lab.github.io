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
  .carousel-layout {
    display: flex;
    gap: 2rem;
    align-items: center;
    margin: 2rem 0;
    flex-wrap: wrap;
  }

  .carousel-text {
    flex: 1;
    min-width: 250px;
    max-width: 50%;
    font-size: 1rem;
    line-height: 1.6;
  }

  .carousel-wrapper {
    flex: 1;
    max-width: 50%;
  }

  .swiper {
    border-radius: 12px;
    overflow: hidden;
    width: 100%;
  }

  .swiper-slide figure {
    margin: 0;
    text-align: center;
  }

  .swiper-slide img {
    max-width: 100%;
    max-height: 400px;
    object-fit: contain;
    display: block;
    margin: 0 auto;
    border-radius: 10px;
  }

  .swiper-slide figcaption {
    font-size: 0.9rem;
    text-align: center;
    margin-top: 0.5rem;
    color: #555;
  }

  .swiper-button-next,
  .swiper-button-prev {
    color: #333;
    top: 50%;
    width: 30px;
    height: 30px;
    margin-top: -15px;
    transform: scale(0.75);
  }

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

<div class="carousel-layout">
  <div class="carousel-text">
    We are a new experimental atomic physics group in the Physics Department at Lehigh University. 
    We utilize the exquisite precision and control of atomic systems to synthesize gases of ultracold bosonic and fermionic atoms 
    in order to investigate exotic behavior in quantum many-body systems.
  </div>

  <div class="carousel-wrapper">
    <div class="swiper" id="single-swiper-carousel">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <figure>
            <img src="/assets/img/gallery_1/lehigh.webp" alt="Lehigh University campus">
            <figcaption>Lehigh University campus</figcaption>
          </figure>
        </div>
        <div class="swiper-slide">
          <figure>
            <img src="/assets/img/gallery_1/lewis_lab_2.jpg" alt="Lewis Lab and Mountaintop Campus">
            <figcaption>Lewis Lab and Mountaintop Campus</figcaption>
          </figure>
        </div>
      </div>

      <div class="swiper-button-next"></div>
      <div class="swiper-button-prev"></div>
      <div class="swiper-pagination"></div>
    </div>
  </div>
</div>

<!-- Swiper JS -->
<script src="https://unpkg.com/swiper/swiper-bundle.min.js"></script>
<script>
  document.addEventListener("DOMContentLoaded", function () {
    if (!document.getElementById("single-swiper-carousel").classList.contains("swiper-initialized")) {
      new Swiper("#single-swiper-carousel", {
        loop: true,
        slidesPerView: 1,
        spaceBetween: 10,
        pagination: {
          el: "#single-swiper-carousel .swiper-pagination",
          clickable: true
        },
        navigation: {
          nextEl: "#single-swiper-carousel .swiper-button-next",
          prevEl: "#single-swiper-carousel .swiper-button-prev"
        }
      });
    }
  });
</script>

### key research topics, themes, and ideas :
ultracold atoms, bose condensation, degenerate fermi gases, optical lattices, quantum simulation,
non-equilibirum physics, quantum thermalization, floquet engineering, disordered system, laser cooling
