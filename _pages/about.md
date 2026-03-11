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
<div class='paper-box'>
<div class='paper-box-image'>
    <div>
      <div class="badge">arxiv</div>
      <img src='https://raw.githubusercontent.com/BV003/images/main/paper/2.png' alt="sym" width="100%">
    </div>
</div>
<div class='paper-box-text' markdown="1">  
NeuronScope: A Multi-Agent Framework for Explaining Polysemantic Neurons in Language Models    
[**paper**](https://arxiv.org/pdf/2601.03671)<br>
**Weiqi Liu**, Yongliang Miao, Haiyan Zhao, Yanguang Liu, Mengnan Du   
arxiv
</div>
</div>

<div style="height: 20px;"></div>

<div class='paper-box'>
<div class='paper-box-image'>
    <div>
      <div class="badge">NeurIPS 2025</div>
      <img src='https://raw.githubusercontent.com/BV003/images/main/paper/1.png' alt="sym" width="100%">
    </div>
</div>
<div class='paper-box-text' markdown="1">  
MARS-VFL: A Unified Benchmark for Vertical Federated Learning with Realistic Evaluation    
[**paper**](https://neurips.cc/virtual/2025/poster/121843) [**code**](https://github.com/shentt67/MARS-VFL)<br>
Wei Shen, **Weiqi Liu**, Mingde Chen, Wenke Huang, Mang Ye  
NeurIPS, 2025, Spotlight
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




