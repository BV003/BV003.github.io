---
permalink: /
layout: null
---

<html lang="en">
  <head>
  <title>Michael Liu</title>
  <meta content="text/html; charset=utf-8" http-equiv="Content-Type">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Crimson+Pro:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Source+Sans+3:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
      :root {
        --black: #000000;
        --primary: var(--black);
        --accent: var(--black);
        --accent-bright: var(--black);
        --secondary: var(--black);
        --text: #2d3748;
        --text-light: #4a5568;
        --bg: #fafafa;
        --bg-card: #ffffff;
        --border: #e2e8f0;
        --highlight-blue: #e6f3fa;
        --highlight-gold: #fff9e6;
      }

      /* margin: 0 auto; */
      .container {
        max-width: 750px;
        margin: 0 auto;
      }

      /* Section Styling */
      .section {
        padding: 0px 0;
        margin-bottom: 42px;
      }

      .section h2 {
        margin-top: 0 !important;
        margin-bottom: 8px !important;
      }

      .section-title {
        font-family: 'Crimson Pro', Georgia, serif;
        font-size: 1.5rem;
        font-weight: 600;
        color: var(--primary);
        display: flex;
        align-items: center;
        gap: 12px;
      }

      .section-title::before {
        content: '';
        width: 4px;
        height: 24px;
        background: var(--black);
        border-radius: 2px;
      }

      .section-title a {
        font-size: 0.5em;
        font-family: 'Source Sans 3', sans-serif;
        font-weight: 500;
        color: var(--black);
        text-decoration: none;
        margin-left: auto;
      }

      .section-title a:hover {
        text-decoration: underline;
      }

      /* News Section */
      .news-container {
        background: var(--bg-card);
        border-radius: 10px;
        border: 1px solid var(--border);
        max-height: 210px;
        overflow-y: auto;
        scrollbar-width: thin;
        scrollbar-color: var(--border) transparent;
      }

      .news-container::-webkit-scrollbar {
        width: 6px;
      }

      .news-container::-webkit-scrollbar-track {
        background: transparent;
      }

      .news-container::-webkit-scrollbar-thumb {
        background: var(--border);
        border-radius: 3px;
      }

      .news-item {
        padding: 12px 20px;
        border-bottom: 1px solid var(--border);
        display: grid;
        grid-template-columns: 72px 1fr;
        gap: 14px;
        align-items: baseline;
        transition: background 0.2s;
      }

      .news-item:last-child {
        border-bottom: none;
      }

      .news-item:hover {
        background: rgba(0, 98, 155, 0.04);
      }

      .news-date {
        font-size: 13px;
        font-weight: 600;
        color: var(--black);
        font-family: 'Crimson Pro', serif;
      }

      .news-content {
        font-size: 14px;
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
        color: #000000;
        font-weight: 600;
      }

      .research-text {
        text-align: justify;
        text-align-last: left;
        margin-bottom: 12px;
        line-height: 1.5;
      }
  </style>
  </head>

<body>
<div class="container">

