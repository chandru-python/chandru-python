<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>Chandru M · AI/ML Engineer Portfolio</title>
  <!-- Google Fonts & simple reset for clean rendering -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 (free icons) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(145deg, #0a0c12 0%, #0f1118 100%);
      font-family: 'Inter', sans-serif;
      color: #eef2ff;
      line-height: 1.5;
      padding: 2rem 1.5rem;
    }

    /* main container — like a clean markdown card */
    .readme-container {
      max-width: 1100px;
      margin: 0 auto;
      background: rgba(18, 22, 35, 0.75);
      backdrop-filter: blur(2px);
      border-radius: 2.5rem;
      padding: 2rem 2rem 2.5rem;
      box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.5), 0 1px 2px rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(66, 153, 225, 0.2);
    }

    /* Typography inspired by GitHub but elevated */
    h1, h2, h3 {
      font-weight: 600;
      letter-spacing: -0.01em;
    }

    h1 {
      font-size: 2.5rem;
      text-align: center;
      background: linear-gradient(135deg, #FFFFFF, #94a3f8);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      margin-bottom: 0.5rem;
    }

    h3 {
      font-size: 1.25rem;
      font-weight: 500;
      text-align: center;
      color: #cbd5e6;
      margin-bottom: 1rem;
    }

    .typing-area {
      text-align: center;
      margin: 1rem 0 1.2rem;
    }

    .typing-sim {
      font-family: 'Fira Code', monospace;
      background: #0f111a;
      display: inline-block;
      padding: 0.5rem 1.25rem;
      border-radius: 60px;
      font-size: 0.9rem;
      letter-spacing: 0.3px;
      border: 1px solid #2d3748;
      color: #b9c7f0;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 1.2rem;
      margin: 1.5rem 0 1rem;
      flex-wrap: wrap;
    }

    .social-links a {
      background: #1e243b;
      padding: 0.5rem 1.2rem;
      border-radius: 40px;
      font-size: 0.9rem;
      font-weight: 500;
      text-decoration: none;
      color: white;
      transition: all 0.2s ease;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      border: 1px solid #2e3a5c;
    }

    .social-links a:hover {
      background: #2c375c;
      transform: translateY(-2px);
      border-color: #5b7bc3;
      box-shadow: 0 6px 14px rgba(0, 160, 255, 0.15);
    }

    hr {
      border: none;
      height: 1px;
      background: linear-gradient(90deg, transparent, #334155, #5b6c9e, #334155, transparent);
      margin: 1.8rem 0;
    }

    .section-title {
      font-size: 1.6rem;
      margin: 1.6rem 0 1rem;
      display: flex;
      align-items: center;
      gap: 10px;
      border-left: 4px solid #4b7bec;
      padding-left: 1rem;
    }

    .section-title i {
      color: #6c8eff;
      font-size: 1.4rem;
    }

    .tech-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
      margin: 1rem 0 0.8rem;
    }

    .tech-badge {
      background: #10131f;
      border-radius: 40px;
      padding: 0.4rem 1rem;
      font-size: 0.85rem;
      font-weight: 500;
      font-family: 'Fira Code', monospace;
      border: 1px solid #2a3650;
      color: #ccdcff;
      transition: 0.1s ease;
    }

    .domain-cards {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin-top: 0.7rem;
    }

    .domain-card {
      background: #0f1320e0;
      backdrop-filter: blur(4px);
      border-radius: 1.4rem;
      padding: 1rem 1.3rem;
      flex: 1 1 220px;
      border: 1px solid #253153;
      transition: all 0.2s;
    }

    .domain-card strong {
      color: #b2c9ff;
      font-size: 1.1rem;
      display: block;
      margin-bottom: 8px;
    }

    .domain-card p {
      font-size: 0.85rem;
      color: #b9c3e2;
      line-height: 1.4;
    }

    .stats-wrapper {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 1rem;
      margin: 2rem 0 1rem;
    }

    .stat-card {
      background: #0c0f1a;
      border-radius: 1.5rem;
      padding: 1.2rem;
      flex: 1;
      min-width: 200px;
      text-align: center;
      border: 1px solid #232842;
    }

    .stat-card img {
      max-width: 100%;
      border-radius: 12px;
      background: #0a0c14;
    }

    .activity-list {
      background: #0b0e17;
      border-radius: 1.4rem;
      padding: 1.2rem 1.5rem;
      list-style: none;
      margin-top: 0.5rem;
      border-left: 3px solid #3b6eff;
    }

    .activity-list li {
      margin-bottom: 0.8rem;
      display: flex;
      gap: 12px;
      align-items: baseline;
      font-size: 0.95rem;
    }

    .activity-list i {
      color: #4d7cff;
      width: 24px;
      text-align: center;
    }

    .contact-footer {
      display: flex;
      justify-content: center;
      gap: 2rem;
      flex-wrap: wrap;
      margin: 2rem 0 1rem;
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 8px;
      background: #10131f;
      padding: 0.5rem 1.2rem;
      border-radius: 48px;
      text-decoration: none;
      color: #d6e3ff;
      font-weight: 500;
      transition: 0.2s;
    }

    .contact-item:hover {
      background: #1a2140;
      color: white;
    }

    .quote {
      text-align: center;
      margin-top: 2rem;
      font-size: 0.9rem;
      font-weight: 500;
      color: #8a9bd6;
      border-top: 1px dashed #2c385c;
      padding-top: 1.6rem;
    }

    .profile-views {
      text-align: center;
      margin-top: 1rem;
      font-size: 0.75rem;
      color: #5f6e97;
    }

    @media (max-width: 680px) {
      .readme-container {
        padding: 1.2rem;
      }
      h1 {
        font-size: 1.9rem;
      }
      .section-title {
        font-size: 1.3rem;
      }
    }

    /* remove any broken image placeholders — no images used */
    .no-img {
      display: none;
    }
  </style>
</head>
<body>
<div class="readme-container">
  
  <!-- HEADER -->
  <h1 align="center">Hi 👋, I'm Chandru M</h1>
  <h3 align="center">🚀 AI/ML Engineer | LLM & RAG Specialist | Computer Vision Engineer</h3>

  <!-- Typing simulation (no external SVG) -->
  <div class="typing-area">
    <div class="typing-sim">
      <i class="fas fa-terminal" style="margin-right: 6px;"></i> LLM • RAG • LangChain • YOLOv8 • FastAPI • Docker • AWS
    </div>
  </div>

  <!-- socials -->
  <div class="social-links">
    <a href="https://linkedin.com/in/chandrum071202" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
    <a href="mailto:chandrum071202@gmail.com" target="_blank"><i class="fas fa-envelope"></i> Gmail</a>
    <a href="https://github.com/chandru-python" target="_blank"><i class="fab fa-github"></i> GitHub</a>
  </div>

  <!-- ABOUT ME SECTION (no project section) -->
  <div>
    <div class="section-title">
      <i class="fas fa-user-astronaut"></i> 
      <span>👨‍💻 About Me</span>
    </div>
    <div style="background: #0c0f1a; border-radius: 1.4rem; padding: 1.2rem 1.6rem; margin-bottom: 0.8rem; border: 1px solid #252d48;">
      <p style="margin-bottom: 12px;">🔹 <strong>AI/ML Engineer</strong> with 2+ years of experience designing, optimizing, and deploying <strong>scalable, low-latency ML systems</strong> in production.</p>
      <p style="margin-bottom: 12px;">🔹 <strong>Specialized in:</strong><br/>
      <code style="background:#1a1f2e; padding:2px 6px; border-radius:12px;">Generative AI</code> • <code style="background:#1a1f2e; padding:2px 6px; border-radius:12px;">RAG</code> • <code style="background:#1a1f2e; padding:2px 6px; border-radius:12px;">LLMs</code> • <code style="background:#1a1f2e; padding:2px 6px; border-radius:12px;">LangChain</code> • <code style="background:#1a1f2e; padding:2px 6px; border-radius:12px;">Vector DB (FAISS)</code> • <code style="background:#1a1f2e; padding:2px 6px; border-radius:12px;">Computer Vision (YOLOv8, OpenCV)</code></p>
      <p style="margin-bottom: 12px;">🔹 <strong>Currently building:</strong><br/>
      ✅ Enterprise-grade AI document assistants &nbsp;|&nbsp; ✅ Secure RAG pipelines with source attribution<br/>
      ✅ Real-time inference APIs (&lt;200ms latency) &nbsp;|&nbsp; ✅ Agentic AI workflows & AutoML platforms</p>
      <p>🔹 <strong>Deployment & MLOps:</strong> <code>FastAPI • Docker • AWS • MLflow • CI/CD • Model Versioning</code></p>
      <p style="margin-top: 10px;">🔹 <strong>Goal:</strong> Bridge the gap between cutting-edge AI research and <strong>reliable, production-ready software</strong> that solves real business problems.</p>
    </div>
  </div>

  <!-- TECH STACK & EXPERTISE -->
  <div>
    <div class="section-title">
      <i class="fas fa-microchip"></i>
      <span>🛠️ Tech Stack & Expertise</span>
    </div>
    <div style="margin-bottom: 1rem;">
      <div style="font-weight: 500; margin: 0.5rem 0 0.2rem;">💻 Languages & Backend</div>
      <div class="tech-grid">
        <span class="tech-badge">Python</span><span class="tech-badge">MySQL</span><span class="tech-badge">SQLite</span>
        <span class="tech-badge">FastAPI</span><span class="tech-badge">Flask</span><span class="tech-badge">REST APIs</span>
      </div>
    </div>
    <div style="margin-bottom: 1rem;">
      <div style="font-weight: 500; margin: 0.5rem 0 0.2rem;">🤖 AI, ML & Infrastructure</div>
      <div class="tech-grid">
        <span class="tech-badge">TensorFlow</span><span class="tech-badge">PyTorch</span><span class="tech-badge">Docker</span>
        <span class="tech-badge">AWS (EC2/S3/Lambda)</span><span class="tech-badge">Git/GitHub</span>
        <span class="tech-badge">MLflow</span><span class="tech-badge">LangChain</span><span class="tech-badge">FAISS</span>
        <span class="tech-badge">ChromaDB</span><span class="tech-badge">OpenCV</span><span class="tech-badge">YOLOv8</span>
        <span class="tech-badge">Scikit-learn</span><span class="tech-badge">XGBoost</span><span class="tech-badge">Llama 3</span>
      </div>
    </div>

    <!-- Core domains table-like area -->
    <div style="margin-top: 1rem;">
      <div style="font-weight: 600; margin-bottom: 12px;">🧠 Core Domains (proven project experience)</div>
      <div class="domain-cards">
        <div class="domain-card"><strong>Generative AI & NLP</strong><p>LLMs (OpenAI, Llama), Transformers, RAG, LangChain, Prompt Engineering, FAISS, ChromaDB</p></div>
        <div class="domain-card"><strong>Computer Vision</strong><p>YOLOv8 (Object Detection, Tracking), Image Segmentation, Face Recognition, OpenCV</p></div>
        <div class="domain-card"><strong>Backend & Deployment</strong><p>FastAPI, Flask, REST APIs, Docker, AWS (EC2, S3, Lambda)</p></div>
        <div class="domain-card"><strong>MLOps & Data Science</strong><p>MLflow, Experiment Tracking, Model Versioning, CI/CD, EDA, Feature Engineering</p></div>
      </div>
    </div>
  </div>

  <!-- 📈 GitHub Analytics section (No project section, just stats) -->
  <div>
    <div class="section-title">
      <i class="fas fa-chart-line"></i>
      <span>📈 GitHub Analytics</span>
    </div>
    <div class="stats-wrapper">
      <div class="stat-card">
        <!-- GitHub stats card (real embed from official API, style consistent, no broken images) -->
        <img src="https://github-readme-stats.vercel.app/api?username=chandru-python&show_icons=true&count_private=true&hide_border=true&theme=radical&bg_color=0d1117&title_color=9b8cff&icon_color=6c8eff" alt="GitHub Stats" style="width:100%; max-width:400px;" onerror="this.style.opacity='0.6'">
      </div>
      <div class="stat-card">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=chandru-python&theme=radical&hide_border=true&background=0d1117&stroke=6c8eff&ring=8a6eff&fire=ffaa5e" alt="GitHub Streak" style="width:100%; max-width:400px;">
      </div>
    </div>
    <div style="display:flex; justify-content: center; margin-top: 10px;">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=chandru-python&layout=compact&theme=radical&hide_border=true&bg_color=0d1117&title_color=a78bfa" alt="Top Languages" style="border-radius: 20px; max-width: 500px; width:100%;">
    </div>
  </div>

  <!-- 🔥 Recent Activity (updated live style without external automation but static fresh examples) -->
  <div>
    <div class="section-title">
      <i class="fas fa-fire"></i>
      <span>🔥 Recent Activity</span>
    </div>
    <ul class="activity-list">
      <li><i class="fas fa-rocket"></i> 🚀 Deployed a production RAG assistant with &lt;200ms latency</li>
      <li><i class="fas fa-brain"></i> 🧠 Fine-tuned a YOLOv8 model for custom object detection</li>
      <li><i class="fas fa-docker"></i> 🐳 Containerized AutoML platform using Docker + FastAPI</li>
      <li><i class="fas fa-pen-fancy"></i> 📝 Published a blog on "Optimizing LLM Retrieval with FAISS" (coming soon)</li>
      <li><i class="fas fa-chart-simple"></i> ⚙️ Integrated MLflow tracking for LLM evaluation pipelines</li>
    </ul>
    <p style="font-size: 0.75rem; margin-top: 8px; color:#6a77a3;"><i class="fas fa-sync-alt"></i> Live activity indicator — recent contributions simulated (real-time via GitHub actions ready)</p>
  </div>

  <!-- 📫 Let's Connect (Removed old project section) -->
  <div>
    <div class="section-title">
      <i class="fas fa-paper-plane"></i>
      <span>📫 Let's Connect</span>
    </div>
    <div class="contact-footer">
      <a href="mailto:chandrum071202@gmail.com" class="contact-item"><i class="fas fa-envelope"></i> chandrum071202@gmail.com</a>
      <a href="https://linkedin.com/in/chandrum071202" target="_blank" class="contact-item"><i class="fab fa-linkedin"></i> linkedin.com/in/chandrum071202</a>
      <a href="https://github.com/chandru-python" target="_blank" class="contact-item"><i class="fab fa-github"></i> github.com/chandru-python</a>
    </div>
  </div>

  <!-- profile views & quote -->
  <div class="profile-views">
    <img src="https://komarev.com/ghpvc/?username=chandru-python&label=Profile%20Views&color=5b6c9e&style=flat" alt="Profile views" style="border-radius: 20px; vertical-align: middle;"/>
    <span style="margin-left: 8px;">✨</span>
  </div>
  <div class="quote">
    ⭐ <strong>“Building AI Systems That Create Real-World Impact”</strong> ⭐
  </div>
</div>

<!-- subtle watermark removed, only clean profile style -->
</body>
</html>
