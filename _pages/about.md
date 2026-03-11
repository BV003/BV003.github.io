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
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

  <style>
    :root {
      --primary: #1a1a2e;
      --secondary: #16213e;
      --accent: #0f3460;
      --highlight: #e94560;
      --text: #2d3748;
      --text-light: #718096;
      --bg: #f7fafc;
      --bg-card: #ffffff;
      --border: #e2e8f0;
      --shadow: rgba(0, 0, 0, 0.1);
      --gradient-start: #667eea;
      --gradient-end: #764ba2;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Source Sans 3', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }

    /* Navigation */
    .navbar {
      background: var(--bg-card);
      border-bottom: 1px solid var(--border);
      padding: 1rem 0;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 2px 10px var(--shadow);
    }

    .nav-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .nav-brand {
      font-family: 'Crimson Pro', serif;
      font-size: 1.5rem;
      font-weight: 700;
      color: var(--primary);
      text-decoration: none;
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text);
      font-weight: 500;
      transition: color 0.3s;
      position: relative;
    }

    .nav-links a:hover {
      color: var(--highlight);
    }

    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--highlight);
      transition: width 0.3s;
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    /* Main Layout */
    .main-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 3rem 2rem;
      display: grid;
      grid-template-columns: 320px 1fr;
      gap: 3rem;
    }

    /* Left Sidebar */
    .sidebar {
      position: sticky;
      top: 100px;
      height: fit-content;
    }

    .profile-card {
      background: var(--bg-card);
      border-radius: 20px;
      padding: 2rem;
      box-shadow: 0 10px 40px var(--shadow);
      text-align: center;
      margin-bottom: 1.5rem;
    }

    .profile-image {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      object-fit: cover;
      border: 4px solid var(--bg);
      box-shadow: 0 4px 20px var(--shadow);
      margin-bottom: 1rem;
      transition: transform 0.3s;
    }

    .profile-image:hover {
      transform: scale(1.05);
    }

    .profile-name {
      font-family: 'Crimson Pro', serif;
      font-size: 1.5rem;
      font-weight: 700;
      color: var(--primary);
      margin-bottom: 0.5rem;
    }

    .profile-title {
      color: var(--text-light);
      font-size: 0.9rem;
      margin-bottom: 1.5rem;
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 1rem;
      margin-bottom: 1.5rem;
    }

    .social-links a {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background: var(--bg);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--text);
      text-decoration: none;
      transition: all 0.3s;
    }

    .social-links a:hover {
      background: var(--highlight);
      color: white;
      transform: translateY(-3px);
    }

    .quick-links {
      background: var(--bg-card);
      border-radius: 15px;
      padding: 1.5rem;
      box-shadow: 0 5px 20px var(--shadow);
    }

    .quick-links h3 {
      font-family: 'Crimson Pro', serif;
      font-size: 1.1rem;
      margin-bottom: 1rem;
      color: var(--primary);
    }

    .quick-link {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      padding: 0.75rem;
      text-decoration: none;
      color: var(--text);
      border-radius: 8px;
      transition: all 0.3s;
      margin-bottom: 0.5rem;
    }

    .quick-link:hover {
      background: var(--bg);
      color: var(--highlight);
    }

    .quick-link i {
      width: 20px;
      color: var(--highlight);
    }

    /* Right Content */
    .content {
      display: flex;
      flex-direction: column;
      gap: 2.5rem;
    }

    /* Section Styling */
    .section {
      background: var(--bg-card);
      border-radius: 20px;
      padding: 2rem;
      box-shadow: 0 5px 20px var(--shadow);
    }

    .section-header {
      display: flex;
      align-items: center;
      gap: 1rem;
      margin-bottom: 1.5rem;
      padding-bottom: 1rem;
      border-bottom: 2px solid var(--border);
    }

    .section-icon {
      width: 45px;
      height: 45px;
      background: linear-gradient(135deg, var(--gradient-start), var(--gradient-end));
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 1.2rem;
    }

    .section-title {
      font-family: 'Crimson Pro', serif;
      font-size: 1.5rem;
      font-weight: 700;
      color: var(--primary);
    }

    /* About Section */
    .about-content {
      font-size: 1.05rem;
      line-height: 1.8;
    }

    .about-content strong {
      color: var(--highlight);
    }

    .highlight-box {
      background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(118, 75, 162, 0.1));
      border-left: 4px solid var(--gradient-start);
      padding: 1.5rem;
      border-radius: 0 12px 12px 0;
      margin-top: 1.5rem;
    }

    .highlight-box p {
      margin: 0;
      color: var(--text);
    }

    /* News Section */
    .news-container {
      max-height: 300px;
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
      padding: 1rem 0;
      border-bottom: 1px solid var(--border);
      display: grid;
      grid-template-columns: 100px 1fr;
      gap: 1rem;
      align-items: start;
      transition: all 0.3s;
    }

    .news-item:last-child {
      border-bottom: none;
    }

    .news-item:hover {
      background: rgba(102, 126, 234, 0.03);
      margin: 0 -1rem;
      padding-left: 1rem;
      padding-right: 1rem;
      border-radius: 8px;
    }

    .news-date {
      font-weight: 600;
      color: var(--highlight);
      font-size: 0.9rem;
      font-family: 'Crimson Pro', serif;
    }

    .news-content {
      color: var(--text);
      line-height: 1.6;
    }

    .news-content a {
      color: var(--accent);
      text-decoration: none;
      font-weight: 600;
    }

    .news-content a:hover {
      text-decoration: underline;
    }

    /* Experience Cards */
    .experience-card {
      background: linear-gradient(135deg, var(--bg), var(--bg-card));
      border: 1px solid var(--border);
      border-radius: 15px;
      padding: 1.5rem;
      margin-bottom: 1rem;
      transition: all 0.3s;
      position: relative;
      overflow: hidden;
    }

    .experience-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 4px;
      height: 100%;
      background: linear-gradient(180deg, var(--gradient-start), var(--gradient-end));
    }

    .experience-card:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 30px var(--shadow);
    }

    .experience-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 0.5rem;
    }

    .company-name {
      font-family: 'Crimson Pro', serif;
      font-size: 1.3rem;
      font-weight: 700;
      color: var(--primary);
    }

    .experience-date {
      background: var(--bg);
      padding: 0.3rem 0.8rem;
      border-radius: 20px;
      font-size: 0.85rem;
      color: var(--text-light);
      font-weight: 600;
    }

    .company-role {
      color: var(--text-light);
      font-size: 0.95rem;
    }

    /* Publications */
    .publication-grid {
      display: grid;
      gap: 1.5rem;
    }

    .publication-card {
      background: var(--bg);
      border-radius: 15px;
      overflow: hidden;
      display: grid;
      grid-template-columns: 200px 1fr;
      transition: all 0.3s;
      border: 1px solid var(--border);
    }

    .publication-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 40px var(--shadow);
    }

    .publication-image {
      position: relative;
      overflow: hidden;
    }

    .publication-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.3s;
    }

    .publication-card:hover .publication-image img {
      transform: scale(1.05);
    }

    .publication-badge {
      position: absolute;
      top: 10px;
      left: 10px;
      background: linear-gradient(135deg, var(--highlight), #ff6b6b);
      color: white;
      padding: 0.3rem 0.8rem;
      border-radius: 20px;
      font-size: 0.75rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .publication-content {
      padding: 1.5rem;
    }

    .publication-title {
      font-family: 'Crimson Pro', serif;
      font-size: 1.2rem;
      font-weight: 700;
      color: var(--primary);
      margin-bottom: 0.75rem;
      line-height: 1.4;
    }

    .publication-authors {
      color: var(--text-light);
      font-size: 0.95rem;
      margin-bottom: 0.5rem;
    }

    .publication-venue {
      color: var(--highlight);
      font-weight: 600;
      font-size: 0.9rem;
      margin-bottom: 1rem;
    }

    .publication-links {
      display: flex;
      gap: 0.75rem;
    }

    .pub-link {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.4rem 1rem;
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 20px;
      text-decoration: none;
      color: var(--text);
      font-size: 0.85rem;
      font-weight: 500;
      transition: all 0.3s;
    }

    .pub-link:hover {
      background: var(--highlight);
      color: white;
      border-color: var(--highlight);
    }

    /* Education */
    .education-item {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      padding: 1.5rem;
      background: var(--bg);
      border-radius: 15px;
      transition: all 0.3s;
    }

    .education-item:hover {
      background: linear-gradient(135deg, rgba(102, 126, 234, 0.05), rgba(118, 75, 162, 0.05));
    }

    .edu-logo {
      width: 70px;
      height: 70px;
      border-radius: 50%;
      object-fit: cover;
      border: 3px solid var(--bg-card);
      box-shadow: 0 4px 15px var(--shadow);
    }

    .edu-info h3 {
      font-family: 'Crimson Pro', serif;
      color: var(--primary);
      margin-bottom: 0.3rem;
    }

    .edu-info p {
      color: var(--text-light);
      font-size: 0.95rem;
    }

    /* Contact Section */
    .contact-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1rem;
    }

    .contact-card {
      display: flex;
      align-items: center;
      gap: 1rem;
      padding: 1rem;
      background: var(--bg);
      border-radius: 12px;
      text-decoration: none;
      color: var(--text);
      transition: all 0.3s;
      border: 1px solid var(--border);
    }

    .contact-card:hover {
      background: linear-gradient(135deg, var(--gradient-start), var(--gradient-end));
      color: white;
      transform: translateY(-3px);
      box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
    }

    .contact-icon {
      width: 45px;
      height: 45px;
      background: var(--bg-card);
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--highlight);
      font-size: 1.1rem;
    }

    .contact-card:hover .contact-icon {
      background: rgba(255, 255, 255, 0.2);
      color: white;
    }

    .contact-info {
      font-size: 0.9rem;
    }

    .contact-info strong {
      display: block;
      margin-bottom: 0.2rem;
    }

    /* Visitor Counter */
    .visitor-counter {
      text-align: center;
      margin-top: 2rem;
      padding: 1rem;
      background: var(--bg-card);
      border-radius: 15px;
      box-shadow: 0 5px 20px var(--shadow);
    }

    .visitor-counter img {
      border-radius: 8px;
      max-width: 100%;
    }

    /* Responsive Design */
    @media (max-width: 900px) {
      .main-container {
        grid-template-columns: 1fr;
        padding: 1.5rem;
      }

      .sidebar {
        position: static;
        margin-bottom: 2rem;
      }

      .publication-card {
        grid-template-columns: 1fr;
      }

      .publication-image {
        height: 150px;
      }

      .contact-grid {
        grid-template-columns: 1fr;
      }

      .nav-links {
        gap: 1rem;
        font-size: 0.9rem;
      }
    }

    @media (max-width: 600px) {
      .nav-container {
        flex-direction: column;
        gap: 1rem;
      }

      .section {
        padding: 1.5rem;
      }

      .experience-header {
        flex-direction: column;
        gap: 0.5rem;
      }

      .news-item {
        grid-template-columns: 1fr;
        gap: 0.5rem;
      }
    }
  </style>
  </head>

