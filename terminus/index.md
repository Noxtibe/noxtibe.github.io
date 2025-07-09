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
    max-width: 960px;
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
    autoplay
    loop
    playsinline
    controls
  ></video>

  <div class="game-description">
    <strong>Pitch :</strong> Terminus is a survival-horror game where the player has to explore a mysterious train station overrun by shadowy creatures, gather resources, and unravel the mystery of their origin while trying to escape.
  </div>

  <div class="role-description">
    <strong>My Role :</strong> I worked on the core gameplay systems in Unreal Engine 5 using C++. I was responsible for the shooting mechanics, the inventory system, the dynamic lighting interactions, and the enemy AI behavior.
  </div>

</div>
