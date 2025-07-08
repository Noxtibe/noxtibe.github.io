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
    padding: 2rem 1rem;
  }

  .game-entry {
    opacity: 0;
    transform: translateY(40px);
    transition: opacity 1s ease-out, transform 1s ease-out;
    max-width: 900px;
    width: 100%;
    text-align: center;
  }

  .game-entry.visible {
    opacity: 1;
    transform: translateY(0);
  }

  .game-title {
    font-size: 2.2rem;
    font-weight: 600;
    color: #ffffff;
    margin-bottom: 1rem;
  }

  .game-video {
    width: 100%;
    border-radius: 16px;
    object-fit: cover;
    aspect-ratio: 16 / 9;
    cursor: pointer;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
    transition: transform 0.3s ease;
  }

  .game-video:hover {
    transform: scale(1.01);
  }

  .tag-container {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: 1rem;
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

<div class="games-container">
  {% assign games = 
    site.pages | where_exp: "page", "page.categories contains 'game'" 
  %}
  {% for game in games %}
    <div class="game-entry">
      <h2 class="game-title">{{ game.title }}</h2>
      <a href="{{ game.url | relative_url }}">
        <video
          class="game-video"
          src="{{ '/assets/' | append: game.video | relative_url }}"
          muted
          loop
          preload="metadata"
          onmouseenter="this.play()"
          onmouseleave="this.pause()"
        ></video>
      </a>
      <div class="tag-container">
        {% for tag in game.tags %}
          <div class="tag">{{ tag }}</div>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
</div>

<script>
  // Fade-in on scroll
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.game-entry').forEach(entry => {
    observer.observe(entry);
  });
</script>