<!-- Header Section with Avatar and Links -->
<section class="section" style="margin-bottom: 20px; padding-bottom: 30px; border-bottom: 1px solid var(--border);">
  <div class="header-container">
    <div class="header-left">
      <img src="/images/profile.png" alt="Weiqi Liu" class="header-avatar">
      <div class="header-info">
        <h1 class="header-name">Weiqi Liu</h1>
        <p class="header-subtitle">Michael</p>
      </div>
    </div>
    <div class="header-right">
      <div class="header-links">
        <a href="/files/cv.pdf" class="header-link" target="_blank">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
            <polyline points="14 2 14 8 20 8"></polyline>
          </svg>
          CV
        </a>
        <a href="https://bv003me.vercel.app/" class="header-link" target="_blank">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"></path>
            <path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"></path>
          </svg>
          Blog
        </a>
      </div>
      <div class="header-social">
        <a href="mailto:michaelliuwq003@gmail.com" class="social-icon" title="Email">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <rect x="2" y="4" width="20" height="16" rx="2"/>
            <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/>
          </svg>
        </a>
        <a href="https://github.com/BV003" class="social-icon" target="_blank" title="GitHub">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
          </svg>
        </a>
        <a href="https://scholar.google.com" class="social-icon" target="_blank" title="Google Scholar">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/>
          </svg>
        </a>
      </div>
    </div>
  </div>

  <style>
    .header-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 30px;
    }

    .header-left {
      display: flex;
      align-items: center;
      gap: 20px;
    }

    .header-avatar {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid var(--border);
    }

    .header-name {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: 1.8rem;
      font-weight: 700;
      color: var(--black);
      margin: 0;
    }

    .header-subtitle {
      font-size: 1rem;
      color: var(--text-light);
      margin: 4px 0 0 0;
    }

    .header-right {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      gap: 12px;
    }

    .header-links {
      display: flex;
      gap: 12px;
    }

    .header-link {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 8px 16px;
      background: var(--black);
      color: white;
      text-decoration: none;
      border-radius: 6px;
      font-size: 14px;
      font-weight: 500;
      transition: all 0.2s ease;
    }

    .header-link:hover {
      opacity: 0.8;
      transform: translateY(-1px);
    }

    .header-social {
      display: flex;
      gap: 10px;
    }

    .social-icon {
      width: 36px;
      height: 36px;
      display: flex;
      align-items: center;
      justify-content: center;
      border: 1px solid var(--border);
      border-radius: 50%;
      color: var(--text);
      text-decoration: none;
      transition: all 0.2s ease;
    }

    .social-icon:hover {
      background: var(--black);
      color: white;
      border-color: var(--black);
    }

    @media (max-width: 600px) {
      .header-container {
        flex-direction: column;
        align-items: flex-start;
        gap: 20px;
      }

      .header-right {
        align-items: flex-start;
        width: 100%;
      }

      .header-links {
        width: 100%;
      }

      .header-link {
        flex: 1;
        justify-content: center;
      }
    }
  </style>
</section>

<section class="section">
  <h2 class="section-title">
    About Me
  </h2>
Hi.
<br>
I'm Weiqi Liu, and you can call me Michael.
<br>
I aim to become one of the top engineers in the world.
<br>
For any <strong>suggestions</strong> or <strong>collaborations</strong>, please feel free to drop me an e-mail.
</section>

<section class="section">
  <h2 class="section-title">
    Research
  </h2>

<p class="research-text">
My primary focus is currently on <strong>artificial intelligence</strong> research. The emergence of large language models has greatly accelerated technological innovation and can automate many repetitive cognitive tasks. When these models are integrated with software and hardware, they enable large-scale automation in the real world. I believe that researching how to build more efficient AI models and exploring their practical applications is a highly promising direction.

As for my personal interests, I am also deeply passionate about <strong>investing</strong>, <strong>Web3 technologies</strong>, <strong>literary writing</strong>, and <strong>aesthetics</strong>.
</p> 

</section>


<section class="section">
  <h2 class="section-title">
    News
  </h2>
<div class="news-container">

  <div class="news-item">
    <span class="news-date">Jan 2026</span>
    <div class="news-content">
      <i class="fab fa-apple" aria-hidden="true" style="margin-right: 3.6px;"></i>I am excited to begin my role as an AI Software Engineer Intern at <strong>Apple</strong>.
    </div>
  </div>

  <div class="news-item">
    <span class="news-date">Jan 2026</span>
    <div class="news-content">
      🎉One paper related to AI interpretability is now available on arXiv. Feel free to check it out.
    </div>
  </div>

  <div class="news-item">
    <span class="news-date">Sep 2025</span>
    <div class="news-content">
      🥰One paper is accepted to NeurIPS 2025(Spotlight). Thanks to all my collaborators.
    </div>
  </div>
  
</div>
</section>


