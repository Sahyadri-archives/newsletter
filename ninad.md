---
layout: page
title: Ninad
---
<style>
  .pdf-grid-container {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
    padding: 20px 0;
  }

  .ninad-card {
    display: flex;
    flex-direction: column;
    width: 220px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s ease;
    overflow: hidden; /* Keeps the top corners of the green bar rounded */
  }

  .ninad-card:hover {
    transform: translateY(-8px);
  }

  .ninad-caption-banner {
    background-color: #6d8571; /* Matching your site's green */
    color: white;
    padding: 12px 5px;
    text-align: center;
    font-weight: 600;
    font-size: 1rem;
    margin: 0;
  }

  /* Ensures thumbnails are uniform */
  .ninad-card img {
    width: 100%;
    height: 300px; 
    object-fit: cover;
    display: block;
  }
</style>

<div class="pdf-grid-container">

  <figure class="ninad-card">
    <figcaption class="ninad-caption-banner">Ninad 2023-24</figcaption>
    {% include pdf.html thumbnail_path="/assets/Ninads/23-24.png" pdf_path="/assets/Ninads/Ninad_2023-24.pdf" %}
  </figure>

  <figure class="ninad-card">
    <figcaption class="ninad-caption-banner">Ninad 2020-21</figcaption>
    {% include pdf.html thumbnail_path="/assets/Ninads/20-21.png" pdf_path="/assets/Ninads/Ninad 2020-21.pdf" %}
  </figure>

  <figure class="ninad-card">
    <figcaption class="ninad-caption-banner">Ninad 2019-20</figcaption>
    {% include pdf.html thumbnail_path="/assets/Ninads/19-20.png" pdf_path="/assets/Ninads/Ninad_2019-20.pdf" %}
  </figure>

  <figure class="ninad-card">
    <figcaption class="ninad-caption-banner">Ninad 2017</figcaption>
    {% include pdf.html thumbnail_path="/assets/Ninads/17.png" pdf_path="/assets/Ninads/ninad_2017.pdf" %}
  </figure>

</div>
