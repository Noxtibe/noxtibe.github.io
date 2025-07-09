---
layout: default
title: Terminus
permalink: /games/terminus/
---

<style>
  .game-detail-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 4rem 2rem;
    max-width: 1200px;
    margin: 0 auto;
    text-align: center;
  }

  .game-detail-title {
    font-size: 2.5rem;
    color: #ffffff;
    margin-bottom: 2rem;
  }

  .game-detail-video {
    width: 100%;
    max-width: 100%;
    height: auto;
    aspect-ratio: 16 / 9;
    border-radius: 16px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.5);
    margin-bottom: 2rem;
  }

  .game-description, .role-description {
    color: #ffffff;
    font-size: 1.2rem;
    line-height: 1.8;
    margin-bottom: 2rem;
    text-align: left;
  }

  @media (max-width: 768px) {
    .game-detail-container {
      padding: 2rem 1rem;
    }

    .game-detail-title {
      font-size: 2rem;
    }

    .game-description, .role-description {
      font-size: 1rem;
      text-align: left;
    }
  }
</style>

<div class="game-detail-container">

  <div class="game-detail-title">Terminus</div>

  <video
    class="game-detail-video"
    src="{{ '/assets/WEB_Terminus_Trailer.mp4' | relative_url }}"
    muted
    loop
    playsinline
    controls
  ></video>

  <div class="game-description">
    <strong>Pitch :</strong> Paris, 1968, as the city descends into social chaos, a much darker threat emerges from the depths. Charles MERCIER, a former soldier recruited by a secret organisation, is sent into the metro to stop an impending disaster.
  </div>

  <div class="role-description">
    <strong>My Role :</strong> On this project, I worked on the weapon reloading system, a system for controlling the game's lights in real time and a dialogue system.
    I also did almost all the VFX, helped with optimisation, debugging, and much more.
  </div>

</div>
