---
layout: default
title: Home
permalink: /
---

<!--
  Full-page video background hero.
  Make sure you have placed your video at assets/background.mp4
-->

<style>
  /* Ensure page fills the viewport and hides scrollbars */
  html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    overflow: hidden;
  }

  /* Video covers entire viewport, sits behind content */
  .video-bg {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: -1;
  }

  /* Hero container centers its content */
  .hero {
    position: relative;
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  /* Title styling */
  .hero h1 {
    color: #ffffff;
    font-size: 4vw;
    max-font-size: 48px;
    letter-spacing: 4px;
    text-shadow: 0 0 10px rgba(0, 0, 0, 0.7);
    margin: 0;
  }
  
  /* On very small screens, bump up font-size */
  @media (max-width: 480px) {
    .hero h1 {
      font-size: 8vw;
    }
  }
</style>

<div class="hero">
  <video class="video-bg" autoplay muted loop>
    <source src="{{ '/assets/WEB_Homepage_Video.mp4' | relative_url }}" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <h1>Benoit BARRAU | Gameplay Programmer</h1>
</div>
