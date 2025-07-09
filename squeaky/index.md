---
layout: default
title: Squeaky
permalink: /games/squeaky/
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

  .game-detail-video {
    width: 100%;
    max-width: 100%;
    height: auto;
    aspect-ratio: 16 / 9;
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

  <div class="game-detail-title">Squeaky Clean</div>

  <div class="game-links">
    <a href="https://miya-loustalot.itch.io/squeaky-clean" target="_blank">Download on Itch.io</a>
  </div>

  <video
    class="game-detail-video"
    src="{{ '/assets/WEB_Squeaky_Gameplay.mp4' | relative_url }}"
    muted
    loop
    playsinline
    controls
  ></video>

  <div class="game-description">
    <strong>Pitch :</strong>
    Get cleaning with Octave the Octopus! Electrical appliances need a fresh scrubbing, rinsing, and maybe a bonus cat delivery before they get happy about your job! 
    Pay attention to the duckies though!
  </div>

  <div class="role-description">
    <strong>My Role :</strong>
    This game was made in 48h. I mainly worked on all the VFX and helped with the programming of the objects that appear, the debugging & more.
  </div>

</div>

