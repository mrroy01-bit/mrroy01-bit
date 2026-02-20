<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ritik Kumar — GitHub README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Mono:ital,wght@0,300;0,400;0,500;1,300&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0a0c0f;
    --surface: #111418;
    --border: #1e2329;
    --border-bright: #2d333b;
    --text: #cdd9e5;
    --muted: #768390;
    --accent: #58a6ff;
    --accent2: #3fb950;
    --accent3: #e3b341;
    --accent4: #ff7b72;
    --white: #f0f6fc;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Mono', monospace;
    font-size: 14px;
    line-height: 1.7;
    min-height: 100vh;
    padding: 48px 24px;
  }

  .readme {
    max-width: 860px;
    margin: 0 auto;
  }

  /* ── HEADER ── */
  .header {
    border: 1px solid var(--border-bright);
    border-radius: 12px;
    padding: 48px;
    margin-bottom: 24px;
    position: relative;
    overflow: hidden;
    background: var(--surface);
  }
  .header::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 80% 60% at 70% 50%, rgba(88,166,255,0.06) 0%, transparent 70%);
    pointer-events: none;
  }
  .header-grid {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 32px;
    align-items: start;
    position: relative;
  }
  .greeting {
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 12px;
  }
  .name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(32px, 5vw, 52px);
    font-weight: 800;
    color: var(--white);
    line-height: 1.05;
    letter-spacing: -0.02em;
    margin-bottom: 8px;
  }
  .title {
    font-family: 'Syne', sans-serif;
    font-size: 18px;
    font-weight: 400;
    color: var(--muted);
    margin-bottom: 20px;
  }
  .tagline {
    font-size: 13px;
    color: var(--muted);
    max-width: 460px;
    line-height: 1.6;
    font-style: italic;
  }
  .status-pill {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: rgba(63,185,80,0.1);
    border: 1px solid rgba(63,185,80,0.25);
    color: var(--accent2);
    font-size: 11px;
    padding: 4px 12px;
    border-radius: 100px;
    margin-top: 20px;
    font-family: 'DM Mono', monospace;
  }
  .status-dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--accent2);
    animation: pulse 2s infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }
  .avatar-placeholder {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background: linear-gradient(135deg, #1f3a5e, #0d2137);
    border: 2px solid var(--border-bright);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Syne', sans-serif;
    font-size: 32px;
    font-weight: 800;
    color: var(--accent);
  }

  /* ── BADGES ── */
  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 24px;
  }
  .badge {
    font-size: 11px;
    font-family: 'DM Mono', monospace;
    padding: 4px 10px;
    border-radius: 6px;
    border: 1px solid var(--border-bright);
    color: var(--muted);
    background: var(--bg);
  }

  /* ── SECTION HEADERS ── */
  .section {
    margin-bottom: 24px;
  }
  .section-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 16px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
  }
  .section-num {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--accent);
    opacity: 0.6;
    letter-spacing: 0.1em;
  }
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 16px;
    font-weight: 700;
    color: var(--white);
    letter-spacing: -0.01em;
  }
  .section-rule {
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, var(--border-bright), transparent);
  }

  /* ── CARDS ── */
  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px 24px;
    transition: border-color 0.2s;
  }
  .card:hover { border-color: var(--border-bright); }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }
  .about-item {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    font-size: 13px;
    color: var(--text);
    line-height: 1.5;
  }
  .about-icon {
    color: var(--accent);
    font-size: 14px;
    flex-shrink: 0;
    margin-top: 1px;
  }

  /* ── TECH STACK ── */
  .stack-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
  }
  .stack-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px;
  }
  .stack-label {
    font-family: 'Syne', sans-serif;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .stack-label-dot {
    width: 8px;
    height: 8px;
    border-radius: 2px;
    flex-shrink: 0;
  }
  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }
  .tag {
    font-size: 11.5px;
    padding: 3px 9px;
    border-radius: 5px;
    border: 1px solid var(--border-bright);
    color: var(--text);
    background: var(--bg);
    font-family: 'DM Mono', monospace;
  }

  /* ── PROJECTS ── */
  .project-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 22px;
    position: relative;
    overflow: hidden;
  }
  .project-card::after {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px;
    height: 100%;
    border-radius: 10px 0 0 10px;
  }
  .project-card.blue::after { background: var(--accent); }
  .project-card.green::after { background: var(--accent2); }
  .project-card.yellow::after { background: var(--accent3); }
  .project-card.red::after { background: var(--accent4); }
  .project-title {
    font-family: 'Syne', sans-serif;
    font-size: 14px;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 6px;
  }
  .project-desc {
    font-size: 12px;
    color: var(--muted);
    margin-bottom: 14px;
    line-height: 1.6;
  }
  .project-stat {
    font-size: 11px;
    color: var(--accent2);
    font-family: 'DM Mono', monospace;
  }

  /* ── METRICS ── */
  .metrics {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
    margin-bottom: 12px;
  }
  .metric-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px;
    text-align: center;
  }
  .metric-val {
    font-family: 'Syne', sans-serif;
    font-size: 28px;
    font-weight: 800;
    color: var(--white);
    line-height: 1;
    margin-bottom: 4px;
  }
  .metric-val span {
    color: var(--accent);
  }
  .metric-label {
    font-size: 11px;
    color: var(--muted);
    font-family: 'DM Mono', monospace;
  }

  /* ── CONNECT ── */
  .connect-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
  }
  .connect-link {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px 20px;
    display: flex;
    align-items: center;
    gap: 10px;
    text-decoration: none;
    color: var(--text);
    font-size: 12px;
    font-family: 'DM Mono', monospace;
    transition: all 0.2s;
  }
  .connect-link:hover {
    border-color: var(--border-bright);
    color: var(--white);
  }
  .connect-icon {
    font-size: 16px;
  }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding: 32px;
    font-size: 12px;
    color: var(--muted);
    font-style: italic;
    border-top: 1px solid var(--border);
    margin-top: 12px;
  }

  /* ── CURRENTLY ── */
  .currently-list {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  .currently-item {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    font-size: 13px;
    color: var(--text);
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 14px 18px;
  }
  .currently-badge {
    font-size: 10px;
    padding: 2px 7px;
    border-radius: 4px;
    font-family: 'DM Mono', monospace;
    flex-shrink: 0;
    margin-top: 1px;
  }
  .badge-blue { background: rgba(88,166,255,0.12); color: var(--accent); border: 1px solid rgba(88,166,255,0.2); }
  .badge-green { background: rgba(63,185,80,0.12); color: var(--accent2); border: 1px solid rgba(63,185,80,0.2); }
  .badge-yellow { background: rgba(227,179,65,0.12); color: var(--accent3); border: 1px solid rgba(227,179,65,0.2); }

  @media (max-width: 640px) {
    .header-grid, .about-grid, .stack-grid, .project-grid, .metrics, .connect-grid { grid-template-columns: 1fr; }
    .metrics { grid-template-columns: repeat(2, 1fr); }
    .connect-grid { grid-template-columns: repeat(2, 1fr); }
    .avatar-placeholder { display: none; }
  }
</style>
</head>
<body>
<div class="readme">

  <!-- HEADER -->
  <div class="header">
    <div class="header-grid">
      <div>
        <div class="greeting">// Hello, World</div>
        <h1 class="name">Ritik Kumar</h1>
        <p class="title">Full Stack & Mobile Developer</p>
        <p class="tagline">Transforming ideas into robust digital solutions — React, Next.js, Node.js, Expo & MongoDB specialist.</p>
        <div class="status-pill"><span class="status-dot"></span> Open to opportunities</div>
        <div class="badges">
          <span class="badge">3+ years exp</span>
          <span class="badge">50+ projects</span>
          <span class="badge">10K+ app users</span>
          <span class="badge">React · Node.js · Expo · MongoDB</span>
        </div>
      </div>
      <div class="avatar-placeholder">RK</div>
    </div>
  </div>

  <!-- METRICS -->
  <div class="metrics">
    <div class="metric-card">
      <div class="metric-val">50<span>+</span></div>
      <div class="metric-label">projects shipped</div>
    </div>
    <div class="metric-card">
      <div class="metric-val">60<span>%</span></div>
      <div class="metric-label">perf. improvement</div>
    </div>
    <div class="metric-card">
      <div class="metric-val">10k<span>+</span></div>
      <div class="metric-label">active users</div>
    </div>
    <div class="metric-card">
      <div class="metric-val">20<span>+</span></div>
      <div class="metric-label">open source PRs</div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">01</span>
      <span class="section-title">About</span>
      <div class="section-rule"></div>
    </div>
    <div class="card">
      <div class="about-grid">
        <div class="about-item"><span class="about-icon">→</span> Building scalable web & mobile apps with modern architectures</div>
        <div class="about-item"><span class="about-icon">→</span> Cross-platform mobile apps with Expo & React Native</div>
        <div class="about-item"><span class="about-icon">→</span> Integrating AI/ML capabilities into production applications</div>
        <div class="about-item"><span class="about-icon">→</span> Cloud deployments on AWS & Firebase</div>
        <div class="about-item"><span class="about-icon">→</span> CI/CD pipelines, testing & DevOps automation</div>
        <div class="about-item"><span class="about-icon">→</span> Team lead for 5+ developer squads</div>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">02</span>
      <span class="section-title">Tech Stack</span>
      <div class="section-rule"></div>
    </div>
    <div class="stack-grid">
      <div class="stack-card">
        <div class="stack-label" style="color: #61dafb"><span class="stack-label-dot" style="background:#61dafb"></span>Frontend</div>
        <div class="tags">
          <span class="tag">React</span>
          <span class="tag">Next.js</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-label" style="color: #3fb950"><span class="stack-label-dot" style="background:#3fb950"></span>Backend</div>
        <div class="tags">
          <span class="tag">Node.js</span>
          <span class="tag">Express</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-label" style="color: #e3b341"><span class="stack-label-dot" style="background:#e3b341"></span>Mobile</div>
        <div class="tags">
          <span class="tag">Expo</span>
          <span class="tag">Expo Router</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-label" style="color: #ff7b72"><span class="stack-label-dot" style="background:#ff7b72"></span>Database & Cloud</div>
        <div class="tags">
          <span class="tag">MongoDB</span>
        </div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">03</span>
      <span class="section-title">Featured Projects</span>
      <div class="section-rule"></div>
    </div>
    <div class="project-grid">
      <div class="project-card blue">
        <div class="project-title">E-Commerce Platform</div>
        <div class="project-desc">Real-time inventory management with AI-powered product recommendations and Stripe integration.</div>
        <div class="tags" style="margin-bottom: 12px">
          <span class="tag">React</span><span class="tag">Node.js</span><span class="tag">MongoDB</span><span class="tag">Stripe</span>
        </div>
        <div class="project-stat">↑ 40% conversion rate · 5K+ daily users</div>
      </div>
      <div class="project-card green">
        <div class="project-title">Healthcare Management</div>
        <div class="project-desc">HIPAA-compliant patient portal with appointment scheduling and real-time doctor–patient communication.</div>
        <div class="tags" style="margin-bottom: 12px">
          <span class="tag">Next.js</span><span class="tag">TypeScript</span><span class="tag">PostgreSQL</span>
        </div>
        <div class="project-stat">↓ 30% wait time reduction</div>
      </div>
    </div>
  </div>

  <!-- CURRENTLY -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">04</span>
      <span class="section-title">Currently</span>
      <div class="section-rule"></div>
    </div>
    <div class="currently-list">
      <div class="currently-item">
        <span class="currently-badge badge-blue">building</span>
        Next.js 14 App Router + Server Components for enterprise-scale applications
      </div>
      <div class="currently-item">
        <span class="currently-badge badge-blue">building</span>
        AI-powered features with OpenAI API, Langchain & TensorFlow.js
      </div>
      <div class="currently-item">
        <span class="currently-badge badge-green">learning</span>
        Web3 & Solidity — smart contract development
      </div>
      <div class="currently-item">
        <span class="currently-badge badge-yellow">open to</span>
        Innovative startups · open-source collaboration · mentoring
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">05</span>
      <span class="section-title">Connect</span>
      <div class="section-rule"></div>
    </div>
    <div class="connect-grid">
      <a class="connect-link" href="/cdn-cgi/l/email-protection#3d4f544954565648505c4f0f050f087d5a505c5451135e5250">
        <span class="connect-icon">✉</span> <span class="__cf_email__" data-cfemail="d6a4bfa2bfbdbda3bbb7a4e4eee4e396b1bbb7bfbaf8b5b9bb">[email&#160;protected]</span>
      </a>
      <a class="connect-link" href="https://github.com/mrroy01-bit">
        <span class="connect-icon">⌥</span> github/mrroy01-bit
      </a>
      <a class="connect-link" href="https://linkedin.com/in/ritik-kumar-roy0211">
        <span class="connect-icon">↗</span> linkedin/ritik-kumar-roy0211
      </a>
    </div>
  </div>

  <div c
