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
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">

  <style>
      :root {
        --bg: #0d1014;
        --panel: #12161b;
        --text: #d6dde4;
        --muted: #7a8591;
        --accent: #5fd4c9;
        --line: #232a32;
      }

      * { box-sizing: border-box; }

      body {
        margin: 0;
        min-height: 100vh;
        background: var(--bg);
        color: var(--text);
        font-family: 'JetBrains Mono', ui-monospace, SFMono-Regular, Menlo, monospace;
        -webkit-font-smoothing: antialiased;
      }

      ::selection { background: var(--accent); color: var(--bg); }

      .container {
        max-width: 780px;
        margin: 0 auto;
        padding: 56px 24px 80px;
      }

      .back-link {
        display: inline-flex;
        align-items: center;
        gap: 6px;
        font-size: 13px;
        color: var(--muted);
        text-decoration: none;
        transition: color 0.2s ease;
      }

      .back-link::before { content: "["; }
      .back-link::after { content: "]"; }

      .back-link:hover {
        color: var(--accent);
      }

      .page-title {
        font-size: clamp(2rem, 6vw, 2.75rem);
        font-weight: 700;
        line-height: 1.1;
        letter-spacing: -0.01em;
        margin: 56px 0 14px;
      }

      .page-title::before {
        content: "~/ ";
        color: var(--muted);
        font-weight: 400;
      }

      .page-intro {
        margin: 0 0 44px;
        font-size: 0.95rem;
        line-height: 1.6;
        color: var(--muted);
      }

      .page-intro::before { content: "> "; color: var(--accent); }

      .page-intro::after {
        content: "_";
        margin-left: 2px;
        color: var(--accent);
        animation: blink 1.1s steps(1) infinite;
      }

      @keyframes blink { 50% { opacity: 0; } }

      .site-list {
        counter-reset: site;
        display: grid;
        gap: 12px;
      }

      .site-card {
        counter-increment: site;
        display: grid;
        grid-template-columns: 48px 1fr;
        column-gap: 8px;
        padding: 20px 22px 20px 18px;
        background: var(--panel);
        border: 1px solid var(--line);
        border-radius: 6px;
        color: var(--text);
        text-decoration: none;
        transition: border-color 0.2s ease;
      }

      .site-card::before {
        content: counter(site, decimal-leading-zero);
        grid-row: 1 / span 2;
        padding-top: 3px;
        font-size: 12px;
        color: var(--muted);
        transition: color 0.2s ease;
      }

      .site-card > * {
        grid-column: 2;
      }

      .site-card:hover,
      .site-card:focus-visible {
        outline: none;
        border-color: var(--accent);
      }

      .site-card:hover::before,
      .site-card:focus-visible::before {
        color: var(--accent);
      }

      .site-name {
        font-size: 1.05rem;
        font-weight: 700;
        line-height: 1.35;
        display: flex;
        justify-content: space-between;
        align-items: baseline;
        gap: 16px;
        transition: color 0.2s ease;
      }

      .site-card:hover .site-name,
      .site-card:focus-visible .site-name {
        color: var(--accent);
      }

      .site-arrow {
        font-size: 1rem;
        color: var(--muted);
        flex-shrink: 0;
        transition: transform 0.2s ease, color 0.2s ease;
      }

      .site-card:hover .site-arrow,
      .site-card:focus-visible .site-arrow {
        color: var(--accent);
        transform: translateX(4px);
      }

      .site-desc {
        margin: 8px 0 0;
        max-width: 64ch;
        font-size: 0.85rem;
        line-height: 1.65;
        color: var(--muted);
      }

      @media (prefers-reduced-motion: reduce) {
        .page-intro::after { animation: none; }
        .site-arrow { transition: none; }
      }

      @media (max-width: 560px) {
        .container { padding: 40px 16px 64px; }
        .page-title { margin-top: 44px; }
        .page-intro { margin-bottom: 36px; }
        .site-card { grid-template-columns: 34px 1fr; padding: 18px 16px 18px 14px; }
      }
  </style>
  </head>

<body>
<main class="container">

  <a href="/" class="back-link">Michael Liu&rsquo;s Homepage &rarr;</a>

  <h1 class="page-title">My Sites</h1>
  <p class="page-intro">Sites I build and maintain.</p>

  <div class="site-list">
    <a href="https://bv003.github.io/EEP596/" class="site-card">
      <div class="site-name">Deep Learning <span class="site-arrow">&rarr;</span></div>
      <p class="site-desc">Course notes on deep learning: lectures and labs on regression, neural networks, CNNs, and generative models.</p>
    </a>

    <a href="https://bv003.github.io/tech-stack-atlas/" class="site-card">
      <div class="site-name">Tech Stack Atlas <span class="site-arrow">&rarr;</span></div>
      <p class="site-desc">Layered technology stacks across four areas: inference, training, search &amp; recommendation, and AI agents.</p>
    </a>

    <a href="https://bv003.github.io/New-Technologies/" class="site-card">
      <div class="site-name">New Technologies <span class="site-arrow">&rarr;</span></div>
      <p class="site-desc">A timeline of notable new AI technologies, from ChatGPT onward.</p>
    </a>
  </div>

</main>
</body>
</html>
