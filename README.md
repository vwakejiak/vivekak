<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dr. Vivekanandan A K — Materials Scientist & Nanotechnology Researcher</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #F9F6F0;
    --warm-white: #FDFCFA;
    --dark: #1A1612;
    --mid: #4A3F35;
    --accent: #B8763A;
    --accent-light: #D4955A;
    --border: #E2D8CC;
    --soft: #8A7B6E;
    --section-bg: #F2EDE5;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--warm-white);
    color: var(--dark);
    font-size: 15px;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ─── NAV ─── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(253,252,250,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 0 5vw;
    height: 64px;
    display: flex; align-items: center; justify-content: space-between;
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.25rem;
    font-weight: 600;
    color: var(--dark);
    letter-spacing: 0.02em;
    text-decoration: none;
  }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-size: 0.78rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--mid);
    text-decoration: none;
    font-weight: 500;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }

  /* ─── HERO ─── */
  #hero {
    min-height: 100vh;
    padding: 64px 5vw 0;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 6rem;
    background: var(--warm-white);
    position: relative;
  }
  
  #hero::before {
    content: '';
    position: absolute;
    top: 0; right: 0;
    width: 45vw; height: 100%;
    background: var(--section-bg);
    z-index: 0;
  }
  .hero-text { position: relative; z-index: 1; padding: 4rem 0; }
  .hero-tag {
    display: inline-block;
    font-size: 0.7rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    border: 1px solid var(--accent);
    padding: 0.35rem 1rem;
    border-radius: 100px;
    margin-bottom: 2rem;
    font-weight: 500;
  }
  .hero-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3rem, 5vw, 4.5rem);
    font-weight: 300;
    line-height: 1.1;
    color: var(--dark);
    margin-bottom: 0.5rem;
  }
  .hero-name span { font-style: italic; color: var(--accent); }
  .hero-title {
    font-size: 0.85rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--soft);
    margin-bottom: 2rem;
    font-weight: 400;
  }
  .hero-summary {
    font-size: 1rem;
    color: var(--mid);
    max-width: 480px;
    line-height: 1.8;
    margin-bottom: 2.5rem;
  }
  .hero-stats {
    display: flex; gap: 2.5rem; margin-bottom: 2.5rem;
  }
  .stat { border-left: 2px solid var(--accent); padding-left: 1rem; }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2rem;
    font-weight: 600;
    color: var(--dark);
    line-height: 1;
  }
  .stat-label { font-size: 0.72rem; color: var(--soft); text-transform: uppercase; letter-spacing: 0.08em; margin-top: 0.2rem; }

  .hero-cta { display: flex; gap: 1rem; flex-wrap: wrap; }
  .btn-primary {
    background: var(--accent);
    color: #fff;
    padding: 0.75rem 2rem;
    border-radius: 4px;
    font-size: 0.78rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: 500;
    transition: background 0.2s, transform 0.2s;
  }
  .btn-primary:hover { background: var(--accent-light); transform: translateY(-1px); }
  .btn-outline {
    border: 1.5px solid var(--border);
    color: var(--mid);
    padding: 0.75rem 2rem;
    border-radius: 4px;
    font-size: 0.78rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: 500;
    transition: border-color 0.2s, color 0.2s;
  }
  .btn-outline:hover { border-color: var(--accent); color: var(--accent); }

  /* Photo area */
  .hero-photo { position: relative; z-index: 1; display: flex; justify-content: center; align-items: center; padding: 4rem 2rem; }
  .photo-frame {
    width: 320px; height: 380px;
    border-radius: 4px;
    background: var(--border);
    position: relative;
    overflow: hidden;
    box-shadow: 0 32px 64px rgba(26,22,18,0.12);
  }
  .photo-frame img { width: 100%; height: 100%; object-fit: cover; display: block; }
  .photo-placeholder {
    width: 100%; height: 100%;
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    background: linear-gradient(145deg, #EDE7DC, #D8CEBC);
    cursor: pointer;
    gap: 0.75rem;
    transition: background 0.3s;
  }
  .photo-placeholder:hover { background: linear-gradient(145deg, #E2D9CC, #CFC3AE); }
  .photo-placeholder svg { opacity: 0.45; }
  .photo-placeholder span { font-size: 0.75rem; color: var(--soft); letter-spacing: 0.08em; text-transform: uppercase; }
  .photo-input { display: none; }
  .photo-corner {
    position: absolute; bottom: -10px; right: -10px;
    width: 80px; height: 80px;
    border: 2px solid var(--accent);
    border-radius: 4px;
    z-index: -1;
  }

  /* ─── SECTION COMMON ─── */
  section { padding: 6rem 5vw; }
  .section-label {
    font-size: 0.7rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    font-weight: 500;
    margin-bottom: 0.75rem;
  }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 300;
    line-height: 1.15;
    color: var(--dark);
    margin-bottom: 3rem;
  }
  .divider { width: 48px; height: 2px; background: var(--accent); margin: 1.5rem 0 3rem; }

  /* ─── ABOUT ─── */
  #about { background: var(--section-bg); }
  .about-grid { display: grid; grid-template-columns: 1fr 1.8fr; gap: 5rem; align-items: start; }
  .about-photo-wrap { position: relative; }
  .about-photo-frame {
    width: 100%; aspect-ratio: 3/4;
    border-radius: 4px;
    overflow: hidden;
    box-shadow: 0 20px 50px rgba(26,22,18,0.1);
    background: var(--border);
  }
  .about-photo-frame img { width: 100%; height: 100%; object-fit: cover; }
  .about-badge {
    position: absolute; bottom: -20px; right: -20px;
    background: var(--accent);
    color: #fff;
    padding: 1.25rem 1.5rem;
    border-radius: 4px;
    text-align: center;
    font-family: 'Cormorant Garamond', serif;
    box-shadow: 0 8px 24px rgba(184,118,58,0.35);
  }
  .about-badge-num { font-size: 2.5rem; font-weight: 600; line-height: 1; display: block; }
  .about-badge-text { font-size: 0.7rem; letter-spacing: 0.1em; text-transform: uppercase; margin-top: 0.25rem; }

  .about-content p { color: var(--mid); margin-bottom: 1.25rem; line-height: 1.85; }
  .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-top: 2rem; }
  .contact-item {
    display: flex; align-items: center; gap: 0.75rem;
    font-size: 0.88rem; color: var(--mid);
  }
  .contact-item a { color: var(--accent); text-decoration: none; }
  .contact-item a:hover { text-decoration: underline; }
  .contact-icon { color: var(--accent); flex-shrink: 0; }

  /* ─── EXPERIENCE ─── */
  #experience { background: var(--warm-white); }
  .timeline { position: relative; }
  .timeline::before {
    content: '';
    position: absolute; left: 180px; top: 0; bottom: 0;
    width: 1px; background: var(--border);
  }
  .timeline-item { display: grid; grid-template-columns: 180px 1fr; gap: 0; margin-bottom: 3rem; position: relative; }
  .timeline-date {
    padding-right: 2.5rem; padding-top: 0.2rem;
    text-align: right;
    font-size: 0.78rem; color: var(--soft);
    line-height: 1.5;
  }
  .timeline-dot {
    position: absolute; left: 180px; top: 6px;
    width: 10px; height: 10px;
    background: var(--accent); border-radius: 50%;
    transform: translateX(-4.5px);
  }
  .timeline-body { padding-left: 2.5rem; }
  .timeline-role {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.25rem; font-weight: 600;
    color: var(--dark); margin-bottom: 0.2rem;
  }
  .timeline-place { font-size: 0.82rem; color: var(--accent); font-weight: 500; margin-bottom: 0.75rem; letter-spacing: 0.02em; }
  .timeline-desc { font-size: 0.88rem; color: var(--mid); line-height: 1.75; }
  .timeline-desc ul { padding-left: 1.2rem; margin-top: 0.5rem; }
  .timeline-desc ul li { margin-bottom: 0.3rem; }

  /* ─── EDUCATION ─── */
  #education { background: var(--section-bg); }
  .edu-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 2rem; }
  .edu-card {
    background: var(--warm-white);
    border-radius: 6px;
    padding: 2rem;
    border-top: 3px solid var(--accent);
    box-shadow: 0 4px 20px rgba(26,22,18,0.06);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .edu-card:hover { transform: translateY(-4px); box-shadow: 0 12px 36px rgba(26,22,18,0.1); }
  .edu-degree {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.5rem; font-weight: 600;
    color: var(--accent); margin-bottom: 0.5rem;
  }
  .edu-year { font-size: 0.75rem; color: var(--soft); text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 0.75rem; }
  .edu-inst { font-weight: 500; color: var(--dark); margin-bottom: 0.5rem; font-size: 0.9rem; }
  .edu-dept { font-size: 0.82rem; color: var(--soft); margin-bottom: 1rem; }
  .edu-thesis { font-size: 0.8rem; color: var(--mid); font-style: italic; line-height: 1.6; border-left: 2px solid var(--border); padding-left: 0.75rem; }

  /* ─── SKILLS ─── */
  #skills { background: var(--dark); color: var(--cream); }
  #skills .section-title { color: var(--cream); }
  .skills-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 2rem; }
  .skill-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 6px;
    padding: 2rem 1.5rem;
    transition: background 0.2s, border-color 0.2s;
  }
  .skill-card:hover { background: rgba(255,255,255,0.08); border-color: rgba(184,118,58,0.5); }
  .skill-icon { color: var(--accent); margin-bottom: 1rem; }
  .skill-category { font-size: 0.72rem; letter-spacing: 0.12em; text-transform: uppercase; color: var(--accent); margin-bottom: 0.5rem; font-weight: 500; }
  .skill-list { list-style: none; }
  .skill-list li { font-size: 0.88rem; color: rgba(249,246,240,0.75); padding: 0.3rem 0; border-bottom: 1px solid rgba(255,255,255,0.07); }
  .skill-list li:last-child { border-bottom: none; }

  /* ─── PUBLICATIONS ─── */
  #publications { background: var(--warm-white); }
  .pub-filter { display: flex; gap: 0.75rem; flex-wrap: wrap; margin-bottom: 2.5rem; }
  .pub-filter-btn {
    font-size: 0.75rem; letter-spacing: 0.08em; text-transform: uppercase;
    padding: 0.4rem 1.2rem; border-radius: 100px;
    border: 1.5px solid var(--border);
    background: transparent; color: var(--soft);
    cursor: pointer; transition: all 0.2s; font-weight: 500;
  }
  .pub-filter-btn.active, .pub-filter-btn:hover { border-color: var(--accent); color: var(--accent); background: rgba(184,118,58,0.06); }

  .pub-list { display: flex; flex-direction: column; gap: 1.25rem; }
  .pub-item {
    padding: 1.5rem 2rem;
    border-radius: 6px;
    background: var(--section-bg);
    border-left: 3px solid transparent;
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .pub-item:hover { border-left-color: var(--accent); box-shadow: 0 4px 20px rgba(26,22,18,0.06); }
  .pub-badge {
    display: inline-flex; align-items: center; gap: 0.4rem;
    font-size: 0.68rem; letter-spacing: 0.1em; text-transform: uppercase;
    background: rgba(184,118,58,0.12); color: var(--accent);
    padding: 0.25rem 0.8rem; border-radius: 100px; margin-bottom: 0.6rem;
    font-weight: 600;
  }
  .pub-title { font-family: 'Cormorant Garamond', serif; font-size: 1.05rem; font-weight: 600; color: var(--dark); line-height: 1.4; margin-bottom: 0.4rem; }
  .pub-meta { font-size: 0.8rem; color: var(--soft); }
  .pub-meta strong { color: var(--mid); }
  .pub-if { font-size: 0.72rem; color: var(--accent); font-weight: 600; }

  /* ─── COLLABORATIONS ─── */
  #collaborations { background: var(--section-bg); }
  .collab-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.5rem; }
  .collab-card {
    background: var(--warm-white); border-radius: 6px;
    padding: 2rem; display: flex; gap: 1.25rem;
    box-shadow: 0 2px 12px rgba(26,22,18,0.06);
    transition: box-shadow 0.2s;
  }
  .collab-card:hover { box-shadow: 0 8px 30px rgba(26,22,18,0.1); }
  .collab-icon { color: var(--accent); flex-shrink: 0; margin-top: 0.2rem; }
  .collab-name { font-weight: 500; color: var(--dark); margin-bottom: 0.3rem; }
  .collab-year { font-size: 0.75rem; color: var(--accent); text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 0.5rem; }
  .collab-desc { font-size: 0.85rem; color: var(--mid); line-height: 1.65; }

  /* ─── ACHIEVEMENTS ─── */
  #achievements { background: var(--warm-white); }
  .achieve-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 2rem; }
  .achieve-card {
    text-align: center; padding: 2.5rem 2rem;
    border-radius: 6px; background: var(--section-bg);
    border: 1px solid var(--border);
    transition: border-color 0.2s, transform 0.2s;
  }
  .achieve-card:hover { border-color: var(--accent); transform: translateY(-3px); }
  .achieve-icon { font-size: 2.5rem; margin-bottom: 1rem; }
  .achieve-title { font-family: 'Cormorant Garamond', serif; font-size: 1.15rem; font-weight: 600; color: var(--dark); margin-bottom: 0.5rem; }
  .achieve-desc { font-size: 0.85rem; color: var(--soft); line-height: 1.65; }

  /* ─── INVITED TALKS ─── */
  #talks { background: var(--section-bg); }
  .talks-list { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; }
  .talk-card {
    background: var(--warm-white); border-radius: 6px; padding: 1.75rem;
    box-shadow: 0 2px 10px rgba(26,22,18,0.05);
    transition: box-shadow 0.2s;
  }
  .talk-card:hover { box-shadow: 0 8px 28px rgba(26,22,18,0.1); }
  .talk-year { font-size: 0.72rem; color: var(--accent); text-transform: uppercase; letter-spacing: 0.1em; font-weight: 600; margin-bottom: 0.5rem; }
  .talk-title { font-family: 'Cormorant Garamond', serif; font-size: 1rem; font-weight: 600; color: var(--dark); margin-bottom: 0.5rem; line-height: 1.4; }
  .talk-venue { font-size: 0.8rem; color: var(--soft); }

  /* ─── GALLERY ─── */
  #gallery { background: var(--warm-white); }
  .gallery-intro { color: var(--mid); margin-bottom: 2.5rem; max-width: 600px; }
  .gallery-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1rem; }
  .gallery-slot {
    aspect-ratio: 1;
    border-radius: 4px;
    overflow: hidden;
    background: var(--section-bg);
    border: 2px dashed var(--border);
    cursor: pointer;
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    gap: 0.5rem;
    transition: border-color 0.2s, background 0.2s;
    position: relative;
  }
  .gallery-slot:hover { border-color: var(--accent); background: rgba(184,118,58,0.04); }
  .gallery-slot img {
    position: absolute; inset: 0;
    width: 100%; height: 100%; object-fit: cover;
    display: none;
  }
  .gallery-slot.has-image img { display: block; }
  .gallery-slot.has-image .upload-hint { display: none; }
  .upload-hint { display: flex; flex-direction: column; align-items: center; gap: 0.4rem; }
  .upload-hint svg { opacity: 0.35; }
  .upload-hint span { font-size: 0.68rem; color: var(--soft); text-transform: uppercase; letter-spacing: 0.08em; }
  .gallery-input { display: none; }

  /* ─── FOOTER ─── */
  footer {
    background: var(--dark);
    color: rgba(249,246,240,0.6);
    padding: 3rem 5vw;
    display: flex; justify-content: space-between; align-items: center;
    flex-wrap: wrap; gap: 1rem;
  }
  .footer-name { font-family: 'Cormorant Garamond', serif; font-size: 1.2rem; color: var(--cream); font-weight: 300; }
  .footer-links { display: flex; gap: 1.5rem; }
  .footer-links a { font-size: 0.75rem; color: rgba(249,246,240,0.5); text-decoration: none; letter-spacing: 0.08em; text-transform: uppercase; transition: color 0.2s; }
  .footer-links a:hover { color: var(--accent); }

  /* ─── ANIMATIONS ─── */
  @keyframes fadeInUp { from { opacity:0; transform: translateY(24px); } to { opacity:1; transform: translateY(0); } }
  .fade-in { animation: fadeInUp 0.7s ease both; }
  .fade-in-2 { animation: fadeInUp 0.7s 0.15s ease both; }
  .fade-in-3 { animation: fadeInUp 0.7s 0.3s ease both; }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 900px) {
    #hero { grid-template-columns: 1fr; }
    #hero::before { display: none; }
    .hero-photo { padding: 2rem 0; }
    .about-grid, .edu-grid, .skills-grid, .achieve-grid, .talks-list { grid-template-columns: 1fr; }
    .collab-grid { grid-template-columns: 1fr; }
    .timeline::before { left: 0; }
    .timeline-item { grid-template-columns: 1fr; padding-left: 1.5rem; }
    .timeline-date { text-align: left; padding-right: 0; }
    .timeline-dot { left: 0; }
    .gallery-grid { grid-template-columns: repeat(2, 1fr); }
    nav .nav-links { display: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#hero" class="nav-logo">Dr. Vivekanandan A K</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#publications">Publications</a></li>
    <li><a href="#achievements">Achievements</a></li>
    <li><a href="#gallery">Gallery</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-text fade-in">
    <span class="hero-tag">Materials Scientist &amp; Researcher</span>
    <h1 class="hero-name">Dr. <span>Vivekanandan</span> A K</h1>
    <p class="hero-title">Materials Specialist · Nanotechnology Researcher · Postdoctoral Researcher</p>
    <p class="hero-summary">
      Experienced researcher and academic with 11+ years in aerospace materials, nanotechnology, and ultrasonic-assisted manufacturing. Ph.D. from NTUST, Taiwan — with over 12 Q1 journal publications and active international collaborations.
    </p>
    <div class="hero-stats">
      <div class="stat"><div class="stat-num">11+</div><div class="stat-label">Years Experience</div></div>
      <div class="stat"><div class="stat-num">12+</div><div class="stat-label">Q1 Publications</div></div>
      <div class="stat"><div class="stat-num">3</div><div class="stat-label">Postdoctoral Positions</div></div>
    </div>
    <div class="hero-cta">
      <a href="mailto:vivekak77@gmail.com" class="btn-primary">Get In Touch</a>
      <a href="#publications" class="btn-outline">View Research</a>
    </div>
  </div>
  <div class="hero-photo fade-in-2">
    <div class="photo-frame">
      <label for="hero-photo-input">
        <div class="photo-placeholder" id="hero-placeholder">
          <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#8A7B6E" stroke-width="1.5"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          <span>Upload Profile Photo</span>
        </div>
        <img id="hero-img" src="" alt="Dr. Vivekanandan">
      </label>
      <input type="file" accept="image/*" class="photo-input" id="hero-photo-input">
    </div>
    <div class="photo-corner"></div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-photo-wrap">
      <div class="about-photo-frame">
        <label for="about-photo-input" style="cursor:pointer;display:block;width:100%;height:100%;">
          <div style="width:100%;height:100%;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:0.6rem;background:linear-gradient(145deg,#EDE7DC,#D8CEBC);" id="about-placeholder">
            <svg width="36" height="36" viewBox="0 0 24 24" fill="none" stroke="#8A7B6E" stroke-width="1.5"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            <span style="font-size:0.7rem;color:#8A7B6E;letter-spacing:0.1em;text-transform:uppercase;">Upload Photo</span>
          </div>
          <img id="about-img" src="" alt="About Dr. Vivekanandan" style="display:none;width:100%;height:100%;object-fit:cover;">
        </label>
        <input type="file" accept="image/*" class="photo-input" id="about-photo-input">
      </div>
      <div class="about-badge">
        <span class="about-badge-num">11+</span>
        <span class="about-badge-text">Years in Research</span>
      </div>
    </div>
    <div class="about-content">
      <p class="section-label">About Me</p>
      <h2 class="section-title">Materials Scientist with a Global Research Footprint</h2>
      <p>Dr. Vivekanandan A K is an experienced researcher and academic specialising in aerospace materials, nanotechnology, and ultrasonic-assisted manufacturing. Holding a Ph.D. in Mechanical Engineering from the National Taiwan University of Science and Technology, he has completed multiple postdoctoral positions at premier institutions in Taiwan.</p>
      <p>His research spans nanofabrication, corrosion protection, thermoelectric devices, and high-entropy materials. With over 12 Q1-tier publications and ongoing international collaborations, he brings a proven record of high-impact scientific contributions and academic leadership.</p>
      <p>Currently serving as a Postdoctoral Researcher at National Tsing Hua University, Taiwan, Dr. Vivekanandan continues to develop next-generation materials using cutting-edge additive manufacturing techniques.</p>

      <div class="contact-grid">
        <div class="contact-item">
          <svg class="contact-icon" width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M22 16.92v3a2 2 0 0 1-2.18 2A19.79 19.79 0 0 1 11.61 19a19.5 19.5 0 0 1-6-6A19.79 19.79 0 0 1 3.09 4.18 2 2 0 0 1 5.07 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L9.91 9.91a16 16 0 0 0 6 6l.46-.46a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 23 17.92z"/></svg>
          <span>+91-7708969010</span>
        </div>
        <div class="contact-item">
          <svg class="contact-icon" width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          <a href="mailto:vivekak77@gmail.com">vivekak77@gmail.com</a>
        </div>
        <div class="contact-item">
          <svg class="contact-icon" width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          <a href="https://linkedin.com/in/vivekanandan-ak" target="_blank">LinkedIn Profile</a>
        </div>
        <div class="contact-item">
          <svg class="contact-icon" width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M12 20h9"/><path d="M16.5 3.5a2.121 2.121 0 0 1 3 3L7 19l-4 1 1-4L16.5 3.5z"/></svg>
          <a href="https://scholar.google.com.tw/citations?user=urPd1vwAAAAJ&hl=en" target="_blank">Google Scholar</a>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <p class="section-label">Career Journey</p>
  <h2 class="section-title">Academic &amp; Research Experience</h2>
  <div class="timeline">

    <div class="timeline-item">
      <div class="timeline-date">Nov 2025 — Present</div>
      <div class="timeline-dot"></div>
      <div class="timeline-body">
        <div class="timeline-role">Postdoctoral Researcher — Material Science</div>
        <div class="timeline-place">National Tsing Hua University, Taiwan</div>
        <div class="timeline-desc">Development and optimization of high-entropy materials utilizing state-of-the-art additive manufacturing techniques to achieve superior material properties.</div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Aug 2022 — Mar 2025</div>
      <div class="timeline-dot"></div>
      <div class="timeline-body">
        <div class="timeline-role">Associate Professor — Aeronautical Engineering</div>
        <div class="timeline-place">Annasaheb Dange College of Engineering and Technology, Maharashtra, India</div>
        <div class="timeline-desc">
          <ul>
            <li>Taught aircraft structures, composite materials, and strength of materials.</li>
            <li>Conducted advanced research in aerospace materials and led funded projects on corrosion protection.</li>
            <li>Published high-impact journal articles in Q1 journals.</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Mar 2022 — Jul 2022</div>
      <div class="timeline-dot"></div>
      <div class="timeline-body">
        <div class="timeline-role">Postdoctoral Researcher — Material Science</div>
        <div class="timeline-place">National Tsing Hua University, Taiwan</div>
        <div class="timeline-desc">
          <ul>
            <li>Analyzed and developed thermoelectrical materials and devices for aircraft power system alternators.</li>
            <li>Designed ultrasonic tools for precision cutting and processing of micro components.</li>
            <li>Performed research, testing, data gathering, measurements, and engineering analysis.</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Apr 2021 — Feb 2022</div>
      <div class="timeline-dot"></div>
      <div class="timeline-body">
        <div class="timeline-role">Postdoctoral Researcher — Material Science</div>
        <div class="timeline-place">National Yang Ming Chiao Tung University, Taiwan</div>
        <div class="timeline-desc">Fabrication of ZnO, SnO₂ &amp; InSb high aspect ratio single nanowire-based devices using Vacuum die-casting/FIB techniques to demonstrate enhanced electronic properties.</div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Feb 2017 — Mar 2021</div>
      <div class="timeline-dot"></div>
      <div class="timeline-body">
        <div class="timeline-role">Research Assistant — Mechanical Engineering</div>
        <div class="timeline-place">National Taiwan University of Science and Technology, Taiwan</div>
        <div class="timeline-desc">
          <ul>
            <li>Non-linear ultrasonic irradiation behavior: cavitational effects, intensity, and temperature gradient estimations.</li>
            <li>Taught mechanical design engineering to undergraduate exchange students.</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Jul 2015 — Dec 2016</div>
      <div class="timeline-dot"></div>
      <div class="timeline-body">
        <div class="timeline-role">Assistant Professor — Aeronautical Engineering</div>
        <div class="timeline-place">SAMS College of Engineering &amp; Technology, India</div>
        <div class="timeline-desc">Delivered lectures on strength of materials, composite materials, finite element methods, and thermodynamics.</div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Jul 2013 — Dec 2014</div>
      <div class="timeline-dot"></div>
      <div class="timeline-body">
        <div class="timeline-role">Assistant Professor — Aeronautical Engineering</div>
        <div class="timeline-place">ECET, Coimbatore, India</div>
        <div class="timeline-desc">Taught strength of materials, theory of elasticity, theory of vibration, and avionics for undergraduate students.</div>
      </div>
    </div>

  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <p class="section-label">Academic Background</p>
  <h2 class="section-title">Education</h2>
  <div class="edu-grid">
    <div class="edu-card">
      <div class="edu-degree">Ph.D.</div>
      <div class="edu-year">2017 – 2021</div>
      <div class="edu-inst">National Taiwan University of Science and Technology, Taiwan</div>
      <div class="edu-dept">Department of Mechanical Engineering</div>
      <div class="edu-thesis">"Acoustical Influence on the Synthesis of Hybrid Transition Metal Oxide Nanomaterials for Multifunctional Sensing Applications"</div>
    </div>
    <div class="edu-card">
      <div class="edu-degree">M.Tech</div>
      <div class="edu-year">2011 – 2013</div>
      <div class="edu-inst">Hindustan University, India</div>
      <div class="edu-dept">Department of Aeronautical Engineering</div>
      <div class="edu-thesis">"FEM-based Fatigue Analysis on Spar Lugs of Lightweight Aircraft"</div>
    </div>
    <div class="edu-card">
      <div class="edu-degree">B.E.</div>
      <div class="edu-year">2006 – 2010</div>
      <div class="edu-inst">Anna University, India</div>
      <div class="edu-dept">Department of Aeronautical Engineering</div>
      <div class="edu-thesis">"Microstructural and Mechanical Evaluation of SiC Reinforced 8090 Al–Li MMCs"</div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <p class="section-label" style="color:var(--accent);">Expertise</p>
  <h2 class="section-title">Technical Skills</h2>
  <div class="skills-grid">
    <div class="skill-card">
      <div class="skill-icon">
        <svg width="28" height="28" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><circle cx="12" cy="12" r="3"/><path d="M19.07 4.93a10 10 0 0 1 0 14.14M4.93 4.93a10 10 0 0 0 0 14.14"/></svg>
      </div>
      <div class="skill-category">Materials &amp; Processing</div>
      <ul class="skill-list">
        <li>PEO Coatings</li>
        <li>AAO Templates</li>
        <li>Surface Treatment</li>
        <li>Coating Techniques</li>
        <li>High-Entropy Materials</li>
      </ul>
    </div>
    <div class="skill-card">
      <div class="skill-icon">
        <svg width="28" height="28" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><path d="M9 3H5a2 2 0 0 0-2 2v4m6-6h10a2 2 0 0 1 2 2v4M9 3v18m0 0h10a2 2 0 0 0 2-2v-4M9 21H5a2 2 0 0 1-2-2v-4m0 0h18"/></svg>
      </div>
      <div class="skill-category">Characterization</div>
      <ul class="skill-list">
        <li>SEM / TEM</li>
        <li>XRD Analysis</li>
        <li>Raman Spectroscopy</li>
        <li>FTIR</li>
        <li>FIB Techniques</li>
      </ul>
    </div>
    <div class="skill-card">
      <div class="skill-icon">
        <svg width="28" height="28" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>
      </div>
      <div class="skill-category">Simulation &amp; Analysis</div>
      <ul class="skill-list">
        <li>ANSYS</li>
        <li>SolidWorks</li>
        <li>MSC Adams</li>
        <li>Finite Element Analysis</li>
      </ul>
    </div>
    <div class="skill-card">
      <div class="skill-icon">
        <svg width="28" height="28" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/></svg>
      </div>
      <div class="skill-category">Fabrication &amp; Testing</div>
      <ul class="skill-list">
        <li>Ultrasonic Tool Design</li>
        <li>Precision Machining</li>
        <li>Microfabrication</li>
        <li>Additive Manufacturing</li>
      </ul>
    </div>
  </div>
</section>

<!-- PUBLICATIONS -->
<section id="publications">
  <p class="section-label">Research Output</p>
  <h2 class="section-title">Selected Publications</h2>
  <div class="pub-list">

    <div class="pub-item">
      <div class="pub-badge">Q1 · IF 5.5 · 2025</div>
      <div class="pub-title">High-performance Electrochemical Sensors Using Sn-Bi₂O₃ nanoparticle on graphene oxide nanocomposite for Selective Detection of Antibiotic in Diverse Environmental Samples</div>
      <div class="pub-meta"><strong>Krishnanpandi A, Munusamy N, Vivekanandan AK</strong> et al. · Journal of the Taiwan Institute of Chemical Engineers</div>
    </div>

    <div class="pub-item">
      <div class="pub-badge">Q1 · IF 8.1 · 2024</div>
      <div class="pub-title">Progress and Perspective in harnessing MXene–carbon-based composites (0–3D): Synthesis, performance, and applications</div>
      <div class="pub-meta"><strong>Muthukutty B, Kumar PS, Vivekanandan AK</strong> et al. · Chemosphere</div>
    </div>

    <div class="pub-item">
      <div class="pub-badge">Q1 · IF 3.4 · 2023</div>
      <div class="pub-title">Growth kinetics of crumb-like structure formation on SnO₂ nanowires during direct oxidation</div>
      <div class="pub-meta"><strong>Vivekanandan AK</strong>, Shao-Fu C, Zhong-You L, Shih-Hsun C · Heliyon</div>
    </div>

    <div class="pub-item">
      <div class="pub-badge">Q1 · IF 4.7 · 2022</div>
      <div class="pub-title">Tailoring InSb nanowires for high thermoelectric performance using AAO template-assisted die-casting process</div>
      <div class="pub-meta"><strong>Vivekanandan AK</strong>, Lee CW, Chen SH · Nanomaterials</div>
    </div>

    <div class="pub-item">
      <div class="pub-badge">Q1 · IF 12.7 · 2021</div>
      <div class="pub-title">Novel Construction of Barium Tungstate Unified Oxidised Carbon Black Composite as Electrode Modifier for Low Potential Detection of Antihistamine Drug Promethazine Hydrochloride</div>
      <div class="pub-meta"><strong>Muthukutty B, Vivekanandan AK</strong>, Chen SM, Chen SH · Composites Part B</div>
    </div>

    <div class="pub-item">
      <div class="pub-badge">Q1 · IF 7.1 · 2020</div>
      <div class="pub-title">Intermetallic Compound Cu₂Sb Nanoparticle for Effective Electrocatalytic Oxidation of Antibiotic Drug: Sulphadiazine</div>
      <div class="pub-meta"><strong>Vivekanandan AK</strong>, Muthukutty B, Chen SM, Chen SH · ACS Sustainable Chemistry and Engineering</div>
    </div>

    <div class="pub-item">
      <div class="pub-badge">Q1 · IF 8.7 · 2020</div>
      <div class="pub-title">Sonochemical synthesis of nickel-manganous oxide nanocrumbs decorated partially reduced graphene oxide for efficient electrochemical detection of metronidazole</div>
      <div class="pub-meta"><strong>Vivekanandan AK</strong>, Subash V, Chen SM, Chen SH · Ultrasonics Sonochemistry</div>
    </div>

    <div class="pub-item">
      <div class="pub-badge">Q1 · IF 5.8 · 2021</div>
      <div class="pub-title">Size-controllable Zinc Oxide nanowires fabricated via the combination of die-casting and oxidation process</div>
      <div class="pub-meta"><strong>Vivekanandan AK</strong>, Azher K, Chang SF, Chen SH · Journal of Alloys and Compounds</div>
    </div>

  </div>
</section>

<!-- COLLABORATIONS -->
<section id="collaborations">
  <p class="section-label">Global Partnerships</p>
  <h2 class="section-title">Current Collaborations &amp; Projects</h2>
  <div class="collab-grid">
    <div class="collab-card">
      <div class="collab-icon">
        <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
      </div>
      <div>
        <div class="collab-year">2025 – 2026</div>
        <div class="collab-name">National Yang Ming Chiao Tung University, Taiwan</div>
        <div class="collab-desc">Process Optimization of Zinc Oxide Nanowire Fabrication Using Vacuum Die-Casting and Thermal Oxidation. Role: Data Curation and Original Draft Writing.</div>
      </div>
    </div>
    <div class="collab-card">
      <div class="collab-icon">
        <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
      </div>
      <div>
        <div class="collab-year">2024 – 2025</div>
        <div class="collab-name">National Taipei University of Technology, Taiwan</div>
        <div class="collab-desc">Investigating the effects of heat treatment on Nb₂O₅-reinforced Mg-3 wt% Al Alloy Matrix Composites. Role: Data Curation and Original Draft Writing.</div>
      </div>
    </div>
    <div class="collab-card">
      <div class="collab-icon">
        <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
      </div>
      <div>
        <div class="collab-year">Industrial Project · 2023–25</div>
        <div class="collab-name">Surface Engineering of Aerospace Aluminium Alloy</div>
        <div class="collab-desc">Enhanced corrosion protection via surface engineering — Annasaheb Dange College of Engineering and Technology, Maharashtra.</div>
      </div>
    </div>
    <div class="collab-card">
      <div class="collab-icon">
        <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>
      </div>
      <div>
        <div class="collab-year">Industrial Project · 2024–25 · KUB Industries, Pune</div>
        <div class="collab-name">Magnetic Foot Hexapod Robot</div>
        <div class="collab-desc">Designed and developed a Hexapod Robot with aluminum joints and 3D-printed foot attachments using tripod gait motion for chimney inspection on vertical surfaces.</div>
      </div>
    </div>
  </div>
</section>

<!-- ACHIEVEMENTS -->
<section id="achievements">
  <p class="section-label">Recognition</p>
  <h2 class="section-title">Achievements &amp; Honours</h2>
  <div class="achieve-grid">
    <div class="achieve-card">
      <div class="achieve-icon">🏆</div>
      <div class="achieve-title">Young Researcher of the Year (2020)</div>
      <div class="achieve-desc">Awarded by the Taiwan Tribology Society (TTS), Taiwan, for outstanding excellence in research and teaching contributions.</div>
    </div>
    <div class="achieve-card">
      <div class="achieve-icon">🎓</div>
      <div class="achieve-title">Full Scholarship Recipient</div>
      <div class="achieve-desc">Recipient of a full scholarship from National Taiwan University of Science and Technology for Ph.D. studies (2017–2021).</div>
    </div>
    <div class="achieve-card">
      <div class="achieve-icon">📝</div>
      <div class="achieve-title">Active Journal Reviewer</div>
      <div class="achieve-desc">Peer reviewer for Journal of Alloys and Compounds, Sensors and Actuators: B, and Electrochimica Acta.</div>
    </div>
  </div>
</section>

<!-- INVITED TALKS -->
<section id="talks" style="background:var(--section-bg);">
  <p class="section-label">Speaking Engagements</p>
  <h2 class="section-title">Invited Speaker</h2>
  <div class="talks-list">
    <div class="talk-card">
      <div class="talk-year">Apr 2023 · Coimbatore, India</div>
      <div class="talk-title">Futuristic Thermoelectric Materials</div>
      <div class="talk-venue">7th International Conference on Science, Engineering, and Technology (ICSET-22) — Nehru Institute of Engineering and Technology</div>
    </div>
    <div class="talk-card">
      <div class="talk-year">May 2022 · Salem, India</div>
      <div class="talk-title">Smart Materials in Thermoelectric Energy Harvesting</div>
      <div class="talk-venue">Mahindra International Lectures Series — Department of Aeronautical Engineering, Mahindra Engineering College</div>
    </div>
    <div class="talk-card">
      <div class="talk-year">Dec 2021 · Hyderabad, India</div>
      <div class="talk-title">Ultrasonic Assisted Manufacturing Process</div>
      <div class="talk-venue">Department of Mechanical Engineering — Vardhaman College of Engineering</div>
    </div>
  </div>
</section>

<!-- GALLERY -->
<section id="gallery">
  <p class="section-label">Visual Portfolio</p>
  <h2 class="section-title">Research &amp; Lab Gallery</h2>
  <p class="gallery-intro">Upload images from your research lab, conferences, fieldwork, and collaborations to enrich your portfolio.</p>
  <div class="gallery-grid" id="gallery-grid">
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div>
    <div class="footer-name">Dr. Vivekanandan A K</div>
    <div style="font-size:0.75rem;margin-top:0.3rem;">Materials Specialist · Nanotechnology Researcher</div>
  </div>
  <div class="footer-links">
    <a href="mailto:vivekak77@gmail.com">Email</a>
    <a href="https://linkedin.com/in/vivekanandan-ak" target="_blank">LinkedIn</a>
    <a href="https://scholar.google.com.tw/citations?user=urPd1vwAAAAJ&hl=en" target="_blank">Scholar</a>
  </div>
</footer>

<script>
  // Hero photo upload
  document.getElementById('hero-photo-input').addEventListener('change', function(e) {
    const file = e.target.files[0];
    if (!file) return;
    const url = URL.createObjectURL(file);
    const img = document.getElementById('hero-img');
    img.src = url;
    img.style.display = 'block';
    document.getElementById('hero-placeholder').style.display = 'none';
  });

  // About photo upload
  document.getElementById('about-photo-input').addEventListener('change', function(e) {
    const file = e.target.files[0];
    if (!file) return;
    const url = URL.createObjectURL(file);
    const img = document.getElementById('about-img');
    img.src = url;
    img.style.display = 'block';
    document.getElementById('about-placeholder').style.display = 'none';
  });

  // Gallery - generate 8 slots
  const galleryGrid = document.getElementById('gallery-grid');
  for (let i = 0; i < 8; i++) {
    const slot = document.createElement('div');
    slot.className = 'gallery-slot';
    slot.innerHTML = `
      <input type="file" accept="image/*" class="gallery-input" id="gallery-input-${i}">
      <img id="gallery-img-${i}" src="" alt="Gallery image">
      <div class="upload-hint">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#8A7B6E" stroke-width="1.5"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
        <span>Add Photo</span>
      </div>
    `;
    slot.addEventListener('click', () => {
      document.getElementById(`gallery-input-${i}`).click();
    });
    document.getElementById ? null : null;
    galleryGrid.appendChild(slot);

    const input = slot.querySelector(`#gallery-input-${i}`);
    input.addEventListener('change', function(e) {
      const file = e.target.files[0];
      if (!file) return;
      const url = URL.createObjectURL(file);
      const img = document.getElementById(`gallery-img-${i}`);
      img.src = url;
      slot.classList.add('has-image');
    });
  }

  // Smooth scroll active states
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-links a');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        navLinks.forEach(link => {
          link.style.color = link.getAttribute('href') === '#' + entry.target.id ? 'var(--accent)' : '';
        });
      }
    });
  }, { threshold: 0.4 });
  sections.forEach(s => observer.observe(s));
</script>
</body>
</html>
