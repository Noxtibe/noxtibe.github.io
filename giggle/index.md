---
layout: default
title: Giggle Heist
permalink: /games/giggle/
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
    aspect-ratio: 16 / 9;
    object-fit: cover;
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

  <div class="game-detail-title">Giggle Heist</div>

  <div class="game-links">
    <a href="https://elbaz-melina.itch.io/giggleheist" target="_blank">Download on Itch.io</a>
  </div>

  <img
    class="game-detail-image"
    src="{{ '/assets/WEB_Giggle_Image.jpg' | relative_url }}"
    alt="Giggle Heist Screenshot"
  />

  <div class="game-description">
    <strong>Pitch :</strong>
    Giggle Heist is a two players game where you have to rob a bank without arms!  
    Steal as much money as you can with your lifelong slime accomplice!  
    But be careful not to be betrayed by him...
  </div>

  <div class="role-description">
    <strong>My Role :</strong>
    This game was made in 48h. I mainly worked on the camera and the movements of the 2 players. I also did the VFX.
  </div>

</div>