<section class="section">
  <h2 class="section-title">
    Work Experience
  </h2>

  <div class="experience-card">
    <div class="experience-header">
      <div class="company-info">
        <div class="company-name-row">
          <span class="company-name">Apple</span>
          <span class="experience-date-inline">2026</span>
        </div>
        <div class="company-role">AI Software Engineer Intern</div>
      </div>
    </div>
  </div>

  <style>
    .experience-card {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 24px;
      margin-top: 8px;
      transition: all 0.3s ease;
    }

    .experience-card:hover {
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
      transform: translateY(-2px);
    }

    .experience-header {
      margin-bottom: 0;
    }

    .company-info {
      display: flex;
      flex-direction: column;
      gap: 4px;
    }

    .company-name-row {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .company-name {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: 1.3rem;
      font-weight: 600;
      color: var(--primary);
    }

    .experience-date-inline {
      font-family: 'Crimson Pro', serif;
      font-size: 0.85rem;
      font-weight: 600;
      color: var(--text-light);
      background: var(--bg);
      padding: 3px 10px;
      border-radius: 20px;
      border: 1px solid var(--border);
    }

    @media (max-width: 600px) {
      .company-name-row {
        flex-wrap: wrap;
      }
    }
  </style>

</section>

<section class="section">
  <h2 class="section-title">
    Academic Publications
  </h2>

  <style>
    .pub-container {
      display: flex;
      flex-direction: column;
      gap: 24px;
    }

    .pub-item {
      display: grid;
      grid-template-columns: 220px 1fr;
      gap: 24px;
      padding: 20px;
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 12px;
      transition: all 0.25s ease;
    }

    .pub-item:hover {
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.06);
    }

    .pub-image {
      position: relative;
      border-radius: 8px;
      overflow: hidden;
      background: var(--bg);
    }

    .pub-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .pub-badge {
      position: absolute;
      top: 10px;
      left: 10px;
      background: var(--black);
      color: white;
      padding: 4px 12px;
      border-radius: 4px;
      font-size: 12px;
      font-weight: 600;
      letter-spacing: 0.3px;
    }

    .pub-badge-spotlight {
      background: #000;
      color: #fff;
    }

    .pub-content {
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .pub-title {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: 1.15rem;
      font-weight: 600;
      color: var(--black);
      line-height: 1.4;
      margin-bottom: 10px;
    }

    .pub-authors {
      font-size: 14px;
      color: var(--text);
      margin-bottom: 6px;
      line-height: 1.5;
    }

    .pub-venue {
      font-size: 13px;
      color: var(--text-light);
      font-weight: 500;
      margin-bottom: 12px;
    }

    .pub-links {
      display: flex;
      gap: 12px;
    }

    .pub-link {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 6px 14px;
      border: 1px solid var(--border);
      border-radius: 6px;
      text-decoration: none;
      color: var(--black);
      font-size: 13px;
      font-weight: 500;
      transition: all 0.2s ease;
    }

    .pub-link:hover {
      background: var(--black);
      color: white;
      border-color: var(--black);
    }

    @media (max-width: 600px) {
      .pub-item {
        grid-template-columns: 1fr;
        gap: 16px;
      }

      .pub-image {
        height: 160px;
      }
    }
  </style>

  <div class="pub-container">
    <!-- Publication 1 -->
    <div class="pub-item">
      <div class="pub-image">
        <div class="pub-badge">arXiv</div>
        <img src='https://raw.githubusercontent.com/BV003/images/main/paper/2.png' alt="NeuronScope Paper">
      </div>
      <div class="pub-content">
        <div class="pub-title">NeuronScope: A Multi-Agent Framework for Explaining Polysemantic Neurons in Language Models</div>
        <div class="pub-authors"><strong>Weiqi Liu</strong>, Yongliang Miao, Haiyan Zhao, Yanguang Liu, Mengnan Du</div>
        <div class="pub-venue">arXiv, 2026</div>
        <div class="pub-links">
          <a href="https://arxiv.org/pdf/2601.03671" class="pub-link" target="_blank">
            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
              <polyline points="14 2 14 8 20 8"></polyline>
            </svg>
            Paper
          </a>
        </div>
      </div>
    </div>

    <!-- Publication 2 -->
    <div class="pub-item">
      <div class="pub-image">
        <div class="pub-badge pub-badge-spotlight">NeurIPS 2025</div>
        <img src='https://raw.githubusercontent.com/BV003/images/main/paper/1.png' alt="MARS-VFL Paper">
      </div>
      <div class="pub-content">
        <div class="pub-title">MARS-VFL: A Unified Benchmark for Vertical Federated Learning with Realistic Evaluation</div>
        <div class="pub-authors">Wei Shen, <strong>Weiqi Liu</strong>, Mingde Chen, Wenke Huang, Mang Ye</div>
        <div class="pub-venue">NeurIPS, 2025 <span style="color: var(--black); font-weight: 600;">(Spotlight)</span></div>
        <div class="pub-links">
          <a href="https://neurips.cc/virtual/2025/poster/121843" class="pub-link" target="_blank">
            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
              <polyline points="14 2 14 8 20 8"></polyline>
            </svg>
            Paper
          </a>
          <a href="https://github.com/shentt67/MARS-VFL" class="pub-link" target="_blank">
            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
            </svg>
            Code
          </a>
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

<div style="display: flex; align-items: center; gap: 15px; font-family: 'Segoe UI', Tahoma, sans-serif;">
  <div style="display: flex; 
  align-items: center; 
  gap: 16px;
  padding: 21px 0;
  background-color: #ffffff;
  border-radius: 4px;
  ">
    <img src="/images/whu.png" 
        alt="Wuhan University Logo" 
        style="width:75px; height:75px; border-radius:50%; border:1px solid #ccc;">
    <div>
        <strong>Wuhan University</strong><br>
        B.S. in Software Engineering<br>
        2022 - 2026
    </div>

  </div>         
</div>
</section>


<section class="section">
  <h2 class="section-title">
    Service
  </h2>

  <div class="experience-card">
    <div class="experience-header">
      <div class="company-info">
        <div class="company-name-row">
          <span class="company-name">Reviewer</span>
          <span class="experience-date-inline">2025</span>
        </div>
        <div class="company-role">Applied AI Letters</div>
      </div>
    </div>
  </div>

</section>



<section class="section">
  <h2 class="section-title">Contact</h2>
  
  <div class="email-container">
    <a href="mailto:michaelliuwq003@gmail.com" class="email-link experience-card">
      <svg class="email-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <rect x="2" y="4" width="20" height="16" rx="2"/>
        <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/>
      </svg>
      <span>michaelliuwq003@gmail.com</span>
    </a>
    <a href="mailto:2022302111185@whu.edu.cn" class="email-link experience-card">
      <svg class="email-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <rect x="2" y="4" width="20" height="16" rx="2"/>
        <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/>
      </svg>
      <span>2022302111185@whu.edu.cn</span>
    </a>
  </div>

  <style>
    .email-container {
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-top: 8px;
    }
    
    .email-link {
      display: flex;
      align-items: center;
      gap: 12px;
      padding: 16px 20px;
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 12px;
      text-decoration: none;
      color: var(--text);
      font-family: 'Source Sans 3', sans-serif;
      font-size: 14px;
      transition: all 0.3s ease;
    }
    
    .email-link:hover {
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
      transform: translateY(-2px);
    }
    
    .email-icon {
      width: 18px;
      height: 18px;
      color: var(--text-light);
      transition: color 0.25s ease;
    }
    
    .email-link:hover .email-icon {
      color: var(--black);
    }
  </style>
</section>

<div style="width: 200px; background-color: #ffffff;  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15); padding: 2px; margin: 5px auto; transition: transform 0.3s ease;">

  <a href='https://mapmyvisitors.com/web/1byw8'  title='Visit tracker' style="display: block; text-decoration: none;">
    <img src='https://mapmyvisitors.com/map.png?cl=ffffff&w=300&t=tt&d=oA1TaZZoeaTCZHmXfZ8HSPLWF_P3209OAemPCXcoJW8'
        style="width: 100%; height: auto; border-radius: 6px; border: 1px solid #f0f0f0;"
        onmouseover="this.parentNode.parentNode.style.transform='translateY(-3px)'"
        onmouseout="this.parentNode.parentNode.style.transform='translateY(0)'">
  </a>
</div>

</div>

</body>
</html>