<body>
  <!-- Navigation -->
  <nav class="navbar">
    <div class="nav-container">
      <a href="/" class="nav-brand">Michael Liu</a>
      <ul class="nav-links">
        <li><a href="/files/cv.pdf"><i class="fas fa-file-alt"></i> CV</a></li>
        <li><a href="https://bv003me.vercel.app/" target="_blank"><i class="fas fa-blog"></i> Blog</a></li>
      </ul>
    </div>
  </nav>

  <div class="main-container">
    <!-- Left Sidebar -->
    <aside class="sidebar">
      <div class="profile-card">
        <img src="/images/profile.png" alt="Michael Liu" class="profile-image">
        <h1 class="profile-name">Weiqi Liu</h1>
        <p class="profile-title">Michael | AI Researcher</p>
        
        <div class="social-links">
          <a href="https://github.com/BV003" target="_blank" title="GitHub">
            <i class="fab fa-github"></i>
          </a>
          <a href="mailto:michaelliuwq003@gmail.com" title="Email">
            <i class="fas fa-envelope"></i>
          </a>
          <a href="https://scholar.google.com" target="_blank" title="Google Scholar">
            <i class="fas fa-graduation-cap"></i>
          </a>
          <a href="https://linkedin.com" target="_blank" title="LinkedIn">
            <i class="fab fa-linkedin-in"></i>
          </a>
        </div>
      </div>

      <div class="quick-links">
        <h3>Quick Links</h3>
        <a href="/files/cv.pdf" class="quick-link">
          <i class="fas fa-file-pdf"></i>
          <span>Download CV</span>
        </a>
        <a href="https://bv003me.vercel.app/" class="quick-link" target="_blank">
          <i class="fas fa-blog"></i>
          <span>My Blog</span>
        </a>
        <a href="mailto:michaelliuwq003@gmail.com" class="quick-link">
          <i class="fas fa-envelope"></i>
          <span>Contact Me</span>
        </a>
      </div>
    </aside>

    <!-- Right Content -->
    <main class="content">
      <!-- About Section -->
      <section class="section">
        <div class="section-header">
          <div class="section-icon">
            <i class="fas fa-user"></i>
          </div>
          <h2 class="section-title">About Me</h2>
        </div>
        <div class="about-content">
          <p>Hi! I'm Weiqi Liu, and you can call me <strong>Michael</strong>.</p>
          <br>
          <p>I aim to become one of the <strong>top engineers</strong> in the world, leveraging the power of AI to solve real-world problems.</p>
          
          <div class="highlight-box">
            <p>For any <strong>suggestions</strong> or <strong>collaborations</strong>, please feel free to reach out to me via email!</p>
          </div>
        </div>
      </section>

      <!-- Research Section -->
      <section class="section">
        <div class="section-header">
          <div class="section-icon">
            <i class="fas fa-brain"></i>
          </div>
          <h2 class="section-title">Research Interests</h2>
        </div>
        <div class="about-content">
          <p>My primary focus is currently on <strong>artificial intelligence</strong> research. The emergence of large language models has greatly accelerated technological innovation and can automate many repetitive cognitive tasks.</p>
          <br>
          <p>When these models are integrated with software and hardware, they enable large-scale automation in the real world. I believe that researching how to build more efficient AI models and exploring their practical applications is a highly promising direction.</p>
          <br>
          <p>Additionally, I'm deeply passionate about <strong>investing</strong>, <strong>Web3 technologies</strong>, <strong>literary writing</strong>, and <strong>aesthetics</strong>.</p>
        </div>
      </section>

      <!-- News Section -->
      <section class="section">
        <div class="section-header">
          <div class="section-icon">
            <i class="fas fa-newspaper"></i>
          </div>
          <h2 class="section-title">Latest News</h2>
        </div>
        <div class="news-container">
          <div class="news-item">
            <span class="news-date">Jan 2026</span>
            <div class="news-content">
              <i class="fab fa-apple" style="color: #555;"></i> Excited to begin my role as an <strong>AI Software Engineer Intern</strong> at Apple!
            </div>
          </div>
          <div class="news-item">
            <span class="news-date">Jan 2026</span>
            <div class="news-content">
              🎉 One paper on <strong>AI interpretability</strong> is now available on arXiv!
            </div>
          </div>
          <div class="news-item">
            <span class="news-date">Sep 2025</span>
            <div class="news-content">
              🥳 One paper accepted to <strong>NeurIPS 2025 (Spotlight)</strong>. Thanks to all collaborators!
            </div>
          </div>
        </div>
      </section>

      <!-- Work Experience -->
      <section class="section">
        <div class="section-header">
          <div class="section-icon">
            <i class="fas fa-briefcase"></i>
          </div>
          <h2 class="section-title">Work Experience</h2>
        </div>
        
        <div class="experience-card">
          <div class="experience-header">
            <div>
              <div class="company-name">Apple</div>
              <div class="company-role">AI Software Engineer Intern</div>
            </div>
            <span class="experience-date">2026</span>
          </div>
        </div>
      </section>

      <!-- Academic Publications -->
      <section class="section">
        <div class="section-header">
          <div class="section-icon">
            <i class="fas fa-book"></i>
          </div>
          <h2 class="section-title">Academic Publications</h2>
        </div>
        
        <div class="publication-grid">
          <div class="publication-card">
            <div class="publication-image">
              <div class="publication-badge">arxiv</div>
              <img src="https://raw.githubusercontent.com/BV003/images/main/paper/2.png" alt="NeuronScope">
            </div>
            <div class="publication-content">
              <h3 class="publication-title">NeuronScope: A Multi-Agent Framework for Explaining Polysemantic Neurons in Language Models</h3>
              <p class="publication-authors"><strong>Weiqi Liu</strong>, Yongliang Miao, Haiyan Zhao, Yanguang Liu, Mengnan Du</p>
              <p class="publication-venue">arxiv 2026</p>
              <div class="publication-links">
                <a href="https://arxiv.org/pdf/2601.03671" class="pub-link" target="_blank">
                  <i class="fas fa-file-pdf"></i> Paper
                </a>
              </div>
            </div>
          </div>

          <div class="publication-card">
            <div class="publication-image">
              <div class="publication-badge" style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);">NeurIPS 2025</div>
              <img src="https://raw.githubusercontent.com/BV003/images/main/paper/1.png" alt="MARS-VFL">
            </div>
            <div class="publication-content">
              <h3 class="publication-title">MARS-VFL: A Unified Benchmark for Vertical Federated Learning with Realistic Evaluation</h3>
              <p class="publication-authors">Wei Shen, <strong>Weiqi Liu</strong>, Mingde Chen, Wenke Huang, Mang Ye</p>
              <p class="publication-venue">NeurIPS 2025, Spotlight</p>
              <div class="publication-links">
                <a href="https://neurips.cc/virtual/2025/poster/121843" class="pub-link" target="_blank">
                  <i class="fas fa-file-pdf"></i> Paper
                </a>
                <a href="https://github.com/shentt67/MARS-VFL" class="pub-link" target="_blank">
                  <i class="fab fa-github"></i> Code
                </a>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Education -->
      <section class="section">
        <div class="section-header">
          <div class="section-icon">
            <i class="fas fa-graduation-cap"></i>
          </div>
          <h2 class="section-title">Education</h2>
        </div>
        
        <div class="education-item">
          <img src="/images/whu.png" alt="Wuhan University" class="edu-logo">
          <div class="edu-info">
            <h3>Wuhan University</h3>
            <p>B.S. in Software Engineering • 2022 - 2026</p>
          </div>
        </div>
      </section>

      <!-- Service -->
      <section class="section">
        <div class="section-header">
          <div class="section-icon">
            <i class="fas fa-hands-helping"></i>
          </div>
          <h2 class="section-title">Academic Service</h2>
        </div>
        
        <div class="experience-card">
          <div class="experience-header">
            <div>
              <div class="company-name">Reviewer</div>
              <div class="company-role">Applied AI Letters</div>
            </div>
            <span class="experience-date">2025</span>
          </div>
        </div>
      </section>

      <!-- Contact -->
      <section class="section">
        <div class="section-header">
          <div class="section-icon">
            <i class="fas fa-envelope"></i>
          </div>
          <h2 class="section-title">Get In Touch</h2>
        </div>
        
        <div class="contact-grid">
          <a href="mailto:michaelliuwq003@gmail.com" class="contact-card">
            <div class="contact-icon">
              <i class="fas fa-envelope"></i>
            </div>
            <div class="contact-info">
              <strong>Personal Email</strong>
              <span>michaelliuwq003@gmail.com</span>
            </div>
          </a>
          
          <a href="mailto:2022302111185@whu.edu.cn" class="contact-card">
            <div class="contact-icon">
              <i class="fas fa-university"></i>
            </div>
            <div class="contact-info">
              <strong>University Email</strong>
              <span>2022302111185@whu.edu.cn</span>
            </div>
          </a>
        </div>
      </section>

      <!-- Visitor Counter -->
      <div class="visitor-counter">
        <a href='https://mapmyvisitors.com/web/1byw8' title='Visit tracker'>
          <img src='https://mapmyvisitors.com/map.png?cl=ffffff&w=300&t=tt&d=oA1TaZZoeaTCZHmXfZ8HSPLWF_P3209OAemPCXcoJW8' alt="Visitor Map">
        </a>
      </div>
    </main>
  </div>
</body>
</html>
