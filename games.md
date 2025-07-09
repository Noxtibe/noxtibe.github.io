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
    color: #ffffff;
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
    color: #ffffff;
    font-size: 0.9rem;
    padding: 0.4rem 0.8rem;
    border-radius: 12px;
    font-weight: 500;
  }

  @media (max-width: 768px) {
    .games-container {
      padding: 2rem 1rem;
      gap: 2rem;
    }

    .game-title {
      font-size: 1.5rem;
    }

    .tag {
      font-size: 0.75rem;
      padding: 0.3rem 0.6rem;
    }
  }
</style>

<div class="games-container">

  <div class="game-entry" data-fade>
    <div class="game-title">Terminus</div>
    <a href="{{ '/games/terminus/' | relative_url }}">
      <video
        class="game-video lazy-video"
        muted
        loop
        preload="none"
        playsinline
        onmouseenter="this.play()"
        onmouseleave="this.pause()"
        data-src="{{ '/assets/WEB_Terminus_Pres.mp4' | relative_url }}"
      ></video>
    </a>
    <div class="tag-container">
      <div class="tag">C++</div>
      <div class="tag">Unreal 5</div>
      <div class="tag">Perforce</div>
      <div class="tag">3rd Person</div>
      <div class="tag">Survival-Horror</div>
    </div>
  </div>

  <div class="game-entry" data-fade>
    <div class="game-title">The Diig</div>
    <a href="{{ '/games/thediig/' | relative_url }}">
      <video
        class="game-video lazy-video"
        muted
        loop
        preload="none"
        playsinline
        onmouseenter="this.play()"
        onmouseleave="this.pause()"
        data-src="{{ '/assets/WEB_TheDiig_Pres.mp4' | relative_url }}"
      ></video>
    </a>
    <div class="tag-container">
      <div class="tag">Blueprint</div>
      <div class="tag">Unreal 5</div>
      <div class="tag">Git</div>
      <div class="tag">3rd Person</div>
      <div class="tag">Puzzle</div>
    </div>
  </div>

  <div class="game-entry" data-fade>
    <div class="game-title">Squeaky Clean | Global Game Jam 2025</div>
    <a href="{{ '/games/squeaky/' | relative_url }}">
      <video
        class="game-video lazy-video"
        muted
        loop
        preload="none"
        playsinline
        onmouseenter="this.play()"
        onmouseleave="this.pause()"
        data-src="{{ '/assets/WEB_Squeaky_Pres.mp4' | relative_url }}"
      ></video>
    </a>
    <div class="tag-container">
      <div class="tag">Blueprint</div>
      <div class="tag">Unreal 5</div>
      <div class="tag">Git</div>
      <div class="tag">3rd Person</div>
      <div class="tag">Arcade</div>
      <div class="tag">Casual</div>
    </div>
  </div>

  <div class="game-entry" data-fade>
    <div class="game-title">Giggle Heist | Global Game Jam 2024</div>
    <a href="{{ '/games/giggle/' | relative_url }}">
      <video
        class="game-video lazy-video"
        muted
        loop
        preload="none"
        playsinline
        onmouseenter="this.play()"
        onmouseleave="this.pause()"
        data-src="{{ '/assets/WEB_Giggle_Pres.mp4' | relative_url }}"
      ></video>
    </a>
    <div class="tag-container">
      <div class="tag">Blueprint</div>
      <div class="tag">Unreal 5</div>
      <div class="tag">Git</div>
      <div class="tag">Top View</div>
      <div class="tag">Co-op</div>
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

  // Lazy-load videos with IntersectionObserver
  const lazyVideos = document.querySelectorAll('.lazy-video');
  const videoObserver = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const video = entry.target;
        const src = video.dataset.src;
        if (src) {
          video.src = src;
          video.load();
          video.dataset.src = "";
        }
        videoObserver.unobserve(video);
      }
    });
  }, {
    threshold: 0.25
  });

  lazyVideos.forEach(video => {
    videoObserver.observe(video);
  });
</script>
