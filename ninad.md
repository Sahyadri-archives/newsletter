---
layout: page
title: Ninad
subtitle: Click on thumbnail to open the album
---

<style>
  .pdf-grid-container {
    display: flex;
    flex-wrap: wrap;
    gap: 25px;
    justify-content: center;
    padding: 20px 0;
  }

  .ninad-card {
    width: 200px; /* Fixed width for uniformity */
    text-align: center;
    transition: transform 0.2s;
  }

  .ninad-card:hover {
    transform: translateY(-5px);
  }

  /* Ensures the thumbnail inside the include fits the container */
  .ninad-card img {
    width: 100%;
    height: 280px; /* Fixed height for consistent alignment */
    object-fit: cover;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  }

  .ninad-caption {
    margin-top: 12px;
    font-weight: 600;
    color: #333;
    font-size: 1.1rem;
  }
</style>

<div class="pdf-grid-container">

  <figure class="ninad-card">
    {% include pdf.html thumbnail_path="/assets/Ninads/17.png" pdf_path="/assets/Ninads/ninad_2017.pdf" %}
    <figcaption class="ninad-caption">Ninad 2017</figcaption>
  </figure>

  <figure class="ninad-card">
    {% include pdf.html thumbnail_path="/assets/Ninads/19-20.png" pdf_path="/assets/Ninads/Ninad_2019-20.pdf" %}
    <figcaption class="ninad-caption">Ninad 2019-20</figcaption>
  </figure>

  <figure class="ninad-card">
    {% include pdf.html thumbnail_path="/assets/Ninads/20-21.png" pdf_path="/assets/Ninads/Ninad 2020-21.pdf" %}
    <figcaption class="ninad-caption">Ninad 2020-21</figcaption>
  </figure>

  <figure class="ninad-card">
    {% include pdf.html thumbnail_path="/assets/Ninads/23-24.png" pdf_path="/assets/Ninads/Ninad_2023-24.pdf" %}
    <figcaption class="ninad-caption">Ninad 2023-24</figcaption>
  </figure>

</div>
