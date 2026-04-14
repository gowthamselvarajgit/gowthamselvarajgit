<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Gowtham S — GitHub README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0d1117;
    --bg2: #161b22;
    --bg3: #21262d;
    --border: #30363d;
    --text: #e6edf3;
    --muted: #8b949e;
    --blue: #58a6ff;
    --green: #3fb950;
    --orange: #f0883e;
    --purple: #bc8cff;
    --cyan: #39d353;
    --red: #ff7b72;
    --yellow: #d29922;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* === HERO === */
  .hero {
    position: relative;
    padding: 70px 40px 50px;
    text-align: center;
    overflow: hidden;
    background: linear-gradient(180deg, #010409 0%, var(--bg) 100%);
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -60px; left: 50%; transform: translateX(-50%);
    width: 600px; height: 300px;
    background: radial-gradient(ellipse, rgba(88,166,255,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .particles {
    position: absolute; inset: 0; pointer-events: none;
    overflow: hidden;
  }
  .particle {
    position: absolute;
    width: 2px; height: 2px;
    border-radius: 50%;
    background: var(--blue);
    opacity: 0;
    animation: floatUp linear infinite;
  }
  @keyframes floatUp {
    0%   { opacity: 0; transform: translateY(0) scale(1); }
    10%  { opacity: 0.6; }
    90%  { opacity: 0.2; }
    100% { opacity: 0; transform: translateY(-200px) scale(0.5); }
  }
  .hero h1 {
    font-size: 64px;
    font-weight: 700;
    letter-spacing: -2px;
    background: linear-gradient(135deg, #58a6ff 0%, #a5d6ff 50%, #58a6ff 100%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: shimmer 4s ease-in-out infinite;
    background-size: 200% auto;
    margin-bottom: 10px;
  }
  @keyframes shimmer {
    0%   { background-position: 0% center; }
    50%  { background-position: 100% center; }
    100% { background-position: 0% center; }
  }
  .hero .subtitle {
    font-size: 16px;
    color: var(--muted);
    font-family: 'Fira Code', monospace;
    margin-bottom: 28px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.3s forwards;
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* Typing text */
  .typing-wrap {
    display: inline-block;
    height: 32px;
    overflow: hidden;
    margin-bottom: 28px;
  }
  .typing-line {
    display: block;
    font-family: 'Fira Code', monospace;
    font-size: 17px;
    color: var(--blue);
    font-weight: 500;
    opacity: 0;
    animation: slideIn 0.5s ease forwards;
    white-space: nowrap;
  }
  @keyframes slideIn {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* Badge row */
  .badge-row {
    display: flex; flex-wrap: wrap; justify-content: center; gap: 10px;
    margin-bottom: 16px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.6s forwards;
  }
  .badge {
    display: inline-flex; align-items: center; gap: 7px;
    padding: 7px 16px;
    border-radius: 6px;
    font-size: 13px;
    font-weight: 500;
    text-decoration: none;
    transition: all 0.2s ease;
    border: 1px solid transparent;
  }
  .badge:hover { transform: translateY(-2px); filter: brightness(1.15); }
  .badge svg { width: 16px; height: 16px; }
  .badge-blue   { background: #0f2848; color: #58a6ff; border-color: #1f4a8a; }
  .badge-red    { background: #300b0b; color: #ff7b72; border-color: #5c1a1a; }
  .badge-dark   { background: #161b22; color: #c9d1d9; border-color: #30363d; }
  .badge-green  { background: #0a2d1c; color: #3fb950; border-color: #155830; }
  .badge-orange { background: #2d1a06; color: #f0883e; border-color: #5c3610; }

  /* === CONTAINER === */
  .container { max-width: 860px; margin: 0 auto; padding: 0 24px 60px; }

  /* === SECTION === */
  .section {
    margin: 40px 0;
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .section.visible { opacity: 1; transform: translateY(0); }

  .section-title {
    display: flex; align-items: center; gap: 12px;
    font-size: 18px; font-weight: 600;
    color: var(--text);
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
    margin-bottom: 20px;
  }
  .section-title .icon { font-size: 20px; }

  /* === CODE BLOCK === */
  .code-block {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 10px;
    overflow: hidden;
  }
  .code-header {
    display: flex; align-items: center; gap: 8px;
    padding: 10px 16px;
    background: var(--bg3);
    border-bottom: 1px solid var(--border);
  }
  .dot { width: 12px; height: 12px; border-radius: 50%; }
  .dot-red { background: #ff5f57; }
  .dot-yellow { background: #febc2e; }
  .dot-green { background: #28c840; }
  .code-lang { font-family: 'Fira Code', monospace; font-size: 12px; color: var(--muted); margin-left: auto; }
  .code-body { padding: 20px 24px; font-family: 'Fira Code', monospace; font-size: 13.5px; line-height: 1.8; }
  .k  { color: var(--blue); }
  .s  { color: #a5d6ff; }
  .v  { color: var(--orange); }
  .c  { color: var(--muted); font-style: italic; }
  .p  { color: var(--text); }

  /* === SKILL GRID === */
  .skill-group { margin-bottom: 22px; }
  .skill-group-label {
    font-size: 12px; font-weight: 600; letter-spacing: 0.08em;
    color: var(--muted); text-transform: uppercase;
    margin-bottom: 10px;
  }
  .skill-pills { display: flex; flex-wrap: wrap; gap: 8px; }
  .pill {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 5px 13px;
    border-radius: 6px;
    font-size: 13px; font-weight: 500;
    border: 1px solid var(--border);
    background: var(--bg2);
    color: var(--text);
    transition: all 0.2s ease;
    cursor: default;
  }
  .pill:hover {
    border-color: var(--blue);
    color: var(--blue);
    background: rgba(88,166,255,0.06);
    transform: translateY(-1px);
  }
  .pill .dot2 { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }

  /* === EXP CARDS === */
  .exp-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  @media(max-width:620px){ .exp-grid { grid-template-columns: 1fr; } }
  .exp-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px 22px;
    transition: border-color 0.2s;
    position: relative; overflow: hidden;
  }
  .exp-card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0;
    height: 3px;
  }
  .exp-card.blue::before  { background: linear-gradient(90deg, var(--blue), transparent); }
  .exp-card.green::before { background: linear-gradient(90deg, var(--green), transparent); }
  .exp-card:hover { border-color: rgba(88,166,255,0.4); }
  .exp-card h3 { font-size: 15px; font-weight: 600; color: var(--text); margin-bottom: 2px; }
  .exp-card .role {
    font-family: 'Fira Code', monospace; font-size: 12px;
    color: var(--blue); margin-bottom: 4px;
  }
  .exp-card .date { font-size: 12px; color: var(--muted); margin-bottom: 14px; }
  .exp-card ul { list-style: none; padding: 0; }
  .exp-card ul li {
    font-size: 13px; color: var(--muted); padding: 3px 0; padding-left: 16px;
    position: relative;
  }
  .exp-card ul li::before { content: '▸'; position: absolute; left: 0; color: var(--blue); font-size: 10px; top: 5px; }

  /* === PROJECT CARDS === */
  .project-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  @media(max-width:620px){ .project-grid { grid-template-columns: 1fr; } }
  .project-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px 22px;
    transition: all 0.25s ease;
    cursor: pointer;
  }
  .project-card:hover {
    border-color: var(--blue);
    transform: translateY(-3px);
    box-shadow: 0 8px 30px rgba(88,166,255,0.1);
  }
  .project-card .proj-title {
    font-size: 15px; font-weight: 600; color: var(--blue);
    margin-bottom: 6px; display: flex; align-items: center; gap: 8px;
  }
  .project-card .proj-desc {
    font-size: 13px; color: var(--muted); margin-bottom: 14px; line-height: 1.6;
  }
  .tag-row { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 12px; }
  .tag {
    font-family: 'Fira Code', monospace;
    font-size: 11px; padding: 2px 8px;
    border-radius: 4px;
    background: rgba(88,166,255,0.1);
    color: var(--blue);
    border: 1px solid rgba(88,166,255,0.2);
  }
  .proj-bullet { font-size: 12px; color: var(--muted); padding-left: 14px; position: relative; margin: 3px 0; }
  .proj-bullet::before { content: '◆'; position: absolute; left: 0; color: var(--cyan); font-size: 8px; top: 4px; }

  /* === ACHIEVEMENT TABLE === */
  .ach-table { width: 100%; border-collapse: collapse; }
  .ach-table th {
    font-size: 12px; font-weight: 600; letter-spacing: 0.07em;
    text-transform: uppercase; color: var(--muted);
    padding: 8px 14px; text-align: left;
    border-bottom: 1px solid var(--border);
  }
  .ach-table td {
    padding: 12px 14px; font-size: 13.5px;
    border-bottom: 1px solid rgba(48,54,61,0.5);
    color: var(--text);
  }
  .ach-table tr:hover td { background: rgba(88,166,255,0.03); }
  .ach-medal { font-size: 18px; }

  /* === CERTS === */
  .cert-row { display: flex; flex-wrap: wrap; justify-content: center; gap: 12px; }
  .cert-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 18px 24px; text-align: center; min-width: 180px;
    transition: all 0.2s;
  }
  .cert-card:hover { border-color: var(--blue); transform: translateY(-2px); }
  .cert-card .cert-icon { font-size: 28px; margin-bottom: 8px; }
  .cert-card .cert-name { font-size: 13.5px; font-weight: 600; color: var(--text); }
  .cert-card .cert-by { font-size: 12px; color: var(--muted); margin-top: 3px; }

  /* === STATS GRID === */
  .stats-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; margin-bottom: 16px; }
  @media(max-width:500px){ .stats-grid { grid-template-columns: 1fr 1fr; } }
  .stat-card {
    background: var(--bg2); border: 1px solid var(--border);
    border-radius: 8px; padding: 16px 20px; text-align: center;
  }
  .stat-num { font-size: 28px; font-weight: 700; color: var(--blue); font-family: 'Fira Code', monospace; }
  .stat-label { font-size: 12px; color: var(--muted); margin-top: 4px; }

  /* === CONNECT === */
  .connect-row { display: flex; flex-wrap: wrap; justify-content: center; gap: 12px; }
  .connect-btn {
    display: flex; align-items: center; gap: 10px;
    padding: 12px 22px;
    border-radius: 8px;
    font-size: 14px; font-weight: 500;
    text-decoration: none; color: var(--text);
    background: var(--bg2); border: 1px solid var(--border);
    transition: all 0.2s;
  }
  .connect-btn:hover { border-color: var(--blue); color: var(--blue); transform: translateY(-2px); }
  .connect-btn .icon { font-size: 18px; }

  /* === FOOTER === */
  .footer {
    text-align: center; padding: 40px 20px 30px;
    border-top: 1px solid var(--border);
    margin-top: 40px;
  }
  .footer-typing {
    font-family: 'Fira Code', monospace; font-size: 14px; color: var(--muted);
    margin-bottom: 12px;
  }

  /* === DIVIDER === */
  hr.divider {
    border: none; border-top: 1px solid var(--border); margin: 40px 0;
  }

  /* Star count badge */
  .info-pills { display: flex; flex-wrap: wrap; justify-content: center; gap: 8px; margin-top: 16px; }
  .info-pill {
    font-size: 12px; padding: 4px 12px; border-radius: 20px;
    background: var(--bg3); color: var(--muted); border: 1px solid var(--border);
    display: flex; align-items: center; gap: 5px;
  }
  .info-pill span { color: var(--green); font-weight: 600; }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="particles" id="particles"></div>
  <h1>Gowtham S</h1>
  <div class="subtitle">Cloud Engineer · DevOps Architect · Full Stack Developer</div>
  <div class="typing-wrap">
    <span class="typing-line" id="typing-text">☁️ AWS | Docker | Terraform | Kubernetes</span>
  </div>
  <div class="badge-row">
    <a href="https://www.linkedin.com/in/gowtham4026/" class="badge badge-blue">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      LinkedIn
    </a>
    <a href="mailto:gowtham26.work@gmail.com" class="badge badge-red">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.364l-6.545-4.636v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.273l6.545-4.636 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
      Email
    </a>
    <a href="https://medium.com/@gowtham26.work" class="badge badge-dark">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M13.54 12a6.8 6.8 0 01-6.77 6.82A6.8 6.8 0 010 12a6.8 6.8 0 016.77-6.82A6.8 6.8 0 0113.54 12zM20.96 12c0 3.54-1.51 6.42-3.38 6.42-1.87 0-3.39-2.88-3.39-6.42s1.52-6.42 3.39-6.42 3.38 2.88 3.38 6.42M24 12c0 3.17-.53 5.75-1.19 5.75-.66 0-1.19-2.58-1.19-5.75s.53-5.75 1.19-5.75C23.47 6.25 24 8.83 24 12z"/></svg>
      Medium
    </a>
    <a href="https://www.youtube.com/@FlockZen" class="badge badge-red">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M23.498 6.186a3.016 3.016 0 00-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 00.502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 002.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 002.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/></svg>
      YouTube
    </a>
    <a href="https://github.com/gowthamselvarajgit" class="badge badge-dark">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
      GitHub
    </a>
  </div>
  <div class="info-pills">
    <div class="info-pill">📍 India</div>
    <div class="info-pill">🟢 Open to Work — <span>DevOps | Cloud | Full Stack</span></div>
    <div class="info-pill">🎓 B.E EIE · CGPA <span>7.49</span></div>
  </div>
</div>

<!-- MAIN CONTENT -->
<div class="container">

  <!-- ABOUT -->
  <div class="section" id="s1">
    <div class="section-title"><span class="icon">🧠</span> About Me</div>
    <div class="code-block">
      <div class="code-header">
        <div class="dot dot-red"></div>
        <div class="dot dot-yellow"></div>
        <div class="dot dot-green"></div>
        <span class="code-lang">TypeScript</span>
      </div>
      <div class="code-body">
        <span class="k">const</span> <span class="p">gowtham</span> <span class="k">=</span> {<br/>
        &nbsp;&nbsp;<span class="s">name</span>        : <span class="v">"Gowtham S"</span>,<br/>
        &nbsp;&nbsp;<span class="s">role</span>        : <span class="v">"Programmer Analyst Trainee @ Cognizant"</span>,<br/>
        &nbsp;&nbsp;<span class="s">location</span>    : <span class="v">"India 🇮🇳"</span>,<br/>
        &nbsp;&nbsp;<span class="s">education</span>   : <span class="v">"B.E Electronics &amp; Instrumentation — BIT (CGPA: 7.49)"</span>,<br/>
        &nbsp;&nbsp;<span class="s">currentBuild</span>: <span class="v">"GrowSpace — Secure Mobile Cloud Storage App"</span>,<br/>
        &nbsp;&nbsp;<span class="s">passions</span>    : [<span class="v">"Cloud Infrastructure"</span>, <span class="v">"DevOps Automation"</span>, <span class="v">"Full Stack Dev"</span>],<br/>
        &nbsp;&nbsp;<span class="s">achievements</span>: [<span class="v">"VISAI Finalist 2023"</span>, <span class="v">"2 Patents Filed"</span>, <span class="v">"50+ Students Trained"</span>],<br/>
        &nbsp;&nbsp;<span class="s">funFact</span>     : <span class="v">"I automate everything... including my birthday emails ☁️"</span>,<br/>
        &nbsp;&nbsp;<span class="s">contact</span>     : <span class="v">"gowtham26.work@gmail.com"</span><br/>
        };
      </div>
    </div>
  </div>

  <hr class="divider"/>

  <!-- TECH STACK -->
  <div class="section" id="s2">
    <div class="section-title"><span class="icon">🛠️</span> Tech Arsenal</div>

    <div class="skill-group">
      <div class="skill-group-label">☁️ Cloud &amp; Infrastructure</div>
      <div class="skill-pills">
        <div class="pill"><div class="dot2" style="background:#FF9900"></div>AWS</div>
        <div class="pill"><div class="dot2" style="background:#2496ED"></div>Docker</div>
        <div class="pill"><div class="dot2" style="background:#326CE5"></div>Kubernetes</div>
        <div class="pill"><div class="dot2" style="background:#7B42BC"></div>Terraform</div>
        <div class="pill"><div class="dot2" style="background:#EE0000"></div>Ansible</div>
        <div class="pill"><div class="dot2" style="background:#D24939"></div>Jenkins</div>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">💻 Languages &amp; Frameworks</div>
      <div class="skill-pills">
        <div class="pill"><div class="dot2" style="background:#ED8B00"></div>Java</div>
        <div class="pill"><div class="dot2" style="background:#6DB33F"></div>Spring Boot</div>
        <div class="pill"><div class="dot2" style="background:#00ADD8"></div>Go</div>
        <div class="pill"><div class="dot2" style="background:#61DAFB"></div>React</div>
        <div class="pill"><div class="dot2" style="background:#61DAFB"></div>React Native</div>
        <div class="pill"><div class="dot2" style="background:#4EAA25"></div>Bash</div>
        <div class="pill"><div class="dot2" style="background:#F7DF1E"></div>HTML/CSS</div>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">📊 Monitoring &amp; Observability</div>
      <div class="skill-pills">
        <div class="pill"><div class="dot2" style="background:#E6522C"></div>Prometheus</div>
        <div class="pill"><div class="dot2" style="background:#F46800"></div>Grafana</div>
        <div class="pill"><div class="dot2" style="background:#CC0000"></div>Zabbix</div>
        <div class="pill"><div class="dot2" style="background:#EE2A24"></div>Nagios</div>
        <div class="pill"><div class="dot2" style="background:#3fb950"></div>Log4j / SLF4J</div>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">🗄️ Databases &amp; Tools</div>
      <div class="skill-pills">
        <div class="pill"><div class="dot2" style="background:#00758F"></div>MySQL</div>
        <div class="pill"><div class="dot2" style="background:#FCC624"></div>Linux</div>
        <div class="pill"><div class="dot2" style="background:#F05032"></div>Git</div>
        <div class="pill"><div class="dot2" style="background:#58a6ff"></div>GitHub</div>
        <div class="pill"><div class="dot2" style="background:#C71A36"></div>Maven</div>
        <div class="pill"><div class="dot2" style="background:#3fb950"></div>Agile / Scrum</div>
      </div>
    </div>
  </div>

  <hr class="divider"/>

  <!-- EXPERIENCE -->
  <div class="section" id="s3">
    <div class="section-title"><span class="icon">💼</span> Work Experience</div>
    <div class="exp-grid">
      <div class="exp-card blue">
        <h3>🏢 Cognizant</h3>
        <div class="role">`Programmer Analyst Trainee`</div>
        <div class="date">📅 Nov 2025 – Present &nbsp;|&nbsp; Kolkata, WB</div>
        <ul>
          <li>Mastered Spring Boot for enterprise-grade backend apps</li>
          <li>Built RESTful APIs with Spring Data JPA + Spring Security</li>
          <li>Applied Agile Scrum with Maven + Log4j/SLF4J logging</li>
        </ul>
      </div>
      <div class="exp-card green">
        <h3>🎓 BIT Sathyamangalam</h3>
        <div class="role">`DevOps Trainer — Intern`</div>
        <div class="date">📅 Apr 2025 – Jul 2025</div>
        <ul>
          <li>Trained in Linux, Docker, K8s, Terraform, Ansible, Jenkins, AWS</li>
          <li>Taught Prometheus, Grafana, Zabbix, Nagios for infra monitoring</li>
          <li>Delivered AWS Cloud workshop to 50+ school students</li>
        </ul>
      </div>
    </div>
  </div>

  <hr class="divider"/>

  <!-- PROJECTS -->
  <div class="section" id="s4">
    <div class="section-title"><span class="icon">🚀</span> Featured Projects</div>
    <div class="project-grid">
      <div class="project-card" onclick="window.open('https://github.com/gowthamselvarajgit/GrowSpace')">
        <div class="proj-title">📂 GrowSpace ↗</div>
        <div class="proj-desc">Mobile-first secure cloud storage & file sharing — like Google Drive, built from scratch</div>
        <div class="tag-row">
          <span class="tag">React Native</span><span class="tag">Golang</span><span class="tag">AWS S3</span><span class="tag">Docker</span><span class="tag">Terraform</span>
        </div>
        <div class="proj-bullet">Secure login & encrypted file sharing</div>
        <div class="proj-bullet">S3-backed upload, delete & sync</div>
        <div class="proj-bullet">Full CI/CD pipeline with Jenkins + Ansible IaC</div>
      </div>
      <div class="project-card">
        <div class="proj-title">🏥 Health Insurance Claim System</div>
        <div class="proj-desc">End-to-end insurance management portal — Led team of 5 as Team Lead</div>
        <div class="tag-row">
          <span class="tag">Java</span><span class="tag">Spring Boot</span><span class="tag">MySQL</span><span class="tag">Thymeleaf</span>
        </div>
        <div class="proj-bullet">Built Policy Management module for dynamic plan creation</div>
        <div class="proj-bullet">Streamlined enrollment with real-time status tracking</div>
        <div class="proj-bullet">Designed secure DB schema with Spring Data JPA</div>
      </div>
      <div class="project-card">
        <div class="proj-title">🎂 Serverless Birthday Wishes</div>
        <div class="proj-desc">Fully automated, IAM-secured personalized email system on AWS</div>
        <div class="tag-row">
          <span class="tag">AWS Lambda</span><span class="tag">SES</span><span class="tag">EventBridge</span><span class="tag">Glue</span>
        </div>
        <div class="proj-bullet">Python Lambda functions for personalized emails</div>
        <div class="proj-bullet">Daily triggers via EventBridge automation</div>
        <div class="proj-bullet">ETL pipeline with AWS Glue + Athena analytics</div>
      </div>
      <div class="project-card" onclick="window.open('https://bit.ly/ArchitectureDiagram')">
        <div class="proj-title">📊 Real-Time E-Commerce Analytics ↗</div>
        <div class="proj-desc">Live data streaming, alerts & dashboard pipeline for e-commerce</div>
        <div class="tag-row">
          <span class="tag">Kinesis</span><span class="tag">Lambda</span><span class="tag">SNS</span><span class="tag">QuickSight</span>
        </div>
        <div class="proj-bullet">Real-time event tracking via Kinesis + Lambda</div>
        <div class="proj-bullet">Instant SNS alerts on anomalies</div>
        <div class="proj-bullet">S3 + Glue logs powering QuickSight dashboards</div>
      </div>
    </div>
  </div>

  <hr class="divider"/>

  <!-- ACHIEVEMENTS -->
  <div class="section" id="s5">
    <div class="section-title"><span class="icon">🏆</span> Achievements &amp; Recognition</div>
    <table class="ach-table">
      <tr>
        <th></th><th>Achievement</th><th>Details</th>
      </tr>
      <tr>
        <td><span class="ach-medal">🏅</span></td>
        <td><strong>VISAI Finalist 2023</strong></td>
        <td style="color:var(--muted)">AI-based Turmeric Grading System — National Level</td>
      </tr>
      <tr>
        <td><span class="ach-medal">📜</span></td>
        <td><strong>Patent Filed — Scitus Redemptio</strong></td>
        <td style="color:var(--muted)">Smart Irrigation System using IoT</td>
      </tr>
      <tr>
        <td><span class="ach-medal">📜</span></td>
        <td><strong>Patent Filed — Health Flush</strong></td>
        <td style="color:var(--muted)">Smart Urinalysis System</td>
      </tr>
      <tr>
        <td><span class="ach-medal">👨‍🏫</span></td>
        <td><strong>Cloud Trainer</strong></td>
        <td style="color:var(--muted)">Taught AWS Cloud to 50+ school students (BAVN)</td>
      </tr>
      <tr>
        <td><span class="ach-medal">🎤</span></td>
        <td><strong>Event Coordinator</strong></td>
        <td style="color:var(--muted)">Organized Ersmernoz-23 &amp; Ersmernoz-24 paper presentations</td>
      </tr>
    </table>
  </div>

  <hr class="divider"/>

  <!-- CERTS -->
  <div class="section" id="s6">
    <div class="section-title"><span class="icon">📜</span> Certifications</div>
    <div class="cert-row">
      <div class="cert-card">
        <div class="cert-icon">🐙</div>
        <div class="cert-name">GitHub Foundations</div>
        <div class="cert-by">GitHub · June 2024</div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">☕</div>
        <div class="cert-name">Java (Basic)</div>
        <div class="cert-by">HackerRank · Sept 2024</div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">☁️</div>
        <div class="cert-name">AWS Cloud Practitioner</div>
        <div class="cert-by">Udemy (Stephane Maarek) · Jan 2024</div>
      </div>
    </div>
  </div>

  <hr class="divider"/>

  <!-- STATS -->
  <div class="section" id="s7">
    <div class="section-title"><span class="icon">📊</span> GitHub Stats</div>
    <div class="stats-grid">
      <div class="stat-card"><div class="stat-num" id="c1">0</div><div class="stat-label">Projects Built</div></div>
      <div class="stat-card"><div class="stat-num" id="c2">0</div><div class="stat-label">Students Trained</div></div>
      <div class="stat-card"><div class="stat-num" id="c3">0</div><div class="stat-label">Certs Earned</div></div>
    </div>
    <div style="display:grid; grid-template-columns:1fr 1fr; gap:12px;">
      <img src="https://github-readme-stats.vercel.app/api?username=gowthamselvarajgit&show_icons=true&theme=github_dark&count_private=true&hide_border=true&bg_color=161b22&title_color=58a6ff&icon_color=58a6ff&text_color=8b949e" style="width:100%;border-radius:8px;" onerror="this.style.display='none'"/>
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=gowthamselvarajgit&layout=compact&theme=github_dark&hide_border=true&bg_color=161b22&title_color=58a6ff&text_color=8b949e" style="width:100%;border-radius:8px;" onerror="this.style.display='none'"/>
    </div>
  </div>

  <hr class="divider"/>

  <!-- CONNECT -->
  <div class="section" id="s8">
    <div class="section-title"><span class="icon">🌐</span> Connect With Me</div>
    <div class="connect-row">
      <a href="https://www.linkedin.com/in/gowtham4026/" class="connect-btn"><span class="icon">💼</span>LinkedIn</a>
      <a href="mailto:gowtham26.work@gmail.com" class="connect-btn"><span class="icon">📧</span>Email</a>
      <a href="https://medium.com/@gowtham26.work" class="connect-btn"><span class="icon">✍️</span>Medium</a>
      <a href="https://www.youtube.com/@FlockZen" class="connect-btn"><span class="icon">▶️</span>YouTube</a>
      <a href="https://github.com/gowthamselvarajgit" class="connect-btn"><span class="icon">🐙</span>GitHub</a>
    </div>
  </div>

</div>

<!-- FOOTER -->
<div class="footer">
  <div class="footer-typing" id="footer-txt">Automate Everything. ⚙️</div>
  <div style="font-size:12px;color:var(--muted);margin-top:8px;">⭐ If you like my work, consider starring my repos!</div>
</div>

<script>
// Particles
const pc = document.getElementById('particles');
for(let i=0;i<30;i++){
  const p = document.createElement('div');
  p.className = 'particle';
  p.style.left = Math.random()*100+'%';
  p.style.top = (50+Math.random()*50)+'%';
  p.style.width = p.style.height = (1+Math.random()*3)+'px';
  p.style.animationDuration = (4+Math.random()*8)+'s';
  p.style.animationDelay = (Math.random()*6)+'s';
  p.style.opacity = 0;
  pc.appendChild(p);
}

// Typing cycle
const lines = [
  "☁️ AWS | Docker | Terraform | Kubernetes",
  "🔧 CI/CD Pipelines | Jenkins | Ansible",
  "💻 Spring Boot | React | Go | Full Stack",
  "🚀 Building GrowSpace — Cloud Storage App",
  "🏆 VISAI Finalist 2023 | 2 Patents Filed"
];
let li = 0;
const typingEl = document.getElementById('typing-text');
setInterval(()=>{
  typingEl.style.opacity = '0';
  typingEl.style.transform = 'translateY(10px)';
  setTimeout(()=>{
    li = (li+1)%lines.length;
    typingEl.textContent = lines[li];
    typingEl.style.transition = 'opacity 0.4s, transform 0.4s';
    typingEl.style.opacity = '1';
    typingEl.style.transform = 'translateY(0)';
  }, 400);
}, 3000);

// Scroll reveal
const obs = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{ if(e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.1 });
document.querySelectorAll('.section').forEach(s=>obs.observe(s));

// Counter animation
function animCount(el, target, suffix=''){
  let val = 0;
  const step = Math.ceil(target/40);
  const t = setInterval(()=>{
    val = Math.min(val+step, target);
    el.textContent = val + suffix;
    if(val>=target) clearInterval(t);
  }, 40);
}
const statsObs = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      animCount(document.getElementById('c1'), 4);
      animCount(document.getElementById('c2'), 50, '+');
      animCount(document.getElementById('c3'), 3);
      statsObs.disconnect();
    }
  });
}, {threshold:0.3});
statsObs.observe(document.getElementById('s7'));

// Footer typing cycle
const footerLines = ["Automate Everything. ⚙️","Simplify the Complex. 🧩","Empower Teams with Cloud. ☁️","Code. Ship. Repeat. 🚀"];
let fi = 0;
const fte = document.getElementById('footer-txt');
setInterval(()=>{
  fte.style.opacity='0';
  setTimeout(()=>{
    fi=(fi+1)%footerLines.length;
    fte.textContent=footerLines[fi];
    fte.style.transition='opacity 0.5s';
    fte.style.opacity='1';
  },400);
}, 2800);
</script>
</body>
</html>
