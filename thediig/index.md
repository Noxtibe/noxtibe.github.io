---
layout: default
title: The Diig
permalink: /games/thediig/
---

<style>
  .game-detail-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 4rem 2rem;
    max-width: 1400px;
    margin: 0 auto;
    text-align: center;
  }

  .game-detail-title {
    font-size: 3.5rem;
    color: #ffffff;
    margin-bottom: 1rem;
  }

  .game-links {
    margin-bottom: 2.5rem;
    font-size: 1.3rem;
    color: #ffffff;
    display: flex;
    gap: 1.5rem;
    flex-wrap: wrap;
    justify-content: center;
  }

  .game-links a {
    text-decoration: none;
    color: #ffffff;
    font-weight: 700;
    transition: color 0.3s ease, transform 0.3s ease;
  }

  .game-links a:hover {
    color: #FFA500;
    transform: scale(1.1);
  }

  .game-detail-image {
    width: 100%;
    max-width: 100%;
    height: auto;
    object-fit: contain;
    border-radius: 16px;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.6);
    margin-bottom: 3rem;
  }

  .game-description,
  .role-description {
    color: #ffffff;
    font-size: 1.3rem;
    line-height: 2;
    margin-bottom: 2.5rem;
    text-align: left;
    max-width: 960px;
  }

  .game-description strong,
  .role-description strong {
    color: #FFA500;
    font-size: 1.6rem;
    display: block;
    margin-bottom: 0.5rem;
  }

  @media (max-width: 768px) {
    .game-detail-container {
      padding: 2rem 1rem;
    }

    .game-detail-title {
      font-size: 2.2rem;
    }

    .game-links {
      font-size: 1.1rem;
      flex-direction: column;
      gap: 0.5rem;
    }

    .game-description,
    .role-description {
      font-size: 1rem;
    }

    .game-description strong,
    .role-description strong {
      font-size: 1.3rem;
    }
  }
</style>

<div class="game-detail-container">

  <div class="game-detail-title">The Diig</div>

  <div class="game-links">
    <a href="https://www.mediafire.com/file/6t5q0t03hcw3ue4/The_Diig.rar/file" target="_blank">Download</a>
  </div>

  <img
    class="game-detail-image"
    src="{{ '/assets/WEB_TheDiig_Image.png' | relative_url }}"
    alt="The Diig Screenshot"
  />

  <div class="game-description">
    <strong>Pitch :</strong>
    Our hero, transported to the edge of the galaxy by a mysterious asteroid, finds himself separated from the rest of his team. 
    He will have to solve the mysteries surrounding an enigmatic civilisation in order to find the answers.
  </div>

  <div class="role-description">
    <strong>My Role :</strong>
    The aim of this project was to remake The Dig (game released in 1995) in 3D in just 3 weeks. As part of a team of around ten people.
    It was also our first team project on Unreal Engine 5.
    I worked on the interaction, inventory and inspection system. I also did a large part of the game's VFX.
  </div>

</div>

