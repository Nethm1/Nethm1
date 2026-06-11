<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nethmi's GitHub README Preview</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Fira+Code:wght@300;400;500&display=swap');

  :root {
    --purple: #9b59b6;
    --deep-purple: #6c3483;
    --violet: #8e44ad;
    --pink: #e91e8c;
    --hot-pink: #ff6eb4;
    --blue: #3d5af1;
    --electric-blue: #0ef;
    --light-blue: #74b9ff;
    --bg-dark: #0d0d1a;
    --bg-card: #12122a;
    --bg-card2: #1a1a35;
    --text-primary: #f0e6ff;
    --text-muted: #a78bca;
    --border-glow: rgba(155, 89, 182, 0.4);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg-dark);
    font-family: 'Space Grotesk', sans-serif;
    color: var(--text-primary);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Animated background particles */
  body::before {
    content: '';
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: 
      radial-gradient(ellipse at 20% 20%, rgba(155,89,182,0.15) 0%, transparent 50%),
      radial-gradient(ellipse at 80% 80%, rgba(233,30,140,0.12) 0%, transparent 50%),
      radial-gradient(ellipse at 50% 50%, rgba(61,90,241,0.08) 0%, transparent 60%);
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 24px;
    position: relative;
    z-index: 1;
  }

  /* ── HERO ─────────────────────────────────── */
  .hero {
    text-align: center;
    padding: 48px 32px 40px;
    background: var(--bg-card);
    border-radius: 24px;
    border: 1px solid var(--border-glow);
    margin-bottom: 24px;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -80px; left: 50%;
    transform: translateX(-50%);
    width: 400px; height: 200px;
    background: radial-gradient(ellipse, rgba(155,89,182,0.35) 0%, transparent 70%);
    animation: pulse-glow 4s ease-in-out infinite;
  }

  @keyframes pulse-glow {
    0%, 100% { opacity: 0.6; transform: translateX(-50%) scale(1); }
    50% { opacity: 1; transform: translateX(-50%) scale(1.1); }
  }

  .wave-emoji {
    font-size: 2.8rem;
    display: inline-block;
    animation: wave 2.5s ease-in-out infinite;
    transform-origin: 70% 70%;
  }

  @keyframes wave {
    0%, 100% { transform: rotate(0deg); }
    10% { transform: rotate(14deg); }
    20% { transform: rotate(-8deg); }
    30% { transform: rotate(14deg); }
    40% { transform: rotate(-4deg); }
    50% { transform: rotate(10deg); }
    60% { transform: rotate(0deg); }
  }

  .hero-name {
    font-size: clamp(2.2rem, 5vw, 3.2rem);
    font-weight: 700;
    background: linear-gradient(135deg, #c084fc 0%, #e879f9 30%, #f472b6 60%, #60a5fa 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin: 12px 0 6px;
    letter-spacing: -0.5px;
    animation: shimmer 4s linear infinite;
    background-size: 200% auto;
  }

  @keyframes shimmer {
    0% { background-position: 0% center; }
    100% { background-position: 200% center; }
  }

  .hero-sub {
    font-size: 1.05rem;
    color: var(--text-muted);
    letter-spacing: 0.5px;
    margin-bottom: 20px;
  }

  .badge-row {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 16px;
  }

  .badge {
    padding: 6px 16px;
    border-radius: 99px;
    font-size: 0.82rem;
    font-weight: 500;
    font-family: 'Fira Code', monospace;
    border: 1px solid;
    animation: badge-float 3s ease-in-out infinite;
  }

  .badge:nth-child(2) { animation-delay: 0.3s; }
  .badge:nth-child(3) { animation-delay: 0.6s; }

  @keyframes badge-float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-4px); }
  }

  .badge-purple {
    background: rgba(155,89,182,0.18);
    border-color: rgba(192,132,252,0.5);
    color: #c084fc;
  }
  .badge-pink {
    background: rgba(233,30,140,0.15);
    border-color: rgba(244,114,182,0.5);
    color: #f472b6;
  }
  .badge-blue {
    background: rgba(61,90,241,0.18);
    border-color: rgba(96,165,250,0.5);
    color: #60a5fa;
  }

  /* ── TYPING EFFECT ─────────────────────────── */
  .typing-container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 8px;
    margin: 20px 0 0;
  }

  .typing-prefix {
    color: var(--hot-pink);
    font-family: 'Fira Code', monospace;
    font-size: 0.9rem;
  }

  .typing-text {
    font-family: 'Fira Code', monospace;
    font-size: 0.9rem;
    color: #a5f3fc;
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid #a5f3fc;
    width: 0;
    animation: typing 3s steps(35) 0.5s forwards, blink 0.8s step-end infinite;
  }

  @keyframes typing {
    to { width: 26ch; }
  }

  @keyframes blink {
    50% { border-color: transparent; }
  }

  /* ── SECTION CARDS ─────────────────────────── */
  .section-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin-bottom: 24px;
  }

  @media (max-width: 600px) {
    .section-grid { grid-template-columns: 1fr; }
  }

  .card {
    background: var(--bg-card);
    border: 1px solid var(--border-glow);
    border-radius: 18px;
    padding: 24px;
    transition: transform 0.3s ease, border-color 0.3s ease, box-shadow 0.3s ease;
  }

  .card:hover {
    transform: translateY(-4px);
    border-color: rgba(192,132,252,0.7);
    box-shadow: 0 8px 32px rgba(155,89,182,0.2);
  }

  .card-full {
    background: var(--bg-card);
    border: 1px solid var(--border-glow);
    border-radius: 18px;
    padding: 24px 28px;
    margin-bottom: 20px;
    transition: transform 0.3s ease, border-color 0.3s ease;
  }

  .card-full:hover {
    transform: translateY(-3px);
    border-color: rgba(232,121,249,0.6);
  }

  .card-title {
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .card-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, rgba(155,89,182,0.5), transparent);
  }

  .gradient-purple { color: #c084fc; }
  .gradient-pink { color: #f472b6; }
  .gradient-blue { color: #60a5fa; }

  /* ── ABOUT LIST ──────────────────────────────── */
  .about-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .about-list li {
    font-size: 0.9rem;
    color: #d8b4fe;
    display: flex;
    align-items: flex-start;
    gap: 10px;
    line-height: 1.5;
  }

  .about-list li span.icon {
    flex-shrink: 0;
    margin-top: 1px;
  }

  /* ── TECH STACK ──────────────────────────────── */
  .tech-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .tech-chip {
    padding: 5px 14px;
    border-radius: 8px;
    font-size: 0.8rem;
    font-family: 'Fira Code', monospace;
    font-weight: 500;
    background: var(--bg-card2);
    border: 1px solid rgba(155,89,182,0.3);
    color: #e9d5ff;
    transition: all 0.2s ease;
    cursor: default;
  }

  .tech-chip:hover {
    background: rgba(155,89,182,0.25);
    border-color: rgba(192,132,252,0.7);
    color: #fff;
    transform: scale(1.05);
  }

  .tech-chip.pink { border-color: rgba(244,114,182,0.35); color: #fbcfe8; }
  .tech-chip.blue { border-color: rgba(96,165,250,0.35); color: #bae6fd; }
  .tech-chip.green { border-color: rgba(74,222,128,0.35); color: #bbf7d0; }

  /* ── CURRENTLY WORKING ───────────────────────── */
  .project-banner {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 16px 20px;
    background: linear-gradient(135deg, rgba(155,89,182,0.2), rgba(61,90,241,0.15));
    border: 1px solid rgba(192,132,252,0.35);
    border-radius: 14px;
    margin-bottom: 12px;
  }

  .project-dot {
    width: 10px; height: 10px;
    border-radius: 50%;
    background: #4ade80;
    box-shadow: 0 0 8px #4ade80;
    animation: dot-pulse 2s ease-in-out infinite;
    flex-shrink: 0;
  }

  @keyframes dot-pulse {
    0%, 100% { opacity: 1; box-shadow: 0 0 8px #4ade80; }
    50% { opacity: 0.5; box-shadow: 0 0 20px #4ade80; }
  }

  .project-name {
    font-size: 1rem;
    font-weight: 600;
    color: #e9d5ff;
  }

  .project-sub {
    font-size: 0.78rem;
    color: var(--text-muted);
    margin-top: 2px;
  }

  .learning-list {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    margin-top: 12px;
  }

  .learn-chip {
    padding: 4px 12px;
    background: rgba(244,114,182,0.1);
    border: 1px dashed rgba(244,114,182,0.45);
    border-radius: 99px;
    font-size: 0.78rem;
    color: #fbcfe8;
    font-family: 'Fira Code', monospace;
  }

  /* ── GOALS ──────────────────────────────────── */
  .goal-row {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 10px 14px;
    border-radius: 10px;
    background: rgba(61,90,241,0.1);
    border-left: 3px solid #60a5fa;
    font-size: 0.88rem;
    color: #bae6fd;
  }

  /* ── CONTACT ─────────────────────────────────── */
  .contact-row {
    display: flex;
    align-items: center;
    gap: 14px;
  }

  .contact-link {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    background: linear-gradient(135deg, rgba(155,89,182,0.3), rgba(233,30,140,0.2));
    border: 1px solid rgba(192,132,252,0.45);
    border-radius: 12px;
    color: #e9d5ff;
    text-decoration: none;
    font-size: 0.88rem;
    font-weight: 500;
    transition: all 0.25s ease;
  }

  .contact-link:hover {
    background: linear-gradient(135deg, rgba(155,89,182,0.5), rgba(233,30,140,0.35));
    border-color: #c084fc;
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(155,89,182,0.3);
  }

  /* ── STATS ───────────────────────────────────── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
  }

  @media (max-width: 480px) {
    .stats-grid { grid-template-columns: 1fr; }
  }

  .stat-img {
    width: 100%;
    border-radius: 12px;
    border: 1px solid rgba(155,89,182,0.3);
    transition: transform 0.3s ease;
  }

  .stat-img:hover { transform: scale(1.02); }

  /* ── DIVIDER ─────────────────────────────────── */
  .gradient-divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, rgba(155,89,182,0.6), rgba(233,30,140,0.6), rgba(61,90,241,0.6), transparent);
    margin: 24px 0;
  }

  /* ── FOOTER ──────────────────────────────────── */
  .footer-note {
    text-align: center;
    font-size: 0.75rem;
    color: rgba(167,139,202,0.5);
    font-family: 'Fira Code', monospace;
    padding: 8px 0 24px;
  }

  /* ── COPY BUTTON ─────────────────────────────── */
  .copy-section {
    background: var(--bg-card2);
    border: 1px solid rgba(155,89,182,0.3);
    border-radius: 18px;
    padding: 24px 28px;
    margin-top: 32px;
  }

  .copy-title {
    font-size: 0.78rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: #c084fc;
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .copy-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, rgba(155,89,182,0.5), transparent);
  }

  .markdown-code {
    background: #080812;
    border: 1px solid rgba(155,89,182,0.25);
    border-radius: 12px;
    padding: 20px;
    font-family: 'Fira Code', monospace;
    font-size: 0.8rem;
    color: #a78bca;
    white-space: pre;
    overflow-x: auto;
    line-height: 1.7;
  }

  .copy-btn {
    margin-top: 16px;
    padding: 10px 28px;
    background: linear-gradient(135deg, #9b59b6, #e91e8c);
    border: none;
    border-radius: 10px;
    color: white;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 0.88rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.25s ease;
  }

  .copy-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 24px rgba(155,89,182,0.5);
  }

  .copy-btn:active { transform: translateY(0); }
</style>
</head>
<body>

<div class="container">

  <!-- ── PREVIEW LABEL ── -->
  <p style="text-align:center; font-size:0.75rem; letter-spacing:3px; text-transform:uppercase; color:rgba(167,139,202,0.5); font-family:'Fira Code',monospace; margin-bottom:24px;">
    ✦ GITHUB README PREVIEW ✦
  </p>

  <!-- ── HERO ── -->
  <div class="hero">
    <div class="wave-emoji">👋</div>
    <h1 class="hero-name">Hi, I'm Nethmi</h1>
    <p class="hero-sub">SLIIT · IT Undergraduate · Year 3 · Semester 2</p>
    <div class="badge-row">
      <span class="badge badge-purple">💻 Software Engineer</span>
      <span class="badge badge-pink">🧪 QA Engineer</span>
      <span class="badge badge-blue">🎯 Intern Seeker</span>
    </div>
    <div class="typing-container">
      <span class="typing-prefix">const goal =</span>
      <span class="typing-text">"Land my first internship"</span>
    </div>
  </div>

  <!-- ── ABOUT + WORKING ── -->
  <div class="section-grid">

    <div class="card">
      <div class="card-title gradient-purple">👩‍💻 About Me</div>
      <ul class="about-list">
        <li><span class="icon">🔭</span> Building <strong style="color:#e9d5ff">CampusX</strong> — a full-stack campus platform</li>
        <li><span class="icon">🌱</span> Currently deepening skills in Spring Boot, React & QA Testing</li>
        <li><span class="icon">✨</span> I love clean code, pixel-perfect UIs, and breaking things before users do</li>
        <li><span class="icon">📍</span> Based in Sri Lanka</li>
      </ul>
    </div>

    <div class="card">
      <div class="card-title gradient-pink">🎯 Goals</div>
      <div class="goal-row" style="margin-bottom:10px;">
        <span>💼</span>
        <span>Secure an internship in <strong>Software Engineering</strong> or <strong>QA</strong></span>
      </div>
      <div class="goal-row" style="background:rgba(155,89,182,0.1); border-left-color:#c084fc; color:#e9d5ff;">
        <span>🚀</span>
        <span>Build production-ready projects that solve real problems</span>
      </div>
      <div style="margin-top: 14px;">
        <p style="font-size:0.78rem; color: var(--text-muted); margin-bottom: 8px; font-family:'Fira Code',monospace;">// currently learning</p>
        <div class="learning-list">
          <span class="learn-chip">Spring Boot</span>
          <span class="learn-chip">React</span>
          <span class="learn-chip">QA Testing</span>
        </div>
      </div>
    </div>

  </div>

  <!-- ── TECH STACK ── -->
  <div class="card-full">
    <div class="card-title gradient-blue">🛠️ Tech Stack</div>
    <div class="tech-grid">
      <span class="tech-chip">☕ Java</span>
      <span class="tech-chip pink">🌱 Spring Boot</span>
      <span class="tech-chip blue">⚛️ React</span>
      <span class="tech-chip blue">🌐 HTML</span>
      <span class="tech-chip pink">🎨 CSS</span>
      <span class="tech-chip blue">📜 JavaScript</span>
      <span class="tech-chip green">🐬 MySQL</span>
      <span class="tech-chip">🔧 Git</span>
      <span class="tech-chip green">🧪 QA Testing</span>
    </div>
  </div>

  <!-- ── CONTACT ── -->
  <div class="card-full">
    <div class="card-title gradient-purple">📫 Let's Connect</div>
    <div class="contact-row">
      <a class="contact-link" href="https://www.linkedin.com/in/nethmi-wasana-b86931386/" target="_blank">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        Nethmi Wasana · LinkedIn
      </a>
    </div>
  </div>

  <!-- ── GITHUB STATS ── -->
  <div class="card-full">
    <div class="card-title gradient-pink">📊 GitHub Stats</div>
    <div class="stats-grid">
      <img class="stat-img" src="https://github-readme-stats.vercel.app/api?username=Nethm1&show_icons=true&theme=radical&bg_color=0d0d1a&border_color=9b59b6&title_color=c084fc&text_color=e9d5ff&icon_color=f472b6&hide_border=false&count_private=true" alt="GitHub Stats">
      <img class="stat-img" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Nethm1&layout=compact&theme=radical&bg_color=0d0d1a&border_color=9b59b6&title_color=c084fc&text_color=e9d5ff&hide_border=false" alt="Top Languages">
      <img class="stat-img" src="https://github-readme-streak-stats.herokuapp.com/?user=Nethm1&theme=radical&background=0d0d1a&border=9b59b6&ring=c084fc&fire=f472b6&currStreakLabel=c084fc" alt="GitHub Streak">
    </div>
  </div>

  <div class="gradient-divider"></div>

  <p class="footer-note">✦ open to internship opportunities · sri lanka & remote ✦</p>

  <!-- ── COPY MARKDOWN ── -->
  <div class="copy-section">
    <div class="copy-title">📋 Copy this to your README.md</div>
    <div class="markdown-code" id="readme-md">
<div style="align:center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=800&color=C084FC&center=true&vCenter=true&width=600&lines=Hi+%F0%9F%91%8B+I'm+Nethmi;SLIIT+IT+Undergraduate;Aspiring+Software+%26+QA+Engineer;Open+to+Internship+Opportunities!" alt="Typing SVG" />

</div>

---

<div align="center">
  <img src="https://img.shields.io/badge/SLIIT-Year%203%20%7C%20Semester%202-9b59b6?style=for-the-badge&logo=graduation-cap&logoColor=white" />
  <img src="https://img.shields.io/badge/Focus-Software%20%26%20QA%20Engineering-e91e8c?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Open%20to%20Internships-3d5af1?style=for-the-badge" />
</div>

---

## 👩‍💻 About Me

- 🔭 Currently building **CampusX** — a full-stack campus management platform  
- 🌱 Deepening skills in **Spring Boot**, **React**, and **QA Testing**  
- 🎯 Goal: Internship in **Software Engineering** or **QA**  
- ✨ I love clean code, pixel-perfect UIs, and finding bugs before users do  
- 📍 Based in **Sri Lanka**

---

## 🛠️ Tech Stack

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 🚀 Featured Project

### CampusX
> A full-stack campus platform built with **Java Spring Boot** + **React** + **MySQL**  
> *Developed as part of SLIIT Year 3 coursework*

---

## 📊 GitHub Stats

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Nethm1&show_icons=true&theme=radical&bg_color=0d0d1a&border_color=9b59b6&title_color=c084fc&text_color=e9d5ff&icon_color=f472b6&count_private=true" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Nethm1&layout=compact&theme=radical&bg_color=0d0d1a&border_color=9b59b6&title_color=c084fc&text_color=e9d5ff" />
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Nethm1&theme=radical&background=0d0d1a&border=9b59b6&ring=c084fc&fire=f472b6&currStreakLabel=c084fc" />
</div>

---

## 📫 Connect With Me

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Nethmi%20Wasana-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nethmi-wasana-b86931386/)

</div>

---

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=Nethm1&color=9b59b6&style=for-the-badge&label=Profile+Views" />
</div>

<div align="center">

*✦ Open to internship opportunities in Sri Lanka & Remote ✦*

</div></div>
    <button class="copy-btn" onclick="copyReadme()">📋 Copy Markdown</button>
    <p id="copy-msg" style="color:#4ade80; font-size:0.8rem; margin-top:8px; font-family:'Fira Code',monospace; display:none;">✓ Copied to clipboard!</p>
  </div>

</div>

<script>
function copyReadme() {
  const md = `<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=800&color=C084FC&center=true&vCenter=true&width=600&lines=Hi+%F0%9F%91%8B+I'm+Nethmi;SLIIT+IT+Undergraduate;Aspiring+Software+%26+QA+Engineer;Open+to+Internship+Opportunities!" alt="Typing SVG" />

</div>

---

<div align="center">
  <img src="https://img.shields.io/badge/SLIIT-Year%203%20%7C%20Semester%202-9b59b6?style=for-the-badge&logo=graduation-cap&logoColor=white" />
  <img src="https://img.shields.io/badge/Focus-Software%20%26%20QA%20Engineering-e91e8c?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Open%20to%20Internships-3d5af1?style=for-the-badge" />
</div>

---

## 👩‍💻 About Me

- 🔭 Currently building **CampusX** — a full-stack campus management platform  
- 🌱 Deepening skills in **Spring Boot**, **React**, and **QA Testing**  
- 🎯 Goal: Internship in **Software Engineering** or **QA**  
- ✨ I love clean code, pixel-perfect UIs, and finding bugs before users do  
- 📍 Based in **Sri Lanka**

---

## 🛠️ Tech Stack

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 🚀 Featured Project

### CampusX
> A full-stack campus platform built with **Java Spring Boot** + **React** + **MySQL**  
> *Developed as part of SLIIT Year 3 coursework*

---

## 📊 GitHub Stats

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Nethm1&show_icons=true&theme=radical&bg_color=0d0d1a&border_color=9b59b6&title_color=c084fc&text_color=e9d5ff&icon_color=f472b6&count_private=true" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Nethm1&layout=compact&theme=radical&bg_color=0d0d1a&border_color=9b59b6&title_color=c084fc&text_color=e9d5ff" />
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Nethm1&theme=radical&background=0d0d1a&border=9b59b6&ring=c084fc&fire=f472b6&currStreakLabel=c084fc" />
</div>

---

## 📫 Connect With Me

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Nethmi%20Wasana-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nethmi-wasana-b86931386/)

</div>

---

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=Nethm1&color=9b59b6&style=for-the-badge&label=Profile+Views" />
</div>

<div align="center">

*✦ Open to internship opportunities in Sri Lanka & Remote ✦*

</div>`;

  navigator.clipboard.writeText(md).then(() => {
    document.getElementById('copy-msg').style.display = 'block';
    setTimeout(() => document.getElementById('copy-msg').style.display = 'none', 3000);
  });
}
</script>
</body>
</html>
