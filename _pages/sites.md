---
permalink: /sites/
layout: null
---

<html lang="en">
  <head>
  <title>My Sites · Michael Liu</title>
  <meta content="text/html; charset=utf-8" http-equiv="Content-Type">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Crimson+Pro:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">

  <style>
      :root {
        --black: #000000;
        --text: #000000;
        --bg: #ffffff;
        --border: #dddddd;
      }

      body {
        margin: 0;
        background: var(--bg);
        color: var(--text);
        font-family: 'Times New Roman', Times, serif;
      }

      .container {
        max-width: 750px;
        margin: 0 auto;
        padding: 48px 16px 56px;
      }

      .back-link {
        display: inline-flex;
        align-items: center;
        gap: 6px;
        font-size: 14px;
        color: var(--black);
        text-decoration: none;
      }

      .back-link:hover {
        text-decoration: underline;
      }

      .page-title {
        font-family: 'Crimson Pro', Georgia, serif;
        font-size: 1.8rem;
        font-weight: 700;
        margin: 24px 0 8px;
      }

      .page-intro {
        margin: 0 0 28px;
        line-height: 1.5;
      }

      .site-list {
        display: grid;
        gap: 16px;
      }

      .site-card {
        display: block;
        padding: 20px 22px;
        border: 1px solid var(--border);
        border-radius: 10px;
        color: var(--text);
        text-decoration: none;
        transition: border-color 0.2s ease, transform 0.2s ease;
      }

      .site-card:hover {
        border-color: var(--black);
        transform: translateY(-2px);
      }

      .site-name {
        font-family: 'Crimson Pro', Georgia, serif;
        font-size: 1.25rem;
        font-weight: 600;
        display: flex;
        justify-content: space-between;
        align-items: baseline;
        gap: 12px;
      }

      .site-arrow {
        font-family: 'Times New Roman', Times, serif;
        font-size: 1rem;
        flex-shrink: 0;
      }

      .site-desc {
        margin: 6px 0 8px;
        font-size: 0.95rem;
        line-height: 1.5;
      }

      .site-url {
        font-size: 13px;
        overflow-wrap: anywhere;
      }
  </style>
  </head>

<body>
<main class="container">

  <a href="/" class="back-link">&larr; Back to Home</a>

  <h1 class="page-title">My Sites</h1>
  <p class="page-intro">Other sites I build and maintain.</p>

  <div class="site-list">
    <a href="https://bv003.github.io/EEP596/" class="site-card">
      <div class="site-name">Deep Learning <span class="site-arrow">&rarr;</span></div>
      <p class="site-desc">Course notes on deep learning: lectures and labs on regression, neural networks, CNNs, and generative models.</p>
      <span class="site-url">bv003.github.io/EEP596</span>
    </a>

    <a href="https://bv003.github.io/tech-stack-atlas/" class="site-card">
      <div class="site-name">Tech Stack Atlas <span class="site-arrow">&rarr;</span></div>
      <p class="site-desc">Layered technology stacks across four areas: inference, training, search &amp; recommendation, and AI agents.</p>
      <span class="site-url">bv003.github.io/tech-stack-atlas</span>
    </a>

    <a href="https://bv003.github.io/New-Technologies/" class="site-card">
      <div class="site-name">New Technologies <span class="site-arrow">&rarr;</span></div>
      <p class="site-desc">A timeline of notable new AI technologies, from ChatGPT onward.</p>
      <span class="site-url">bv003.github.io/New-Technologies</span>
    </a>
  </div>

</main>
</body>
</html>
