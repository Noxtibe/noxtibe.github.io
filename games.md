---
layout: default
title: Games
permalink: /games/
---

<style>
  .games-grid {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 3rem;
    padding: 3rem 1rem;
  }

  .game-card {
    width: 400px;
    border-radius: 16px;
    overflow: hidden;
    background-color: #1f1f1f;
    box-shadow: 0 4px 8px rgba(0,0,0,0.3);
    text-decoration: none;
    transition: transform 0.3s ease;
  }

  .game-card:hover {
    transform: scale(1.02);
  }

  .game-video {
    width: 100%;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    border-radius: 16px 16px 0 0;
    cursor: pointer;
    display: block;
  }

  .tag-container {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    padding: 1rem;
    justify-content: center;
  }

  .tag {
    background-color: #333;
    color: #FFA500;
    font-size: 0.9rem;
    padding: 0.4rem 0.8rem;
    border-radius: 12px;
    font-weight: 500;
  }

  @media (max-width: 768px) {
    .game-card {
      width: 90%;
    }
  }
</style>

<div class="games-grid">

  <a class="game-card" href="{{ '/games/terminus/' | relative_url }}">
    <video
      class="game-video"
      src="{{ '/assets/WEB_Terminus_Pres.mp4' | relative_url }}"
      muted
      loop
      preload="metadata"
      onmouseenter="this.play()"
      onmouseleave="this.pause(); this.currentTime = 0;"
    ></video>
    <div class="tag-container">
      <div class="tag">3rd Person</div>
      <div class="tag">Blueprint</div>
      <div class="tag">Game Jam</div>
    </div>
  </a>

  <a class="game-card" href="{{ '/games/thediig/' | relative_url }}">
    <video
      class="game-video"
      src="{{ '/assets/WEB_TheDiig_Pres.mp4' | relative_url }}"
      muted
      loop
      preload="metadata"
      onmouseenter="this.play()"
      onmouseleave="this.pause(); this.currentTime = 0;"
    ></video>
    <div class="tag-container">
      <div class="tag">2.5D</div>
      <div class="tag">C++</div>
      <div class="tag">Narrative</div>
    </div>
  </a>

  <a class="game-card" href="{{ '/games/squeaky/' | relative_url }}">
    <video
      class="game-video"
      src="{{ '/assets/WEB_Squeaky_Pres.mp4' | relative_url }}"
      muted
      loop
      preload="metadata"
      onmouseenter="this.play()"
      onmouseleave="this.pause(); this.currentTime = 0;"
    ></video>
    <div class="tag-container">
      <div class="tag">Platformer</div>
      <div class="tag">Unreal</div>
      <div class="tag">Puzzle</div>
    </div>
  </a>

  <a class="game-card" href="{{ '/games/giggle/' | relative_url }}">
    <video
      class="game-video"
      src="{{ '/assets/WEB_Giggle_Pres.mp4' | relative_url }}"
      muted
      loop
      preload="metadata"
      onmouseenter="this.play()"
      onmouseleave="this.pause(); this.currentTime = 0;"
    ></video>
    <div class="tag-container">
      <div class="tag">Multiplayer</div>
      <div class="tag">Blueprint</div>
      <div class="tag">Action</div>
    </div>
  </a>

</div>
