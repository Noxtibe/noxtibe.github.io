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
    gap: 3rem;
    padding: 2rem 1rem;
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
    aspect-ratio: 16 / 9;
    object-fit: cover;
    border-radius: 16px;
    background-color: #000;
    transition: transform 0.3s;
    cursor: pointer;
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
      gap: 2rem;
      padding: 1rem 0.5rem;
    }

    .game-title {
      font-size: 1.4rem;
    }

    .game-video {
      border-radius: 10px;
    }

    .tag {
      font-size: 0.75rem;
      padding: 0.3rem 0.6rem;
    }
  }
</style>

<div class="games-container">

  {% assign games = 
    site.data.games | default: 
    [
      {
        "title": "Terminus",
        "url": "/games/terminus/",
        "src": "/assets/WEB_Terminus_Pres.mp4",
        "tags": "C++,Unreal 5,Perforce,3rd Person,Survival-Horror"
      },
      {
        "title": "The Diig",
        "url": "/games/thediig/",
        "src": "/assets/WEB_TheDiig_Pres.mp4",
        "tags": "Blueprint,Unreal 5,Git,3rd Person,Puzzle"
      },
      {
        "title": "Squeaky Clean | Global Game Jam 2025",
        "url": "/games/squeaky/",
        "src": "/assets/WEB_Squeaky_Pres.mp4",
        "tags": "Blueprint,Unreal 5,Git,3rd Person,Arcade,Casual"
      },
      {
        "title": "Giggle Heist | Global Game Jam 2024",
        "url": "/games/giggle/",
        "src": "/assets/WEB_Giggle_Pres.mp4",
        "tags": "Blueprint,Unreal 5,Git,Top View,Co-op"
      }
    ]
  %}

  {% for game in games %}
    <div class="game-entry" data-fade>
      <div class="game-title">{{ game.title }}</div>
      <a href="{{ game.url | relative_url }}">
        <video
          class="game-video lazy-video"
          data-src="{{ game.src | relative_url }}"
          muted
          loop
          playsinline
          preload="none"
        ></video>
      </a>
      <div class="tag-container">
        {% assign tags = game.tags | split: "," %}
        {% for tag in tags %}
          <div class="tag">{{ tag }}</div>
        {% endfor %}
      </div>
    </div>
  {% endfor %}

</div>

<script>
  // Fade-in on scroll
  const fadeElements = document.querySelectorAll('[data-fade]');
  function handleFadeIn() {
    fadeElements.forEach(el => {
      const rect = el.getBoundingClientRect();
      if (rect.top < window.innerHeight - 100) {
        el.classList.add('visible');
      }
    });
  }

  window.addEventListener('scroll', handleFadeIn);
  window.addEventListener('load', handleFadeIn);

  // Lazy loading with autoplay on mobile
  const lazyVideos = document.querySelectorAll('video.lazy-video');
  const isMobile = /iPhone|iPad|Android/i.test(navigator.userAgent);

  const observer = new IntersectionObserver((entries, obs) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const video = entry.target;
        const src = video.getAttribute('data-src');
        if (src && !video.src) {
          video.src = src;
          video.load();
        }
        if (isMobile) {
          video.play().catch(() => {});
        }

        // Only once
        obs.unobserve(video);
      }
    });
  }, {
    rootMargin: "200px 0px"
  });

  lazyVideos.forEach(video => {
    observer.observe(video);

    // Desktop hover playback
    if (!isMobile) {
      video.addEventListener('mouseenter', () => video.play());
      video.addEventListener('mouseleave', () => video.pause());
    }
  });
</script>
