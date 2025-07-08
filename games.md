---
layout: default
title: Games
permalink: /games/
---

<style>
  .games-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 4rem;
    padding: 4rem 2rem;
  }

  .game-entry {
    width: 100%;
    max-width: 960px;
    opacity: 0;
    transform: translateY(40px);
    transition: opacity 1s ease, transform 1s ease;
  }

  .game-entry.visible {
    opacity: 1;
    transform: translateY(0);
  }

  .game-title {
    text-align: center;
    font-size: 2rem;
    font-weight: 600;
    margin-bottom: 1rem;
    color: #ffffff; /* Blanc */
  }

  .game-video {
    width: 100%;
    aspect-ratio: 16/9;
    object-fit: cover;
    border-radius: 16px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.5);
    cursor: pointer;
    transition: transform 0.3s;
  }

  .game-video:hover {
    transform: scale(1.01);
  }

  .tag-container {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    justify-content: center;
    margin-top: 1rem;
  }

  .tag {
    background-color: #333;
    color: #ffffff; /* Blanc */
    font-size: 0.9rem;
    padding: 0.4rem 0.8rem;
    border-radius: 12px;
    font-weight: 500;
  }
</style>

<div class="games-container">

  <div class="game-entry" data-fade>
    <div class="game-title">Terminus</div>
    <a href="{{ '/games/terminus/' | relative_url }}">
      <video
        class="game-video"
        src="{{ '/assets/WEB_Terminus_Pres.mp4' | relative_url }}"
        muted
        loop
        preload="metadata"
        onmouseenter="this.play()"
        onmouseleave="this.pause()"
      ></video>
    </a>
    <div class="tag-container">
      <div class="tag">3rd Person</div>
      <div class="tag">Blueprint</div>
      <div class="tag">Game Jam</div>
    </div>
  </div>

  <div class="game-entry" data-fade>
    <div class="game-title">The Diig</div>
    <a href="{{ '/games/thediig/' | relative_url }}">
      <video
        class="game-video"
        src="{{ '/assets/WEB_TheDiig_Pres.mp4' | relative_url }}"
        muted
        loop
        preload="metadata"
        onmouseenter="this.play()"
        onmouseleave="this.pause()"
      ></video>
    </a>
    <div class="tag-container">
      <div class="tag">2.5D</div>
      <div class="tag">C++</div>
      <div class="tag">Puzzle</div>
    </div>
  </div>

  <div class="game-entry" data-fade>
    <div class="game-title">Squeaky Clean</div>
    <a href="{{ '/games/squeaky/' | relative_url }}">
      <video
        class="game-video"
        src="{{ '/assets/WEB_Squeaky_Pres.mp4' | relative_url }}"
        muted
        loop
        preload="metadata"
        onmouseenter="this.play()"
        onmouseleave="this.pause()"
      ></video>
    </a>
    <div class="tag-container">
      <div class="tag">Side Scroller</div>
      <div class="tag">Solo Project</div>
      <div class="tag">Funny</div>
    </div>
  </div>

  <div class="game-entry" data-fade>
    <div class="game-title">Giggle Heist</div>
    <a href="{{ '/games/giggle/' | relative_url }}">
      <video
        class="game-video"
        src="{{ '/assets/WEB_Giggle_Pres.mp4' | relative_url }}"
        muted
        loop
        preload="metadata"
        onmouseenter="this.play()"
        onmouseleave="this.pause()"
      ></video>
    </a>
    <div class="tag-container">
      <div class="tag">AI</div>
      <div class="tag">C++</div>
      <div class="tag">Maze</div>
    </div>
  </div>

</div>

<script>
  // Fade-in on scroll
  const fadeElements = document.querySelectorAll('[data-fade]');

  function handleFadeIn() {
    fadeElements.forEach(el => {
      const rect = el.getBoundingClientRect();
      const windowHeight = window.innerHeight || document.documentElement.clientHeight;
      if (rect.top < windowHeight - 100) {
        el.classList.add('visible');
      }
    });
  }

  window.addEventListener('scroll', handleFadeIn);
  window.addEventListener('load', handleFadeIn);
</script>
