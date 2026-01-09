---
permalink: /
# title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
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

    /* Section Styling */
    .section {
      padding: 0px 0;
      /* border-top: 1px solid var(--border); */
    }

    .section h2 { 
      margin: 0 !important;
    }

    .section-title {
      font-family: 'Crimson Pro', Georgia, serif;
      font-size: 1.5rem;
      font-weight: 600;
      color: var(--primary);
      margin-bottom: 16px;
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
</style>
</head>

<body>

<section class="section">
  <h2 class="section-title">
    About Me
  </h2>


Hi 👋  
I'm Michael Liu.  
I am currently studying artificial intelligence and software engineering.  
I aim to become one of the top engineers in the world.
</section>


<div class="announcement-container" style="
    max-width: 660px;
    margin: 0 auto 0 auto;
    padding: 1.5rem 2rem; 
    background-color: #f8f9fa;
    border-radius: 4px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    
">
    <h3 style="
        margin-top: 0;
        margin-bottom: 0.75rem;
        color: #2c3e50;
        font-family: 'Helvetica Neue', Arial, sans-serif;
        display: flex;
        align-items: center;
    ">
        <span style="margin-right: 0.5rem;">📢</span>
        Announcement
    </h3>
    <p style="
        margin: 0;
        color: #34495e;
        font-size: 1.05rem;
        line-height: 1.6;
        font-family: 'Georgia', serif;
    ">
        For any suggestions or collaborations, please feel free to drop me an e-mail!
    </p>
</div>



<section class="section">
  <h2 class="section-title">
    Research
  </h2>


<p class="tight">My current research focuses on agent, with the aim of improving them for better performance. At the same time, I have a strong interest in post-training for large language models. From a broader perspective, my research goals are twofold:</p>  
<p class="tight">To continuously make new discoveries in the field of artificial intelligence. The rapid development of AI is remarkable, and I believe there are still many untapped treasures waiting to be explored.</p> 
<p class="tight">To create practical technologies that solve real-world problems. I am committed to applying AI techniques to solve real-world problems and bring advanced algorithms into everyday applications.</p> 

</section>




<section class="section">
  <h2 class="section-title">
    News
  </h2>

<div class="news-container">

  <div class="news-item">
    <span class="news-date">Jan 2026</span>
    <div class="news-content">
      One paper related to AI interpretability is now available on arXiv. Feel free to check it out.🎉
    </div>
  </div>

  <div class="news-item">
    <span class="news-date">Sep 2025</span>
    <div class="news-content">
      One paper is accepted to NeurIPS 2025(Spotlight). Thanks to all my collaborators.🥰
    </div>
  </div>
  
</div>

</section>


<!-- ## Experience -->



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
[[**paper**](https://arxiv.org/pdf/2601.03671)]<br>
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
[[**paper**](https://neurips.cc/virtual/2025/poster/121843)] [[**code**](https://github.com/shentt67/MARS-VFL)]  
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
  padding: 21px;
  background-color: #f8f9fa;
  border-radius: 4px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
    <div>
        <div style="font-weight: bold;font-size: 1em;">B.S. in Software Engineering</div>
        <div style="font-style: italic; color: #555;">Wuhan University</div>
        <div style="font-style: italic; color: #555;">2022 - 2026</div>
    </div>
    <img src="/images/whu.png" 
         alt="Wuhan University Logo" 
         style="width:75px; height:75px; border-radius:50%; border:1px solid #ccc;">
  </div>         
</div>
</section>


<section class="section">
  <h2 class="section-title">
    Service
  </h2>

<strong>Reviewer</strong>: Applied AI Letters(2025)

</section>



<section class="section">
  <h2 class="section-title">
    Email  
  </h2>
<div style="display: flex; flex-direction: column; align-items: flex-start; gap: 8px; font-family: 'Segoe UI', Tahoma, sans-serif; font-size: 1em; color: #333;">
    <div style="display: flex; align-items: center; gap: 10px;">
        <span style="font-weight: bold; color: #555;">🖂</span>
        <a href="mailto:michaelliuwq003@gmail.com" style="text-decoration: none; color: #000000;">michaelliuwq003@gmail.com</a>
    </div>
    <div style="display: flex; align-items: center; gap: 10px;">
        <span style="font-weight: bold; color: #555;">🖂</span>
        <a href="mailto:2022302111185@whu.edu.cn" style="text-decoration: none; color: #000000;">2022302111185@whu.edu.cn</a>
    </div>
</div>

</section>

<div style="width: 150px; background-color: #ffffff;  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15); padding: 2px; margin: 5px auto; transition: transform 0.3s ease;">
  <a href="https://mapmyvisitors.com/web/1byw8" title="Visit tracker" style="display: block; text-decoration: none;">
    <img src="https://mapmyvisitors.com/map.png?d=oA1TaZZoeaTCZHmXfZ8HSPLWF_P3209OAemPCXcoJW8&cl=ffffff" 
         style="width: 100%; height: auto; border-radius: 6px; border: 1px solid #f0f0f0;"
         onmouseover="this.parentNode.parentNode.style.transform='translateY(-3px)'"
         onmouseout="this.parentNode.parentNode.style.transform='translateY(0)'">
  </a>
</div>
</body>
</html>




