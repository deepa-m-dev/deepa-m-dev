<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Deepa M — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Instrument+Serif:ital@0;1&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet"/>
<style>
  :root {
    --ink:    #0d0d0f;
    --paper:  #f7f5f0;
    --cream:  #ede9e1;
    --rust:   #c8512a;
    --rust2:  #e8734a;
    --sage:   #4a6650;
    --slate:  #2c3e50;
    --mid:    #7a7670;
    --border: rgba(13,13,15,0.10);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--paper);
    color: var(--ink);
    font-family: 'Space Grotesk', sans-serif;
    font-size: 16px;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  /* ─── LAYOUT ─────────────────────────────────── */
  .page { max-width: 860px; margin: 0 auto; padding: 0 24px; }

  /* ─── NAV ────────────────────────────────────── */
  nav {
    position: sticky; top: 0; z-index: 100;
    background: rgba(247,245,240,0.88);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 14px 0;
  }
  nav .page {
    display: flex; align-items: center; justify-content: space-between;
  }
  .nav-logo {
    font-family: 'Instrument Serif', serif;
    font-size: 1.1rem; letter-spacing: 0.02em;
  }
  .nav-links { display: flex; gap: 28px; }
  .nav-links a {
    font-size: 0.8rem; font-weight: 500; letter-spacing: 0.06em;
    text-transform: uppercase; color: var(--mid);
    text-decoration: none; transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--rust); }

  /* ─── HERO ───────────────────────────────────── */
  .hero {
    padding: 96px 0 72px;
    border-bottom: 1px solid var(--border);
  }
  .hero-eyebrow {
    display: inline-flex; align-items: center; gap: 10px;
    font-size: 0.72rem; font-weight: 600; letter-spacing: 0.12em;
    text-transform: uppercase; color: var(--rust);
    margin-bottom: 28px;
  }
  .hero-eyebrow::before {
    content: ''; display: block;
    width: 28px; height: 2px; background: var(--rust);
  }
  .hero h1 {
    font-family: 'Instrument Serif', serif;
    font-size: clamp(2.8rem, 7vw, 5rem);
    line-height: 1.08;
    letter-spacing: -0.02em;
    margin-bottom: 20px;
  }
  .hero h1 em {
    font-style: italic; color: var(--rust);
  }
  .hero-sub {
    font-size: 1.1rem; color: var(--mid);
    max-width: 520px; margin-bottom: 40px;
    font-weight: 400; line-height: 1.7;
  }
  .hero-chips { display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 48px; }
  .chip {
    font-size: 0.75rem; font-weight: 500; letter-spacing: 0.04em;
    padding: 6px 14px; border-radius: 100px;
    border: 1.5px solid var(--border); color: var(--slate);
    background: var(--cream);
  }
  .hero-cta { display: flex; gap: 14px; flex-wrap: wrap; }
  .btn {
    display: inline-flex; align-items: center; gap: 8px;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 0.82rem; font-weight: 600; letter-spacing: 0.04em;
    text-transform: uppercase; text-decoration: none;
    padding: 13px 26px; border-radius: 6px;
    border: 1.5px solid transparent; cursor: pointer;
    transition: all 0.2s;
  }
  .btn-primary {
    background: var(--ink); color: var(--paper);
    border-color: var(--ink);
  }
  .btn-primary:hover { background: var(--rust); border-color: var(--rust); }
  .btn-ghost {
    background: transparent; color: var(--ink);
    border-color: var(--border);
  }
  .btn-ghost:hover { border-color: var(--ink); }

  /* ─── SECTION BASE ───────────────────────────── */
  section { padding: 72px 0; border-bottom: 1px solid var(--border); }
  .section-label {
    font-size: 0.7rem; font-weight: 600; letter-spacing: 0.14em;
    text-transform: uppercase; color: var(--mid);
    margin-bottom: 40px;
    display: flex; align-items: center; gap: 14px;
  }
  .section-label::after {
    content: ''; flex: 1; height: 1px; background: var(--border);
  }
  h2 {
    font-family: 'Instrument Serif', serif;
    font-size: clamp(1.8rem, 4vw, 2.6rem);
    line-height: 1.15; letter-spacing: -0.01em;
  }

  /* ─── ABOUT ──────────────────────────────────── */
  .about-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 48px;
    margin-top: 40px;
  }
  .about-text { font-size: 1rem; color: var(--mid); line-height: 1.8; }
  .about-text p + p { margin-top: 16px; }
  .about-hobbies { margin-top: 28px; }
  .hobby-tag {
    display: inline-block; margin: 4px 4px 0 0;
    font-size: 0.78rem; padding: 5px 12px;
    background: var(--cream); border-radius: 4px;
    color: var(--sage); font-weight: 500;
    border: 1px solid rgba(74,102,80,0.2);
  }
  .about-stats { display: flex; flex-direction: column; gap: 0; }
  .stat-item {
    padding: 28px 0; border-bottom: 1px solid var(--border);
  }
  .stat-item:last-child { border-bottom: none; }
  .stat-number {
    font-family: 'Instrument Serif', serif;
    font-size: 3.2rem; line-height: 1;
    color: var(--ink); letter-spacing: -0.03em;
  }
  .stat-number span { font-size: 1.6rem; color: var(--rust); }
  .stat-label {
    font-size: 0.78rem; font-weight: 500; color: var(--mid);
    letter-spacing: 0.05em; text-transform: uppercase; margin-top: 6px;
  }

  /* ─── SKILLS ─────────────────────────────────── */
  .skills-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2px; margin-top: 40px;
    border: 1px solid var(--border); border-radius: 10px;
    overflow: hidden;
  }
  .skill-group {
    padding: 28px 24px; background: var(--paper);
    border: 1px solid var(--border);
    transition: background 0.2s;
  }
  .skill-group:hover { background: var(--cream); }
  .skill-group-title {
    font-size: 0.68rem; font-weight: 700; letter-spacing: 0.14em;
    text-transform: uppercase; color: var(--rust);
    margin-bottom: 16px;
  }
  .skill-list {
    display: flex; flex-wrap: wrap; gap: 6px; list-style: none;
  }
  .skill-list li {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.76rem; font-weight: 400; color: var(--slate);
    background: rgba(13,13,15,0.04); padding: 4px 10px; border-radius: 4px;
  }

  /* ─── FEATURED PROJECT ───────────────────────── */
  .project-card {
    margin-top: 40px;
    border: 1.5px solid var(--border); border-radius: 12px;
    overflow: hidden;
  }
  .project-header {
    background: var(--ink); padding: 40px 40px 32px;
    position: relative; overflow: hidden;
  }
  .project-header::before {
    content: 'FEATURED';
    position: absolute; top: 20px; right: 24px;
    font-size: 0.62rem; font-weight: 700; letter-spacing: 0.16em;
    color: var(--rust2); opacity: 0.7;
  }
  .project-badge {
    display: inline-block; background: var(--rust);
    color: white; font-size: 0.66rem; font-weight: 700;
    letter-spacing: 0.1em; text-transform: uppercase;
    padding: 5px 12px; border-radius: 4px; margin-bottom: 20px;
  }
  .project-header h3 {
    font-family: 'Instrument Serif', serif;
    font-size: 1.9rem; color: var(--paper);
    line-height: 1.2; margin-bottom: 14px;
  }
  .project-desc {
    font-size: 0.92rem; color: rgba(247,245,240,0.6);
    line-height: 1.7; max-width: 540px;
  }
  .project-body { padding: 32px 40px; background: var(--cream); }
  .project-features {
    display: grid; grid-template-columns: 1fr 1fr; gap: 12px;
    margin-bottom: 28px;
  }
  .feature-item {
    display: flex; align-items: flex-start; gap: 10px;
    font-size: 0.88rem; color: var(--slate);
  }
  .feature-item::before {
    content: '→'; color: var(--rust); font-weight: 700;
    flex-shrink: 0; margin-top: 2px;
  }
  .project-tech {
    display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 28px;
  }
  .tech-tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem; padding: 4px 10px;
    background: rgba(200,81,42,0.1); color: var(--rust);
    border-radius: 4px; border: 1px solid rgba(200,81,42,0.2);
  }
  .project-links { display: flex; gap: 12px; }

  /* ─── LEARNING ───────────────────────────────── */
  .learning-list {
    margin-top: 40px;
    display: grid; grid-template-columns: 1fr 1fr; gap: 0;
    border: 1px solid var(--border); border-radius: 10px; overflow: hidden;
  }
  .learn-item {
    display: flex; align-items: center; justify-content: space-between;
    padding: 22px 28px; border-bottom: 1px solid var(--border);
    background: var(--paper); transition: background 0.2s;
  }
  .learn-item:hover { background: var(--cream); }
  .learn-item:nth-child(odd) { border-right: 1px solid var(--border); }
  .learn-name { font-size: 0.95rem; font-weight: 500; color: var(--slate); }
  .learn-status {
    font-size: 0.68rem; font-weight: 600; letter-spacing: 0.08em;
    text-transform: uppercase; color: var(--sage);
    background: rgba(74,102,80,0.1); padding: 4px 10px; border-radius: 100px;
  }

  /* ─── GOALS ──────────────────────────────────── */
  .goals-list { margin-top: 40px; }
  .goal-item {
    display: flex; align-items: flex-start; gap: 24px;
    padding: 28px 0; border-bottom: 1px solid var(--border);
  }
  .goal-item:last-child { border-bottom: none; }
  .goal-num {
    font-family: 'Instrument Serif', serif; font-size: 2.2rem;
    color: var(--cream); font-style: italic;
    flex-shrink: 0; width: 48px; line-height: 1;
    margin-top: 2px;
    text-shadow: 0 0 0 1px var(--border);
    -webkit-text-stroke: 1.5px var(--border);
    color: transparent;
  }
  .goal-content h4 {
    font-size: 1.05rem; font-weight: 600; margin-bottom: 6px;
  }
  .goal-content p { font-size: 0.88rem; color: var(--mid); line-height: 1.6; }

  /* ─── CONNECT ────────────────────────────────── */
  .connect-section {
    padding: 72px 0 80px; text-align: center;
  }
  .connect-section h2 { margin-bottom: 16px; }
  .connect-section p { color: var(--mid); margin-bottom: 36px; font-size: 1.05rem; }
  .connect-links {
    display: flex; gap: 14px; justify-content: center; flex-wrap: wrap;
  }

  /* ─── FOOTER ─────────────────────────────────── */
  footer {
    padding: 24px 0; border-top: 1px solid var(--border);
    text-align: center;
  }
  footer p {
    font-size: 0.78rem; color: var(--mid); letter-spacing: 0.03em;
  }
  footer span { color: var(--rust); }

  /* ─── ANIMATIONS ─────────────────────────────── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .hero > * { animation: fadeUp 0.6s ease both; }
  .hero-eyebrow { animation-delay: 0.05s; }
  .hero h1     { animation-delay: 0.12s; }
  .hero-sub    { animation-delay: 0.18s; }
  .hero-chips  { animation-delay: 0.24s; }
  .hero-cta    { animation-delay: 0.30s; }

  /* ─── RESPONSIVE ─────────────────────────────── */
  @media (max-width: 640px) {
    .about-grid { grid-template-columns: 1fr; }
    .project-features { grid-template-columns: 1fr; }
    .learning-list { grid-template-columns: 1fr; }
    .learn-item:nth-child(odd) { border-right: none; }
    .project-header { padding: 28px 24px 22px; }
    .project-body { padding: 24px; }
    nav .nav-links { display: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="page">
    <div class="nav-logo">Deepa M</div>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Work</a>
      <a href="#connect">Connect</a>
    </div>
  </div>
</nav>

<!-- HERO -->
<div class="page">
<section class="hero">
  <div class="hero-eyebrow">BCA Graduate · Aspiring Developer</div>
  <h1>Building <em>intelligent</em><br>software that matters.</h1>
  <p class="hero-sub">
    I'm Deepa — a Python developer and AI enthusiast who loves turning complex ideas into clean, working systems. Currently exploring the intersection of machine learning and real-world product development.
  </p>
  <div class="hero-chips">
    <span class="chip">Python</span>
    <span class="chip">Machine Learning</span>
    <span class="chip">Flask</span>
    <span class="chip">React</span>
    <span class="chip">Data Science</span>
    <span class="chip">Full Stack</span>
  </div>
  <div class="hero-cta">
    <a href="#projects" class="btn btn-primary">View Featured Work →</a>
    <a href="#connect" class="btn btn-ghost">Get in Touch</a>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">About Me</div>
  <h2>Code, curiosity,<br>and a little creativity.</h2>
  <div class="about-grid">
    <div>
      <div class="about-text">
        <p>I graduated with a Bachelor of Computer Applications and have since been obsessed with how artificial intelligence can change the way software is built and used.</p>
        <p>My work sits at the intersection of backend engineering, data science, and product thinking — I like understanding <em>why</em> something works, not just that it does.</p>
        <p>Outside of code, I recharge through realistic portrait drawing, painting, and writing poetry — creative disciplines that sharpen the same logical-intuitive balance I bring to problem solving.</p>
      </div>
      <div class="about-hobbies">
        <span class="hobby-tag">🎨 Realistic Drawing</span>
        <span class="hobby-tag">🖼 Portrait Art</span>
        <span class="hobby-tag">🎤 Public Speaking</span>
        <span class="hobby-tag">✍️ Poetry</span>
        <span class="hobby-tag">🧠 DSA</span>
      </div>
    </div>
    <div class="about-stats">
      <div class="stat-item">
        <div class="stat-number">7<span>+</span></div>
        <div class="stat-label">Languages & Frameworks</div>
      </div>
      <div class="stat-item">
        <div class="stat-number">3<span>+</span></div>
        <div class="stat-label">AI / ML Projects Shipped</div>
      </div>
      <div class="stat-item">
        <div class="stat-number">∞</div>
        <div class="stat-label">Problems Left to Solve</div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-label">Tech Stack</div>
  <h2>Tools I reach for<br>when the problem is real.</h2>
  <div class="skills-grid">
    <div class="skill-group">
      <div class="skill-group-title">Languages</div>
      <ul class="skill-list">
        <li>Python</li><li>Java</li><li>JavaScript</li>
        <li>PHP</li><li>C</li><li>C++</li><li>SQL</li>
      </ul>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Web & Frontend</div>
      <ul class="skill-list">
        <li>React</li><li>HTML5</li><li>CSS3</li><li>Bootstrap</li>
      </ul>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Backend & APIs</div>
      <ul class="skill-list">
        <li>Flask</li><li>Spring Boot</li>
      </ul>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">AI / Data Science</div>
      <ul class="skill-list">
        <li>Scikit-Learn</li><li>XGBoost</li><li>Pandas</li>
        <li>NumPy</li><li>Matplotlib</li>
      </ul>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Databases</div>
      <ul class="skill-list">
        <li>MySQL</li><li>SQLite</li><li>RDBMS</li>
      </ul>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Tools & Platforms</div>
      <ul class="skill-list">
        <li>Git</li><li>GitHub</li><li>Linux</li>
      </ul>
    </div>
  </div>
</section>

<!-- PROJECT -->
<section id="projects">
  <div class="section-label">Featured Project</div>
  <h2>Where theory<br>meets deployment.</h2>
  <div class="project-card">
    <div class="project-header">
      <div class="project-badge">AI · ML · Flask</div>
      <h3>AI Hiring &amp; Recruitment<br>Intelligence System</h3>
      <p class="project-desc">An end-to-end recruitment platform that uses machine learning to predict candidate suitability — removing guesswork and bias from the hiring pipeline.</p>
    </div>
    <div class="project-body">
      <div class="project-features">
        <div class="feature-item">Candidate suitability prediction via XGBoost</div>
        <div class="feature-item">ML pipeline with feature engineering</div>
        <div class="feature-item">Interactive analytics dashboard</div>
        <div class="feature-item">Data preprocessing at scale</div>
        <div class="feature-item">Web-based deployment on Render</div>
        <div class="feature-item">Clean, interview-ready codebase</div>
      </div>
      <div class="project-tech">
        <span class="tech-tag">Python</span>
        <span class="tech-tag">Flask</span>
        <span class="tech-tag">XGBoost</span>
        <span class="tech-tag">Scikit-Learn</span>
        <span class="tech-tag">Pandas</span>
        <span class="tech-tag">NumPy</span>
        <span class="tech-tag">SQLite</span>
        <span class="tech-tag">Bootstrap</span>
      </div>
      <div class="project-links">
        <a href="https://ai-hiring-system-aowd.onrender.com/" target="_blank" class="btn btn-primary">Live Demo →</a>
        <a href="https://github.com/YOUR_USERNAME" target="_blank" class="btn btn-ghost">View Source</a>
      </div>
    </div>
  </div>
</section>

<!-- LEARNING -->
<section id="learning">
  <div class="section-label">Currently Learning</div>
  <h2>What's on the workbench.</h2>
  <div class="learning-list">
    <div class="learn-item">
      <span class="learn-name">Advanced DSA</span>
      <span class="learn-status">Active</span>
    </div>
    <div class="learn-item">
      <span class="learn-name">Machine Learning</span>
      <span class="learn-status">Active</span>
    </div>
    <div class="learn-item">
      <span class="learn-name">Artificial Intelligence</span>
      <span class="learn-status">Active</span>
    </div>
    <div class="learn-item">
      <span class="learn-name">System Design</span>
      <span class="learn-status">Active</span>
    </div>
    <div class="learn-item">
      <span class="learn-name">Full Stack Development</span>
      <span class="learn-status">Active</span>
    </div>
    <div class="learn-item">
      <span class="learn-name">Deep Learning</span>
      <span class="learn-status">Next</span>
    </div>
  </div>
</section>

<!-- GOALS -->
<section id="goals">
  <div class="section-label">Career Goals</div>
  <h2>Where I'm headed.</h2>
  <div class="goals-list">
    <div class="goal-item">
      <div class="goal-num">01</div>
      <div class="goal-content">
        <h4>Land a Software or Python Development Role</h4>
        <p>Join a team working on products that make a real difference, where I can grow fast and contribute from day one.</p>
      </div>
    </div>
    <div class="goal-item">
      <div class="goal-num">02</div>
      <div class="goal-content">
        <h4>Deepen AI, ML, and Data Science Expertise</h4>
        <p>Move from applying existing models to designing and improving them — understanding the theory behind the results.</p>
      </div>
    </div>
    <div class="goal-item">
      <div class="goal-num">03</div>
      <div class="goal-content">
        <h4>Contribute to Impactful Real-World Projects</h4>
        <p>Build systems that solve meaningful problems — in healthcare, education, hiring, or anywhere AI can genuinely help.</p>
      </div>
    </div>
    <div class="goal-item">
      <div class="goal-num">04</div>
      <div class="goal-content">
        <h4>Keep Getting Better at the Fundamentals</h4>
        <p>Strong algorithms, clean architecture, and clear communication — the skills that compound over an entire career.</p>
      </div>
    </div>
  </div>
</section>

<!-- CONNECT -->
<section id="connect" class="connect-section" style="border-bottom: none;">
  <div class="section-label" style="justify-content: center; text-align: center; margin-bottom: 24px;">Let's Talk</div>
  <h2>Open to opportunities.</h2>
  <p>Whether it's a role, a collaborat