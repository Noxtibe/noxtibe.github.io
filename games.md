---
layout: default
title: Games
permalink: /games/
---

<style>
  .games-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
    padding: 2rem 0;
  }

  .game-card {
    width: 300px;
    border-radius: 16px;
    overflow: hidden;
    background-color: #1f1f1f;
    box-shadow: 0 4px 8px rgba(0,0,0,0.3);
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
</style>

<div class="games-grid">

  {% assign games = "WEB_Terminus_Pres,WEB_TheDiig_Pres,WEB_Squeaky_Pres,WEB_Giggle_Pres" | split: "," %}
  {% for game in games %}
    <div class="game-card">
      <video
        class="game-video"
        src="{{ '/assets/' | append: game | append: '.mp4' | relative_url }}"
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
    </div>
  {% endfor %}

</div>
