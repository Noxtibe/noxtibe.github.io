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
    gap: 4rem;
    padding: 3rem 1rem;
  }

  .game-wrapper {
    width: 100%;
    max-width: 900px;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .game-title {
    font-size: 2rem;
    font-weight: 600;
    margin-bottom: 1rem;
    color: #FFA500;
  }

  .game-card {
    width: 100%;
    border-radius: 16px;
    overflow: hidden;
    background-color: #1f1f1f;
    box-shadow: 0 4px 8px rgba(0,0,0,0.3);
    text-decoration: none;
    transition: transform 0.3s ease;
  }

  .game-card:hover {
    transform: scale(1.01);
  }

  .game-video {
    width: 100%;
    aspect-ratio: 16 / 9;
    object-fit: cover;
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
    .game-title {
      font-size: 1.5rem;
    }

    .game-video {
      aspect-ratio: 1 / 1;
    }
  }
</style>

<div class="games-grid">

  <div class="game-wrapper">
    <div class="game-title">Terminus</div>
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
    </a>
    <div class="tag-container">
      <div class="tag">3rd Person</div>
      <div class="tag">Blueprint</div>
      <div class="tag">Game Jam</div>
    </div>
  </div>

  <div class="game-wrapper">
    <div class="game-title">The Diig</div>
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
    </a>
    <div class="tag-container">
      <div class="tag">2.5D</div>
      <div class="tag">C++</div>
      <div class="tag">Narrative</div>
    </div>
  </div>

  <div class="game-wrapper">
    <div class="game-title">Squeaky</div>
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
    </a>
    <div class="tag-container">
      <div class="tag">Platformer</div>
      <div class="tag">Unreal</div>
      <div class="tag">Puzzle</div>
    </div>
  </div>

  <div class="game-wrapper">
    <div class="game-title">Giggle</div>
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
    </a>
    <div class="tag-container">
      <div class="tag">Multiplayer</div>
      <div class="tag">Blueprint</div>
      <div class="tag">Action</div>
    </div>
  </div>

</div>
