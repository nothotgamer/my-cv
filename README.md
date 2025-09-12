<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Waleed Jamshaid — Website Developer</title>
  <meta name="description" content="Portfolio of Waleed Jamshaid, a skilled Website Developer specializing in frontend and full-stack development.">
  <meta name="keywords" content="Waleed Jamshaid, website developer, frontend, full-stack, React, Flutter, Node.js, portfolio">
  <meta name="author" content="Waleed Jamshaid">
  <link rel="icon" type="image/png" href="favicon.png">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0a1121;
      --card: #1f2937;
      --muted: #d1d5db;
      --accent: #22c55e;
      --accent-dark: #15803d;
      --glass: rgba(255,255,255,0.08);
      --max-width: 1280px;
      --radius: 20px;
      --shadow: 0 12px 48px rgba(0,0,0,0.25);
      font-family: 'Inter', system-ui, sans-serif;
      font-size: 16px;
      line-height: 1.6;
      transition: all 0.3s ease;
    }
    [data-theme="light"] {
      --bg: #f9fafb;
      --card: #ffffff;
      --muted: #4b5563;
      --glass: rgba(0,0,0,0.05);
      color: #1f2937;
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html, body {
      min-height: 100%;
      background: linear-gradient(180deg, var(--bg) 0%, #040b1b 100%);
      color: #f1f5f9;
      scroll-behavior: smooth;
    }
    [data-theme="light"] body {
      background: linear-gradient(180deg, #f9fafb 0%, #e5e7eb 100%);
    }
    a { color: inherit; text-decoration: none; transition: color 0.3s ease, transform 0.2s ease; }
    a:hover { color: var(--accent); transform: scale(1.05); }
    .container {
      max-width: var(--max-width);
      margin: 80px auto 32px; /* Adjusted for header clearance */
      padding: 0 20px;
    }
    .card {
      background: linear-gradient(180deg, var(--card), #111827);
      backdrop-filter: blur(12px);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 32px;
      animation: fadeIn 0.6s ease-out;
    }
    .card:hover {
      transform: translateY(-4px);
    }
    header {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 100;
      background: var(--card);
      padding: 12px 16px;
      border-radius: 0 0 var(--radius) var(--radius);
      display: flex;
      align-items: center;
      justify-content: space-between;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
      transition: padding 0.3s ease, background 0.3s ease;
    }
    header.scrolled {
      padding: 8px 16px;
    }
    .header-content {
      display: flex;
      align-items: center;
      gap: 12px;
      flex: 1;
      overflow: hidden;
    }
    .avatar {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--accent), #10b981);
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 700;
      font-size: 24px;
      color: #052e16;
      box-shadow: 0 4px 16px rgba(0,0,0,0.3);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      flex-shrink: 0;
    }
    .avatar:hover {
      transform: scale(1.1);
      box-shadow: 0 8px 24px rgba(0,0,0,0.4);
    }
    h1 {
      font-size: 28px;
      font-weight: 800;
      letter-spacing: -0.025em;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }
    p.lead {
      margin: 4px 0 0;
      color: var(--muted);
      font-size: 16px;
      font-weight: 400;
    }
    .grid {
      display: grid;
      grid-template-columns: 320px 1fr;
      gap: 28px;
      margin-top: 32px;
    }
    nav.section {
      position: relative;
      padding-right: 20px;
      height: fit-content;
    }
    .section h3 {
      margin: 0 0 16px;
      color: var(--accent);
      font-size: 18px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.05em;
    }
    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }
    .skill {
      background: var(--glass);
      padding: 8px 14px;
      border-radius: 8px;
      font-size: 14px;
      color: var(--muted);
      transition: all 0.3s ease;
    }
    .skill:hover {
      background: rgba(34,197,94,0.15);
      transform: translateY(-2px);
      color: var(--accent);
    }
    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 16px;
    }
    .proj {
      background: linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.02));
      padding: 20px;
      border-radius: 12px;
      transition: all 0.3s ease;
    }
    .proj:hover {
      transform: translateY(-4px);
      box-shadow: 0 8px 24px rgba(0,0,0,0.25);
    }
    .proj strong {
      font-size: 20px;
      font-weight: 700;
    }
    .btn {
      display: inline-flex;
      gap: 8px;
      align-items: center;
      background: var(--accent);
      color: #052e16;
      padding: 10px 16px;
      border-radius: 10px;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.3s ease;
    }
    .btn:hover {
      background: var(--accent-dark);
      transform: translateY(-2px);
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
    }
    .btn.secondary {
      background: transparent;
      border: 1px solid var(--muted);
      color: var(--muted);
    }
    .btn.secondary:hover {
      background: rgba(255,255,255,0.1);
      color: var(--accent);
    }
    .theme-toggle {
      background: var(--glass);
      border: none;
      padding: 8px;
      border-radius: 8px;
      cursor: pointer;
      color: var(--muted);
      transition: all 0.3s ease;
    }
    .theme-toggle:hover {
      background: rgba(34,197,94,0.15);
      color: var(--accent);
    }
    .hamburger {
      display: none;
      background: none;
      border: none;
      font-size: 20px;
      color: var(--muted);
      cursor: pointer;
      padding: 4px;
    }
    .nav-menu {
      display: flex;
      gap: 12px;
      align-items: center;
    }
    .nav-menu.active {
      display: flex;
      flex-direction: column;
      position: absolute;
      top: 100%;
      right: 16px;
      background: var(--card);
      padding: 12px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      z-index: 99;
      width: 200px;
    }
    .back-to-top {
      position: fixed;
      bottom: 24px;
      right: 24px;
      background: var(--accent);
      color: #052e16;
      padding: 10px;
      border-radius: 50%;
      display: none;
      align-items: center;
      justify-content: center;
      box-shadow: var(--shadow);
      transition: all 0.3s ease;
    }
    .back-to-top.show {
      display: flex;
    }
    footer {
      margin-top: 48px;
      text-align: center;
      color: var(--muted);
      font-size: 14px;
      opacity: 0.9;
    }
    .social-links {
      display: flex;
      gap: 16px;
      justify-content: center;
      margin-top: 16px;
    }
    .social-links a {
      font-size: 24px;
      color: var(--muted);
      transition: color 0.3s ease, transform 0.3s ease;
    }
    .social-links a:hover {
      color: var(--accent);
      transform: scale(1.2);
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .fade-in {
      animation: fadeIn 0.6s ease-out;
    }
    a:focus, .btn:focus, .theme-toggle:focus, .hamburger:focus {
      outline: 3px solid var(--accent);
      outline-offset: 3px;
    }
    @media (max-width: 1024px) {
      .grid { grid-template-columns: 1fr; gap: 24px; }
      nav.section { position: static; padding-right: 0; }
      .projects { grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); }
      .container { margin-top: 100px; }
    }
    @media (max-width: 768px) {
      .grid { grid-template-columns: 1fr; gap: 20px; }
      nav.section { position: static; padding-right: 0; }
      .projects { grid-template-columns: 1fr; }
      .avatar { width: 56px; height: 56px; font-size: 20px; }
      h1 { font-size: 24px; }
      p.lead { font-size: 14px; }
      .btn { padding: 8px 14px; font-size: 14px; }
      .container { margin-top: 80px; }
    }
    @media (max-width: 600px) {
      .container { padding: 0 12px; margin: 70px auto 20px; }
      .card { padding: 20px; border-radius: 12px; }
      header { flex-direction: row; align-items: center; padding: 8px 12px; }
      .header-content { text-align: left; max-width: 60%; }
      .nav-menu { display: none; }
      .nav-menu.active { display: flex; }
      .hamburger { display: block; }
      .btn-group { flex-direction: column; align-items: flex-start; }
      .back-to-top { bottom: 16px; right: 16px; padding: 8px; }
      .skills { justify-content: center; }
      .avatar { width: 48px; height: 48px; font-size: 18px; }
      h1 { font-size: 22px; }
      p.lead { font-size: 13px; }
      .muted { font-size: 13px; }
      .proj strong { font-size: 18px; }
    }
    @media (max-width: 480px) {
      .container { padding: 0 10px; margin: 60px auto 16px; }
      .card { padding: 16px; border-radius: 10px; }
      .avatar { width: 40px; height: 40px; font-size: 16px; }
      h1 { font-size: 20px; }
      p.lead { font-size: 12px; }
      .skills { gap: 6px; }
      .skill { padding: 6px 10px; font-size: 12px; }
      .btn { padding: 6px 12px; font-size: 12px; }
      .projects { gap: 10px; }
      .proj { padding: 14px; }
      .nav-menu { width: 180px; }
      .hamburger { font-size: 18px; }
    }
    @media print {
      body { background: white; color: black; }
      .card, header { box-shadow: none; background: white; }
      .btn, footer, .theme-toggle, .back-to-top, .hamburger { display: none; }
      .avatar { background: #22c55e; }
      .nav-menu { display: flex; }
      .container { margin-top: 0; }
    }
  </style>
</head>
<body>
  <header id="header">
    <div class="header-content">
      <div class="avatar">WJ</div>
      <div>
        <h1>Waleed Jamshaid</h1>
        <p class="lead">Website Developer • Frontend & Full-stack • React / Flutter Web / Node.js</p>
        <p class="muted">📍 Sialkot, Pakistan • 📞 +92 3247264682 • ✉️ <a href="mailto:waleedjamshaidmehar@gmail.com">waleedjamshaidmehar@gmail.com</a></p>
      </div>
    </div>
    <button class="hamburger" aria-label="Toggle Menu">☰</button>
    <div class="nav-menu btn-group">
      <a class="btn" href="#contact">Contact</a>
      <a class="btn secondary" href="resume.pdf" download>Download CV</a>
      <button class="theme-toggle" onclick="toggleTheme()" aria-label="Toggle Theme">🌙</button>
    </div>
  </header>
  <div class="container">
    <div class="card fade-in">
      <div class="grid">
        <nav class="section">
          <div style="margin-top: 24px;">
            <h3>Skills</h3>
            <div class="skills">
              <div class="skill">HTML5</div>
              <div class="skill">CSS3</div>
              <div class="skill">JavaScript (ES6+)</div>
              <div class="skill">React.js</div>
              <div class="skill">Flutter Web</div>
              <div class="skill">Node.js</div>
              <div class="skill">Firebase</div>
              <div class="skill">TailwindCSS</div>
              <div class="skill">SEO</div>
              <div class="skill">Responsive Design</div>
              <div class="skill">TypeScript</div>
            </div>
          </div>
          <div style="margin-top: 24px;">
            <h3>Tools</h3>
            <div class="skills">
              <div class="skill">Git / GitHub</div>
              <div class="skill">VS Code</div>
              <div class="skill">Figma</div>
              <div class="skill">Postman</div>
              <div class="skill">Firebase Emulator</div>
              <div class="skill">Vite</div>
            </div>
          </div>
          <div style="margin-top: 24px;">
            <h3>Education</h3>
            <div class="muted">Intermediate in Computer Science (Physics) • Punjab College, Sialkot • 2022–2024</div>
          </div>
          <div style="margin-top: 24px;">
            <h3>Languages</h3>
            <div class="muted">English (Fluent), Urdu (Native), Punjabi (Fluent)</div>
          </div>
        </nav>
        <main class="section">
          <section id="summary" class="fade-in">
            <h3>Professional Summary</h3>
            <p class="muted">Aspiring Website Developer, 19 years old, with hands-on experience building self-made responsive and accessible web applications. Self-taught proficient in frontend frameworks like React and Flutter Web, with skills in full-stack development using Node.js and Firebase. Passionate about performance optimization, clean code, and delivering delightful UI/UX experiences through personal projects.</p>
          </section>
          <section id="projects" style="margin-top: 24px;" class="fade-in">
            <h3>Self-Made Projects</h3>
            <div class="projects">
              <div class="proj">
                <strong>Cheezon — Classifieds App</strong>
                <div class="muted">Flutter Web • Firebase • Node.js • 2024</div>
                <p class="muted">Built a full-featured classifieds platform with dynamic categories, real-time chat, and an admin panel for content moderation. Optimized for mobile and desktop with SEO-friendly URLs. <a href="https://cheezon.app" target="_blank" rel="noopener noreferrer">Live Demo</a></p>
              </div>
              <div class="proj">
                <strong>Portfolio Website</strong>
                <div class="muted">HTML/CSS • React • Vite • 2024</div>
                <p class="muted">Designed and built a personal portfolio with a focus on SEO, performance (Lighthouse score: 95+), and accessibility. Features dark/light mode and smooth animations. <a href="https://waleedjamshaid.dev" target="_blank" rel="noopener noreferrer">Live Demo</a></p>
              </div>
              <div class="proj">
                <strong>E-commerce Store</strong>
                <div class="muted">React • Firebase • Stripe • 2023</div>
                <p class="muted">Developed a fully functional e-commerce store with shopping cart, Stripe payments, and order management. Implemented real-time inventory updates using Firebase. <a href="https://github.com/waleedjamshaid/ecommerce" target="_blank" rel="noopener noreferrer">GitHub</a></p>
              </div>
            </div>
          </section>
          <section style="margin-top: 24px;" id="contact" class="fade-in">
            <h3>Contact</h3>
            <p class="muted">Interested in collaborating? Reach out to discuss opportunities or projects. I respond within 24 hours. Email me at <a href="mailto:waleedjamshaidmehar@gmail.com">waleedjamshaidmehar@gmail.com</a>.</p>
            <p style="margin-top: 16px;"><a class="btn" href="mailto:waleedjamshaidmehar@gmail.com">Email Me</a></p>
          </section>
        </main>
      </div>
      <footer>
        Designed & built by Waleed Jamshaid • Available for freelance or full-time roles
        <div class="social-links">
          <a href="https://linkedin.com/in/waleedjamshaid" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">LinkedIn</a>
          <a href="https://github.com/waleedjamshaid" target="_blank" rel="noopener noreferrer" aria-label="GitHub">GitHub</a>
          <a href="https://x.com/waleedjamshaid" target="_blank" rel="noopener noreferrer" aria-label="X">X</a>
        </div>
      </footer>
    </div>
    <a href="#" class="back-to-top" id="backToTop" title="Back to Top" aria-label="Back to Top">↑</a>
  </div>
  <noscript>
    <style>
      .nav-menu { display: flex; }
      .hamburger { display: none; }
    </style>
  </noscript>
  <script>
    // Theme toggle
    function toggleTheme() {
      const html = document.documentElement;
      const currentTheme = html.getAttribute('data-theme') === 'light' ? 'dark' : 'light';
      html.setAttribute('data-theme', currentTheme);
      localStorage.setItem('theme', currentTheme);
    }
    // Load saved theme
    const savedTheme = localStorage.getItem('theme') || 'dark';
    document.documentElement.setAttribute('data-theme', savedTheme);
    // Hamburger menu toggle
    const hamburger = document.querySelector('.hamburger');
    const navMenu = document.querySelector('.nav-menu');
    hamburger.addEventListener('click', () => {
      navMenu.classList.toggle('active');
    });
    // Close menu when clicking outside
    document.addEventListener('click', (e) => {
      if (!navMenu.contains(e.target) && !hamburger.contains(e.target)) {
        navMenu.classList.remove('active');
      }
    });
    // Shrink header on scroll
    const header = document.getElementById('header');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 50) {
        header.classList.add('scrolled');
      } else {
        header.classList.remove('scrolled');
      }
    });
    // Back to top button
    const backToTop = document.getElementById('backToTop');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 300) {
        backToTop.classList.add('show');
      } else {
        backToTop.classList.remove('show');
      }
    });
    backToTop.addEventListener('click', (e) => {
      e.preventDefault();
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });
    // Fade-in on scroll
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('fade-in');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.2 });
    document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
  </script>
</body>
</html>
