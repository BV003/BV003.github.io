---
permalink: /
layout: null
---

<html lang="en">
  <head>
  <title>Michael Liu</title>
  <meta content="text/html; charset=utf-8" http-equiv="Content-Type">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <script defer src="https://bv003-stats.vercel.app/script.js" data-website-id="cdbe9aa5-de02-4e77-9922-1cb98377b93e"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Crimson+Pro:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

  <style>
      :root {
        /* Palette: Tufte cream paper, near-black ink, one gray */
        --black: #111111;
        --primary: var(--black);
        --accent: var(--black);
        --accent-bright: var(--black);
        --secondary: var(--black);
        --text: #111111;
        --text-light: #6b6b6b;
        --bg: #fffff8;
        --bg-card: #fffff8;
        --border: #e8e8dc;
        /* Type scale: three sizes, nothing else */
        --fs-lg: 1.333rem;   /* name, section titles  (24px) */
        --fs-base: 1rem;     /* body, item titles     (18px) */
        --fs-sm: 0.833rem;   /* dates, meta, details  (15px) */
      }

      html {
        font-size: 18px;
      }

      body {
        margin: 0;
        background: var(--bg);
        color: var(--text);
        font-family: 'Crimson Pro', Georgia, serif;
        font-size: var(--fs-base);
        line-height: 1.55;
        -webkit-font-smoothing: antialiased;
      }

      /* One centered column at every width: header on top, content below */
      .page-shell {
        box-sizing: border-box;
        max-width: calc(35rem + 56px);
        margin: 0 auto;
        padding: 56px 28px 56px;
      }

      @media (max-width: 600px) {
        .page-shell {
          padding: 36px 16px 48px;
        }
      }

      .container {
        max-width: 35rem;   /* ~75 characters per line */
        margin: 0;
      }

      /* Section Styling */
      .section {
        padding: 0px 0;
        margin-bottom: 52px;
      }

      .section h2 {
        margin-top: 0 !important;
        margin-bottom: 8px !important;
      }

      .section-title {
        font-family: 'Crimson Pro', Georgia, serif;
        font-size: var(--fs-lg);
        font-weight: 600;
        color: var(--primary);
        display: flex;
        align-items: center;
      }

      .section-title a {
        font-size: var(--fs-sm);
        font-family: 'Crimson Pro', Georgia, serif;
        font-weight: 500;
        color: var(--black);
        text-decoration: none;
        margin-left: auto;
      }

      .section-title a:hover {
        text-decoration: underline;
      }

      /* News Section */
      /* Bottom fade on content; second mask layer keeps the right-side scrollbar strip fully visible */
      .news-container {
        max-height: 175px;  /* shows ~3.5 entries so the faded one hints at scrolling */
        overflow-y: auto;
        scrollbar-width: thin;
        -webkit-mask-image: linear-gradient(to bottom, #000 calc(100% - 28px), transparent), linear-gradient(#000, #000);
        mask-image: linear-gradient(to bottom, #000 calc(100% - 28px), transparent), linear-gradient(#000, #000);
        -webkit-mask-size: 100% 100%, 16px 100%;
        mask-size: 100% 100%, 16px 100%;
        -webkit-mask-position: 0 0, 100% 0;
        mask-position: 0 0, 100% 0;
        -webkit-mask-repeat: no-repeat;
        mask-repeat: no-repeat;
      }

      /* Drop the bottom fade once scrolled to the end (toggled by script) */
      .news-container.at-end {
        -webkit-mask-image: none;
        mask-image: none;
      }

      .news-item {
        padding: 8px 12px 8px 0;
        display: grid;
        grid-template-columns: 72px 1fr;
        gap: 14px;
        align-items: baseline;  /* date sits on the entry's first line */
      }

      /* Dates use [YYYY.MM]; tabular digits keep the column aligned */
      .news-date {
        font-size: var(--fs-sm);
        font-weight: 400;
        color: var(--text-light);
        font-family: 'Crimson Pro', Georgia, serif;
        white-space: nowrap;
        font-variant-numeric: tabular-nums;
      }

      .news-content {
        font-size: var(--fs-sm);
        color: var(--text);
        line-height: 1.5;
      }

      .news-content a {
        color: var(--black);
        text-decoration: none;
        font-weight: 500;
      }

      .news-content a:hover {
        color: var(--black);
        text-decoration: underline;
      }

      .news-highlight {
        color: var(--black);
        font-weight: 600;
      }

      /* Same look as the sidebar links: plain text, underline on hover */
      .inline-link {
        color: inherit;
        text-decoration: none;
      }

      .inline-link:hover {
        text-decoration: underline;
        text-underline-offset: 3px;
        text-decoration-thickness: 1px;
      }

      .about-text {
        text-align: left;
        margin-bottom: 12px;
        line-height: 1.5;
      }
  </style>
  </head>

<body>
<div class="page-shell">

<header class="site-header">
  <div class="site-title">
    <h1 class="header-name">Michael Liu</h1>
    <img src="/images/signature.png" alt="刘玮祺" class="header-signature-img">
  </div>
  <nav class="site-links" aria-label="Links">
        <a href="https://bv003me.vercel.app/" target="_blank" rel="noopener">Writing</a>
        <a href="/sites/">Websites</a>
        <a href="mailto:michaelliuwq003@gmail.com">Email</a>
        <a href="https://x.com/bbz377889285007" target="_blank" rel="noopener">X</a>
        <a href="https://michaelliu899840.substack.com/" target="_blank" rel="noopener">Substack</a>
        <a href="https://github.com/BV003" target="_blank" rel="noopener">GitHub</a>
        <a href="https://www.linkedin.com/in/michael-liu-0673452b1/" target="_blank" rel="noopener">LinkedIn</a>
        <a href="https://scholar.google.com/citations?user=SYCjc44AAAAJ&hl=en&oi=sra" target="_blank" rel="noopener">Scholar</a>
        <a href="/files/cv.pdf" target="_blank" rel="noopener">CV</a>
  </nav>

  <style>
    /* Header: name + signature, then every link in one format; all left-aligned with the text */
    .site-header {
      margin-bottom: 48px;
    }

    .site-title {
      display: flex;
      align-items: center;
      gap: 18px;
    }

    .header-name {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: var(--fs-lg);
      font-weight: 700;
      color: var(--black);
      margin: 0;
      line-height: 1.15;
    }

    /* The ink fills only the middle third of signature.png; negative margins
       trim the empty paper so the brushwork can sit at the name's scale */
    .header-signature-img {
      display: block;
      height: 100px;
      width: auto;
      margin: -34px 0 -30px -20px;
      /* The PNG has a white ground; multiply lets the ink sit on the paper tone */
      mix-blend-mode: multiply;
    }

    .site-links {
      display: flex;
      flex-wrap: wrap;
      gap: 4px 18px;
      margin-top: 22px;
    }

    .site-links a {
      color: var(--text);
      text-decoration: none;
    }

    .site-links a:hover {
      text-decoration: underline;
      text-underline-offset: 3px;
      text-decoration-thickness: 1px;
    }

    @media (max-width: 600px) {
      .site-header {
        margin-bottom: 32px;
      }

      .site-title {
        gap: 12px;
      }

      .header-signature-img {
        height: 84px;
        margin: -29px 0 -25px -18px;
      }
    }
  </style>
</header>

<main>
<div class="container">

<section class="section">
  <h2 class="section-title">
    About Me
  </h2>
<p class="about-text">
Hi.
<br>
I'm Weiqi Liu, and you can call me Michael.
<br>
I'm an engineer who builds software and AI systems. I'm also interested in investing, cryptocurrency, literary writing, and aesthetics.
</p>
<p class="about-text">
If you'd like to talk, whether it's about something fun, something technical, or something about money, please drop me an <a href="mailto:michaelliuwq003@gmail.com" class="inline-link">e-mail</a>. I'd be glad to hear from you.
</p>
</section>


<section class="section">
  <h2 class="section-title">
    News
  </h2>
<div class="news-container">

  <div class="news-item">
    <span class="news-date">[2026.08]</span>
    <div class="news-content">
      I will begin my M.S. in Electrical and Computer Engineering at University of Washington, Seattle this fall.
    </div>
  </div>

  <div class="news-item">
    <span class="news-date">[2026.06]</span>
    <div class="news-content">
      Graduated from Wuhan University.
    </div>
  </div>

  <div class="news-item">
    <span class="news-date">[2026.01]</span>
    <div class="news-content">
      I am excited to begin my role as an AI Software Engineer Intern at Apple.
    </div>
  </div>

  <div class="news-item">
    <span class="news-date">[2026.01]</span>
    <div class="news-content">
      One paper related to AI interpretability is now available on arXiv. Feel free to check it out.
    </div>
  </div>

  <div class="news-item">
    <span class="news-date">[2025.09]</span>
    <div class="news-content">
      One paper is accepted to NeurIPS 2025(Spotlight). Thanks to all my collaborators.
    </div>
  </div>
  
</div>
</section>


<section class="section">
  <h2 class="section-title">
    Work Experience
  </h2>

  <div class="exp-list">
    <div class="exp-item">
      <div class="exp-main">
        <span class="exp-company">Apple</span>
        <span class="exp-date">Jan 2026 – Jul 2026</span>
      </div>
      <div class="exp-role">AI Software Engineer Intern</div>
    </div>
  </div>

  <style>
    .exp-list {
      margin-top: 8px;
    }

    .exp-item {
      padding: 16px 0;
    }

    .exp-item:first-child {
      padding-top: 8px;
    }


    .exp-item:last-child {

      padding-bottom: 0;

    }

    .exp-main {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      gap: 12px;
      margin-bottom: 4px;
    }

    .exp-company {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: var(--fs-base);
      font-weight: 400;
      color: var(--primary);
    }

    .exp-date {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: var(--fs-sm);
      font-weight: 500;
      color: var(--text-light);
      flex-shrink: 0;
    }

    .exp-role {
      font-size: var(--fs-sm);
      color: var(--text);
      line-height: 1.4;
    }

    @media (max-width: 600px) {
      .exp-main {
        flex-direction: column;
        gap: 4px;
      }
    }
  </style>

</section>

<section class="section">
  <h2 class="section-title">
    Projects
  </h2>

  <div class="project-list">
    <div class="project-item">
      <div class="project-name">
        MemServe
        <a href="https://github.com/PhysFlow/ServerlessLLMonSuperchips" class="pub-link project-link" target="_blank">
          Code
        </a>
      </div>
      <div class="project-desc">Serving models larger than MIG memory on NVIDIA MIG instances with SGLang.</div>
      <ul class="project-points">
        <li>HybridGEMM kernel that computes on weights kept in CPU memory.</li>
        <li>Runtime that tunes the split ratio alpha online from HBM and host-link load.</li>
        <li>Serverless control plane that places models on SGLang workers on demand.</li>
      </ul>
    </div>
  </div>

  <style>
    .project-list {
      margin-top: 8px;
    }

    .project-item {
      padding: 16px 0;
    }

    .project-item:first-child {
      padding-top: 8px;
    }

    .project-item:last-child {
      padding-bottom: 0;
    }

    .project-name {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: var(--fs-base);
      font-weight: 400;
      color: var(--primary);
      margin-bottom: 4px;
    }

    .pub-link.project-link {
      margin-left: 8px;
      align-items: baseline;
    }


    .project-desc {
      font-size: var(--fs-sm);
      color: var(--text);
      line-height: 1.5;
    }

    .project-points {
      margin: 6px 0 0;
      padding: 0;
      list-style: none;
      font-size: var(--fs-sm);
      color: var(--text);
      line-height: 1.6;
    }

    .project-points li {
      position: relative;
      padding-left: 16px;
    }

    .project-points li::before {
      content: "–";
      position: absolute;
      left: 0;
    }
  </style>

</section>

<section class="section">
  <h2 class="section-title">
    Academic Publications
  </h2>

  <style>
    .pub-list {
      margin-top: 8px;
    }

    /* Text-only layout; to bring figures back, set columns to "120px 1fr" and uncomment the pub-image blocks below */
    .pub-item {
      display: grid;
      grid-template-columns: 1fr;
      gap: 20px;
      padding: 16px 0;
      align-items: start;
    }

    .pub-item:first-child {
      padding-top: 8px;
    }


    .pub-item:last-child {

      padding-bottom: 0;

    }

    .pub-image {
      border-radius: 6px;
      overflow: hidden;
      background: var(--bg);
      height: 75px;
    }

    .pub-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .pub-content {
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .pub-title {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: var(--fs-base);
      font-weight: 400;
      color: var(--black);
      line-height: 1.4;
      margin-bottom: 6px;
    }

    .pub-authors {
      font-size: var(--fs-sm);
      color: var(--text);
      margin-bottom: 4px;
      line-height: 1.4;
    }

    /* Venue and Paper/Code buttons share one line; wraps on narrow screens */
    .pub-meta {
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      gap: 6px 14px;
    }

    .pub-venue {
      font-size: var(--fs-sm);
      color: var(--text-light);
      font-weight: 500;
    }

    .pub-links {
      display: flex;
      gap: 10px;
    }

    .pub-link {
      display: inline-flex;
      align-items: center;
      gap: 4px;
      text-decoration: none;
      color: var(--text-light);
      font-size: var(--fs-sm);
      font-weight: 500;
      transition: color 0.2s ease;
    }

    .pub-link:hover {
      color: var(--black);
    }

    @media (max-width: 600px) {
      .pub-item {
        grid-template-columns: 1fr;
        gap: 12px;
      }

      .pub-image {
        height: 140px;
      }
    }

  </style>

  <div class="pub-list">
    <!-- Publication 1 -->
    <div class="pub-item">
      <!--
      <div class="pub-image">
        <img src="/images/Neuron.png" alt="NeuronScope paper figure">
      </div>
      -->
      <div class="pub-content">
        <div class="pub-title">NeuronScope: A Multi-Agent Framework for Explaining Polysemantic Neurons in Language Models</div>
        <div class="pub-authors">Weiqi Liu, Yongliang Miao, Haiyan Zhao, Yanguang Liu, Mengnan Du</div>
        <div class="pub-meta">
          <div class="pub-venue">arXiv, 2026</div>
          <div class="pub-links">
            <a href="https://arxiv.org/pdf/2601.03671" class="pub-link" target="_blank">
              Paper
            </a>
          </div>
        </div>
      </div>
    </div>

    <!-- Publication 2 -->
    <div class="pub-item">
      <!--
      <div class="pub-image">
        <img src="/images/Mars.png" alt="MARS-VFL paper figure">
      </div>
      -->
      <div class="pub-content">
        <div class="pub-title">MARS-VFL: A Unified Benchmark for Vertical Federated Learning with Realistic Evaluation</div>
        <div class="pub-authors">Wei Shen, Weiqi Liu, Mingde Chen, Wenke Huang, Mang Ye</div>
        <div class="pub-meta">
          <div class="pub-venue">NeurIPS, 2025 (Spotlight)</div>
          <div class="pub-links">
            <a href="https://neurips.cc/virtual/2025/poster/121843" class="pub-link" target="_blank">
              Paper
            </a>
            <a href="https://github.com/shentt67/MARS-VFL" class="pub-link" target="_blank">
              Code
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ## Popular Publications -->



<section class="section">

<h2 class="section-title">
  Education
</h2>

<div class="edu-list">
  <div class="edu-item">
    <div class="edu-info">
      <div class="edu-main">
        <span class="edu-school">University of Washington, Seattle</span>
        <span class="edu-date">2026 – Present</span>
      </div>
      <div class="edu-degree">M.S. in Electrical and Computer Engineering</div>
    </div>
  </div>

  <div class="edu-item">
    <div class="edu-info">
      <div class="edu-main">
        <span class="edu-school">Wuhan University</span>
        <span class="edu-date">2022 – 2026</span>
      </div>
      <div class="edu-degree">B.S. in Software Engineering</div>
    </div>
  </div>
</div>

<style>
  .edu-list {
    margin-top: 8px;
  }

  .edu-item {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 16px 0;
  }

  .edu-item:first-child {
    padding-top: 8px;
  }


  .edu-item:last-child {

    padding-bottom: 0;

  }


  .edu-info {
    flex: 1;
  }
  
  .edu-main {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 12px;
    margin-bottom: 4px;
  }

  .edu-school {
    font-family: 'Crimson Pro', Georgia, serif;
    font-size: var(--fs-base);
    font-weight: 400;
    color: var(--primary);
  }

  .edu-date {
    font-family: 'Crimson Pro', Georgia, serif;
    font-size: var(--fs-sm);
    font-weight: 500;
    color: var(--text-light);
    flex-shrink: 0;
  }

  .edu-degree {
    font-size: var(--fs-sm);
    color: var(--text);
  }
  
  @media (max-width: 600px) {

    .edu-main {
      flex-direction: column;
      gap: 4px;
    }
  }
</style>
</section>


<section class="section">
  <h2 class="section-title">
    Service
  </h2>

  <div class="service-list">
    <div class="service-item">
      <div class="service-main">
        <span class="service-role">Reviewer</span>
        <span class="service-date">2025</span>
      </div>
      <div class="service-venue">Applied AI Letters</div>
    </div>
    <div class="service-item">
      <div class="service-main">
        <span class="service-role">Teaching Assistant</span>
        <span class="service-date">Fall 2023</span>
      </div>
      <div class="service-venue">Advanced Programming, Wuhan University</div>
    </div>
  </div>

  <style>
    .service-list {
      margin-top: 8px;
    }

    .service-item {
      padding: 16px 0;
    }

    .service-item:first-child {
      padding-top: 8px;
    }


    .service-item:last-child {

      padding-bottom: 0;

    }

    .service-main {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      gap: 12px;
      margin-bottom: 4px;
    }

    .service-role {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: var(--fs-base);
      font-weight: 400;
      color: var(--primary);
    }

    .service-date {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: var(--fs-sm);
      font-weight: 500;
      color: var(--text-light);
      flex-shrink: 0;
    }

    .service-venue {
      font-size: var(--fs-sm);
      color: var(--text);
    }

    @media (max-width: 600px) {
      .service-main {
        flex-direction: column;
        gap: 4px;
      }
    }
  </style>

</section>

</div>
</main>

</div>

<script>
  document.querySelectorAll('.news-container').forEach(function (el) {
    function update() {
      el.classList.toggle('at-end', el.scrollTop + el.clientHeight >= el.scrollHeight - 1);
    }
    el.addEventListener('scroll', update, { passive: true });
    window.addEventListener('resize', update);
    update();
  });
</script>

</body>
</html>
