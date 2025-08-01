---
layout: page
title: Research
permalink: /research/
---

<!-- Swiper CSS -->
<link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.min.css" />

<style>
  .carousel-layout {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    align-items: center;
    margin: 2rem 0;
  }

  .carousel-text {
    font-size: 1rem;
    line-height: 1.6;
  }

  .carousel-wrapper {
    width: 100%;
  }

  .swiper {
    border-radius: 12px;
    overflow: hidden;
  }

  .swiper-slide figure {
    margin: 0;
  }

  .swiper-slide img {
    width: 100%;
    height: auto;
    display: block;
    object-fit: contain;
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
    {{ include.text }}
  </div>
  <div class="carousel-wrapper">
    <div class="swiper">
      <div class="swiper-wrapper">
        {% assign sorted_images = include.images | sort: "filename" %}
        {% for image in sorted_images %}
        <div class="swiper-slide">
          <figure>
            <img src="/assets/img/gallery_1/{{ image.filename }}" alt="{{ image.caption }}">
            <figcaption>{{ image.caption }}</figcaption>
          </figure>
        </div>
        {% endfor %}
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
  });
</script>
