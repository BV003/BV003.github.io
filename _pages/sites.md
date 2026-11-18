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
        --bg: #07090b;
        --term: #0c1013;
        --bar: #141a1f;
        --text: #c9d4dc;
        --muted: #5d6b77;
        --green: #7ee787;
        --cyan: #56d4dd;
        --yellow: #e3b341;
        --line: #1d252c;
      }

      * { box-sizing: border-box; }

      body {
        margin: 0;
        min-height: 100vh;
        background:
          radial-gradient(circle at 50% 0%, rgba(86,212,221,0.06), transparent 60%),
          var(--bg);
        color: var(--text);
        font-family: 'JetBrains Mono', ui-monospace, SFMono-Regular, Menlo, monospace;
        font-size: 14px;
        -webkit-font-smoothing: antialiased;
      }

      ::selection { background: var(--green); color: var(--bg); }

      .container {
        max-width: 820px;
        margin: 0 auto;
        padding: 56px 24px 80px;
      }

      .back-link {
        font-size: 12px;
        color: var(--muted);
        text-decoration: none;
      }
      .back-link::before { content: "cd "; color: var(--green); }
      .back-link:hover { color: var(--cyan); }

      .terminal {
        margin-top: 28px;
        background: var(--term);
        border: 1px solid var(--line);
        border-radius: 10px;
        overflow: hidden;
        box-shadow: 0 20px 60px rgba(0,0,0,0.5);
      }

      .term-bar {
        display: flex;
        align-items: center;
        gap: 8px;
        padding: 11px 14px;
        background: var(--bar);
        border-bottom: 1px solid var(--line);
      }
      .dot { width: 11px; height: 11px; border-radius: 50%; }
      .dot.r { background: #ff5f57; }
      .dot.y { background: #febc2e; }
      .dot.g { background: #28c840; }
      .term-title {
        flex: 1;
        text-align: center;
        margin-right: 49px;
        font-size: 12px;
        color: var(--muted);
      }

      .term-body { padding: 22px 22px 26px; }

      .prompt { color: var(--muted); margin: 0; line-height: 1.7; }
      .prompt .user { color: var(--green); }
      .prompt .path { color: var(--cyan); }
      .prompt .cmd { color: var(--text); }

      .page-title {
        margin: 18px 0 4px;
        font-size: clamp(1.6rem, 5vw, 2.2rem);
        font-weight: 700;
        color: var(--green);
        letter-spacing: -0.01em;
      }
      .page-title::before { content: "# "; color: var(--muted); font-weight: 400; }

      .page-intro {
        margin: 0 0 22px;
        color: var(--muted);
        line-height: 1.6;
      }
      .page-intro::before { content: "// "; }

      .site-list {
        counter-reset: site;
        border-top: 1px dashed var(--line);
      }

      .site-card {
        counter-increment: site;
        display: grid;
        grid-template-columns: 34px 1fr;
        column-gap: 10px;
        padding: 16px 10px;
        border-bottom: 1px dashed var(--line);
        color: var(--text);
        text-decoration: none;
        transition: background 0.15s ease;
      }
      .site-card::before {
        content: "[" counter(site) "]";
        grid-row: 1 / span 2;
        color: var(--yellow);
      }
      .site-card > * { grid-column: 2; }

      .site-card:hover,
      .site-card:focus-visible {
        outline: none;
        background: rgba(126,231,135,0.05);
      }

      .site-name {
        display: flex;
        justify-content: space-between;
        align-items: baseline;
        gap: 16px;
        font-weight: 700;
        color: var(--cyan);
      }
      .site-card:hover .site-name { color: var(--green); }

      .site-arrow { color: var(--muted); flex-shrink: 0; transition: transform 0.15s ease, color 0.15s ease; }
      .site-card:hover .site-arrow { color: var(--green); transform: translateX(4px); }

      .site-desc {
        margin: 6px 0 0;
        max-width: 66ch;
        font-size: 13px;
        line-height: 1.65;
        color: var(--muted);
      }

      .cursor {
        display: inline-block;
        width: 8px;
        height: 1.1em;
        vertical-align: text-bottom;
        background: var(--green);
        animation: blink 1.1s steps(1) infinite;
      }
      @keyframes blink { 50% { opacity: 0; } }

      .prompt.end { margin-top: 18px; }

      @media (prefers-reduced-motion: reduce) {
        .cursor { animation: none; }
        .site-arrow { transition: none; }
      }

      @media (max-width: 560px) {
        .container { padding: 36px 16px 56px; }
        .term-body { padding: 18px 14px 22px; }
        .site-card { grid-template-columns: 28px 1fr; padding: 14px 4px; }
      }
  </style>
  </head>

<body>
<main class="container">

  <a href="/" class="back-link">Michael Liu&rsquo;s Homepage &rarr;</a>

  <div class="terminal">
    <div class="term-bar">
      <span class="dot r"></span><span class="dot y"></span><span class="dot g"></span>
      <span class="term-title">michael@liu: ~/sites</span>
    </div>

    <div class="term-body">
      <p class="prompt"><span class="user">michael@liu</span>:<span class="path">~</span>$ <span class="cmd">ls ~/sites</span></p>

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

      <p class="prompt end"><span class="user">michael@liu</span>:<span class="path">~</span>$ <span class="cursor"></span></p>
    </div>
  </div>

</main>
</body>
</html>
