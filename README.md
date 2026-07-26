
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aye Mon San | Portfolio Website</title>
  
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
  
  <style>
    :root {
      --primary: #1E40AF;           /* Professional Royal Blue */
      --primary-hover: #1D4ED8;
      --primary-light: #EFF6FF;     /* Soft Light Blue Tint */
      --primary-gradient: linear-gradient(135deg, #1E40AF 0%, #3B82F6 100%);
      --text-dark: #101828;         /* Crisp Dark Text */
      --text-muted: #475467;        /* Soft Charcoal Secondary Text */
      --bg-outer: #D3D3D3;          /* Light Gray Canvas */
      --card-bg: #ffffff;           /* Main Card Background */
      --border-color: #EAECF0;
      --shadow-sm: 0 4px 15px rgba(30, 64, 175, 0.05);
      --shadow-md: 0 10px 25px rgba(30, 64, 175, 0.15);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background-color: var(--bg-outer);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 40px 20px;
    }

    /* Main Canvas Wrapper */
    .app-container {
      width: 100%;
      max-width: 1200px;
      background: var(--card-bg);
      border-radius: 40px;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
      padding: 40px 60px 60px 60px;
      position: relative;
    }

    /* Sticky Navigation Bar */
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 40px;
      position: sticky;
      top: 0;
      background: #ffffff;
      z-index: 100;
      padding: 10px 0;
    }

    .logo {
      display: flex;
      align-items: center;
      font-weight: 700;
      font-size: 1.5em;
      color: var(--text-dark);
      gap: 8px;
    }

    .logo-icon {
      background: var(--primary-gradient);
      color: #fff;
      width: 34px;
      height: 34px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.8em;
    }

    .logo span {
      color: var(--primary);
    }

    .nav-links {
      display: flex;
      align-items: center;
      list-style: none;
      gap: 4px;
      background: #fdfdfd;
      padding: 6px 12px;
      border-radius: 30px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.02);
      border: 1px solid var(--border-color);
      overflow-x: auto;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text-muted);
      font-size: 0.85em;
      font-weight: 500;
      padding: 6px 14px;
      border-radius: 20px;
      transition: all 0.2s ease;
      white-space: nowrap;
    }

    .nav-links a:hover, .nav-links a.active {
      color: var(--primary);
      background: var(--primary-light);
    }

    .btn-contact-nav {
      background: var(--primary-gradient);
      color: #fff;
      padding: 12px 28px;
      border-radius: 14px;
      font-weight: 500;
      text-decoration: none;
      font-size: 0.9em;
      box-shadow: 0 10px 20px rgba(30, 64, 175, 0.25);
    }

    /* Section Containers */
    .content-section {
      padding: 70px 0 30px 0;
      border-bottom: 1px solid var(--border-color);
    }

    .content-section:last-of-type {
      border-bottom: none;
    }

    .section-headline {
      font-size: 2em;
      font-weight: 700;
      color: var(--text-dark);
      margin-bottom: 30px;
      position: relative;
      display: inline-block;
    }

    .section-headline::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -6px;
      width: 40px;
      height: 4px;
      background: var(--primary);
      border-radius: 2px;
    }

    /* HERO SECTION */
    .hero-layout {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      align-items: center;
      gap: 40px;
      padding-top: 20px;
    }

    .hero-content {
      max-width: 540px;
    }

    .accent-line {
      width: 50px;
      height: 4px;
      background: var(--primary-gradient);
      margin-bottom: 24px;
      border-radius: 2px;
    }

    .hero-content h1 {
      font-size: 3.2em;
      font-weight: 700;
      color: var(--text-dark);
      line-height: 1.15;
      margin-bottom: 8px;
      letter-spacing: -1px;
    }

    .hero-content h1 span {
      color: var(--primary);
    }

    .hero-tagline {
      font-size: 0.9em;
      color: var(--primary);
      font-weight: 600;
      letter-spacing: 0.5px;
      margin-bottom: 24px;
      text-transform: uppercase;
    }

    .hero-content p {
      color: var(--text-muted);
      font-size: 1.05em;
      line-height: 1.6;
      margin-bottom: 40px;
    }

    .cta-group {
      display: flex;
      gap: 20px;
    }

    .btn-primary, .btn-secondary {
      padding: 16px 36px;
      border-radius: 16px;
      font-weight: 600;
      text-decoration: none;
      font-size: 0.95em;
      transition: transform 0.2s, box-shadow 0.2s;
      display: inline-block;
    }

    .btn-primary {
      background: var(--primary-gradient);
      color: #fff;
      box-shadow: 0 12px 24px rgba(30, 64, 175, 0.3);
    }

    .btn-secondary {
      background: #ffffff;
      color: var(--primary);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.04);
      border: 1px solid rgba(30, 64, 175, 0.15);
    }

    .btn-primary:hover, .btn-secondary:hover {
      transform: translateY(-2px);
    }

    /* ELEGANT PORTRAIT FRAME */
    .hero-visual {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .profile-frame-container {
      position: relative;
      width: 340px;
      height: 410px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .glow-backdrop {
      position: absolute;
      width: 320px;
      height: 380px;
      background: linear-gradient(135deg, rgba(30, 64, 175, 0.25), rgba(59, 130, 246, 0.15));
      border-radius: 170px 170px 50px 50px;
      filter: blur(20px);
      z-index: 0;
      transform: translateY(10px);
    }

    .arch-gradient-frame {
      position: relative;
      z-index: 1;
      width: 310px;
      height: 380px;
      border-radius: 160px 160px 40px 40px;
      padding: 5px;
      background: linear-gradient(135deg, #1E40AF 0%, #06B6D4 100%);
      box-shadow: 0 20px 40px rgba(30, 64, 175, 0.18);
    }

    .photo-inner-card {
      width: 100%;
      height: 100%;
      border-radius: 155px 160px 35px 35px;
      overflow: hidden;
      background: #f8f9fa;
    }

    .photo-inner-card img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: top center;
      display: block;
      transition: transform 0.4s ease;
    }

    .arch-gradient-frame:hover .photo-inner-card img {
      transform: scale(1.03);
    }

    .floating-badge {
      position: absolute;
      z-index: 3;
      background: #ffffff;
      padding: 10px 18px;
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 0.82em;
      font-weight: 600;
      color: var(--text-dark);
      border: 1px solid rgba(30, 64, 175, 0.12);
    }

    .badge-top-right {
      top: 15px;
      right: -15px;
      animation: floatSmooth 4s ease-in-out infinite alternate;
    }

    .badge-bottom-left {
      bottom: 20px;
      left: -20px;
      animation: floatSmooth 4s ease-in-out infinite alternate-reverse;
    }

    @keyframes floatSmooth {
      0% { transform: translateY(0px); }
      100% { transform: translateY(-8px); }
    }

    /* ABOUT ME & LANGUAGES */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
    }

    .about-details {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
      background: #f8fafc;
      padding: 30px;
      border-radius: 24px;
    }

    .about-meta-box h4 {
      font-size: 0.85em;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--text-muted);
      margin-bottom: 4px;
    }

    .about-meta-box p {
      color: var(--text-dark);
      font-weight: 600;
    }

    /* SKILLS & PROGRESS BARS */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 24px;
    }

    .skills-category {
      background: #f8fafc;
      padding: 28px;
      border-radius: 20px;
      border: 1px solid var(--border-color);
    }

    .skills-category h4 {
      font-size: 1.1em;
      color: var(--text-dark);
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .skill-item {
      margin-bottom: 16px;
    }

    .skill-info {
      display: flex;
      justify-content: space-between;
      margin-bottom: 6px;
      font-size: 0.9em;
      font-weight: 500;
    }

    .progress-bar {
      width: 100%;
      height: 8px;
      background: var(--border-color);
      border-radius: 4px;
      overflow: hidden;
    }

    .progress {
      height: 100%;
      background: var(--primary-gradient);
      border-radius: 4px;
    }

    .skills-flex {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 15px;
    }

    .skill-pill {
      background: var(--primary-light);
      color: var(--primary);
      padding: 8px 16px;
      border-radius: 20px;
      font-size: 0.9em;
      font-weight: 500;
    }

    /* TIMELINES & GRIDS */
    .timeline-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 24px;
    }

    .timeline-card {
      background: #ffffff;
      border: 1px solid var(--border-color);
      padding: 30px;
      border-radius: 24px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.01);
      transition: all 0.3s ease;
    }

    .timeline-card:hover {
      transform: translateY(-5px);
      border-color: var(--primary);
      box-shadow: 0 15px 30px rgba(30, 64, 175, 0.08);
    }

    .card-date-badge {
      display: inline-block;
      background: var(--primary-light);
      color: var(--primary);
      font-size: 0.8em;
      font-weight: 600;
      padding: 4px 12px;
      border-radius: 12px;
      margin-bottom: 16px;
    }

    .card-headline {
      font-size: 1.25em;
      font-weight: 700;
      color: var(--text-dark);
      margin-bottom: 4px;
    }

    .card-subheadline {
      font-size: 0.95em;
      font-weight: 600;
      color: var(--text-muted);
      margin-bottom: 16px;
    }

    .card-bullet-list {
      padding-left: 18px;
      color: var(--text-muted);
      font-size: 0.9em;
    }

    .card-bullet-list li {
      margin-bottom: 8px;
    }

    /* CERTIFICATIONS & ACHIEVEMENTS */
    .cert-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 16px;
    }

    .cert-card {
      background: #f8fafc;
      border: 1px solid var(--border-color);
      padding: 20px;
      border-radius: 16px;
      font-size: 0.9em;
      color: var(--text-dark);
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 12px;
      transition: all 0.2s;
    }

    .cert-card:hover {
      border-color: var(--primary);
      background: var(--primary-light);
      color: var(--primary);
    }

    .cert-icon {
      background: #ffffff;
      width: 36px;
      height: 36px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.03);
      color: var(--primary);
    }

    /* SHOWCASE GRID & FILTER SYSTEM */
    .portfolio-filters {
      display: flex;
      justify-content: center;
      gap: 12px;
      margin-bottom: 30px;
      flex-wrap: wrap;
    }

    .filter-btn {
      background: transparent;
      border: 1px solid var(--border-color);
      color: var(--text-muted);
      padding: 8px 22px;
      border-radius: 25px;
      font-weight: 500;
      font-size: 0.9em;
      cursor: pointer;
      transition: all 0.25s ease;
    }

    .filter-btn.active, .filter-btn:hover {
      background: var(--primary-gradient);
      color: white;
      border-color: transparent;
      box-shadow: 0 6px 15px rgba(30, 64, 175, 0.2);
    }

    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 25px;
    }

    .portfolio-item {
      position: relative;
      border-radius: 20px;
      overflow: hidden;
      cursor: pointer;
      border: 1px solid var(--border-color);
      aspect-ratio: 4 / 3;
      background: #f8fafc;
      transition: transform 0.3s ease;
    }

    .portfolio-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      transition: transform 0.4s ease;
    }

    .portfolio-item:hover img {
      transform: scale(1.05);
    }

    .portfolio-overlay {
      position: absolute;
      inset: 0;
      background: linear-gradient(to top, rgba(16, 24, 40, 0.9) 10%, rgba(16, 24, 40, 0.2) 60%, transparent);
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      padding: 22px;
      color: white;
      opacity: 0;
      transition: opacity 0.3s ease;
    }

    .portfolio-item:hover .portfolio-overlay {
      opacity: 1;
    }

    .portfolio-overlay h4 {
      font-size: 1.15em;
      font-weight: 600;
      margin-bottom: 4px;
    }

    .portfolio-overlay p {
      font-size: 0.85em;
      opacity: 0.9;
    }

    /* MODAL POPUP ENGINE */
    .modal-overlay {
      position: fixed;
      inset: 0;
      background: rgba(16, 24, 40, 0.7);
      backdrop-filter: blur(6px);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 1000;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s ease;
      padding: 20px;
    }

    .modal-overlay.active {
      opacity: 1;
      pointer-events: auto;
    }

    .modal-card {
      background: #ffffff;
      border-radius: 28px;
      padding: 35px;
      width: 100%;
      max-width: 650px;
      position: relative;
      box-shadow: 0 25px 50px rgba(0, 0, 0, 0.2);
    }

    .close-modal {
      position: absolute;
      top: 20px;
      right: 25px;
      font-size: 1.6em;
      cursor: pointer;
      color: var(--text-muted);
      transition: color 0.2s;
    }

    .close-modal:hover {
      color: var(--primary);
    }

    /* CONNECT WITH ME */
    .contact-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 20px;
    }

    .contact-card {
      background: #f8fafc;
      border: 1px solid var(--border-color);
      border-radius: 20px;
      padding: 24px;
      text-decoration: none;
      color: var(--text-dark);
      transition: all 0.3s ease;
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .contact-card:hover {
      border-color: var(--primary);
      transform: translateY(-3px);
      box-shadow: 0 10px 20px rgba(30, 64, 175, 0.05);
    }

    .contact-card .icon {
      font-size: 1.5em;
    }

    .contact-card h4 {
      font-size: 0.9em;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      color: var(--text-muted);
    }

    .contact-card p {
      font-weight: 600;
      color: var(--primary);
      word-break: break-all;
    }

    footer {
      text-align: center;
      margin-top: 60px;
      padding-top: 30px;
      border-top: 1px solid var(--border-color);
      font-size: 0.85em;
      color: var(--text-muted);
    }

    /* RESPONSIVE LAYOUT */
    @media (max-width: 992px) {
      .app-container {
        padding: 30px;
      }
      .nav-links {
        display: none; 
      }
      .hero-layout {
        grid-template-columns: 1fr;
        text-align: center;
      }
      .accent-line {
        margin: 0 auto 24px auto;
      }
      .hero-content {
        margin: 0 auto;
        order: 2;
      }
      .hero-visual {
        order: 1;
        margin-bottom: 20px;
      }
      .cta-group {
        justify-content: center;
      }
      .about-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <div class="app-container">
    
    <!-- NAVIGATION BAR -->
    <nav>
      <div class="logo">
        <div class="logo-icon">A</div>
        Aye Mon San<span>.</span>
      </div>
      
      <ul class="nav-links">
        <li><a href="#about" class="active">About Me</a></li>
        <li><a href="#qualifications">Qualifications</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#certifications">Certifications</a></li>
        <li><a href="#portfolio">Showcase</a></li>
      </ul>

      <a href="#connect" class="btn-contact-nav">Connect</a>
    </nav>

    <!-- HERO SECTION -->
    <section class="content-section hero-layout" id="home" style="padding-top: 0;">
      <div class="hero-content">
        <div class="accent-line"></div>
        <h1>I'm <span>Aye Mon San</span>,<br>an <span>English Instructor</span></h1>
        <div class="hero-tagline">English Instructor | TEFL Certified | Passionate Educator</div>
        <p>
          Passionate about creating inclusive and engaging learning environments where students can develop strong English communication skills while building cultural awareness and confidence.
        </p>
        <div class="cta-group">
          <a href="#connect" class="btn-primary">Connect with Me</a>
          <a href="#portfolio" class="btn-secondary">Portfolio Showcase</a>
        </div>
      </div>

      <!-- PORTRAIT FRAME -->
      <div class="hero-visual">
        <div class="profile-frame-container">
          <div class="glow-backdrop"></div>
          
          <div class="arch-gradient-frame">
            <div class="photo-inner-card">
              <img src="profile.jpeg" alt="Aye Mon San Portrait" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'500\' height=\'600\' viewBox=\'0 0 500 600\'><rect width=\'500\' height=\'600\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'24\' fill=\'%231E40AF\'>Aye Mon San</text></svg>';">
            </div>
          </div>

          <div class="floating-badge badge-top-right">
            <span>🎓</span> TEFL Certified
          </div>
          <div class="floating-badge badge-bottom-left">
            <span>✨</span> English Educator
          </div>
        </div>
      </div>
    </section>

    <!-- ABOUT ME -->
    <section class="content-section" id="about">
      <h3 class="section-headline">About Me</h3>
      <div class="about-grid" style="margin-top: 20px;">
        <div>
          <p style="color: var(--text-muted); line-height: 1.7; margin-bottom: 20px; text-align: justify;">
            I am a passionate English instructor and English Communication student with experience in online teaching, tutoring, and community education. I enjoy helping learners build confidence in English through engaging, student-centered lessons while promoting intercultural understanding and lifelong learning.
          </p>
        </div>
        
        <div class="about-details">
          <div class="about-meta-box"><h4>Nationality</h4><p>Myanmar</p></div>
          <div class="about-meta-box"><h4>Age / Gender</h4><p>27 / Female</p></div>
          <div class="about-meta-box"><h4>Current Base</h4><p>Chiang Mai, Thailand</p></div>
          <div class="about-meta-box"><h4>Status</h4><p>Open to Opportunities</p></div>
        </div>
      </div>
    </section>

    <!-- QUALIFICATIONS -->
    <section class="content-section" id="qualifications">
      <h3 class="section-headline">Qualifications</h3>
      <div class="timeline-grid" style="margin-top: 20px;">
        <div class="timeline-card">
          <span class="card-date-badge">2024 – Present</span>
          <h4 class="card-headline">B.A. in English Communication Arts</h4>
          <p class="card-subheadline">Payap University</p>
        </div>

        <div class="timeline-card">
          <span class="card-date-badge">2021 – 2024</span>
          <h4 class="card-headline">Associate Degree in Mass Media & Journalism</h4>
          <p class="card-subheadline">Mon National College</p>
        </div>

        <div class="timeline-card">
          <span class="card-date-badge">2018 – 2019</span>
          <h4 class="card-headline">B.A. in English</h4>
          <p class="card-subheadline">Hpa-An Distance University</p>
        </div>
      </div>
    </section>

    <!-- EXPERIENCE -->
    <section class="content-section" id="experience">
      <h3 class="section-headline">Professional Experience</h3>
      <div class="timeline-grid" style="margin-top: 20px;">
        <div class="timeline-card">
          <span class="card-date-badge">2025 – 2026</span>
          <h4 class="card-headline">General English Teacher</h4>
          <p class="card-subheadline">Poy English Program (Online)</p>
          <ul class="card-bullet-list">
            <li>Delivered engaging online English lessons in a supportive learning environment.</li>
            <li>Designed interactive lessons focusing on practical communication, grammar, and pronunciation.</li>
          </ul>
        </div>

        <div class="timeline-card">
          <span class="card-date-badge">Sep 2024 – Jul 2025</span>
          <h4 class="card-headline">Freelance English Tutor</h4>
          <p class="card-subheadline">Online Marketplace</p>
          <ul class="card-bullet-list">
            <li>Delivered personalized one-on-one and small-group English lessons to diverse learners.</li>
            <li>Helped students improve speaking fluency, pronunciation, and vocabulary.</li>
          </ul>
        </div>

        <div class="timeline-card">
          <span class="card-date-badge">Jan 2025</span>
          <h4 class="card-headline">Volunteer Teacher</h4>
          <p class="card-subheadline">Chiang Rai Kindergarten</p>
          <ul class="card-bullet-list">
            <li>Supported English learning through interactive games and creative lessons.</li>
            <li>Organized educational activities to encourage active student participation.</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- SKILLS & LANGUAGES -->
    <section class="content-section" id="skills">
      <h3 class="section-headline">Skills & Languages</h3>
      
      <div class="skills-grid" style="margin-top: 20px;">
        <!-- Languages Proficiency -->
        <div class="skills-category">
          <h4><i class="fa-solid fa-globe" style="color: var(--primary);"></i> Language Proficiency</h4>
          
          <div class="skill-item">
            <div class="skill-info"><span>Mon</span><span>Native</span></div>
            <div class="progress-bar"><div class="progress" style="width: 100%;"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-info"><span>Burmese</span><span>Bilingual</span></div>
            <div class="progress-bar"><div class="progress" style="width: 100%;"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-info"><span>English</span><span>C1 / Professional</span></div>
            <div class="progress-bar"><div class="progress" style="width: 90%;"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-info"><span>Thai</span><span>Conversational</span></div>
            <div class="progress-bar"><div class="progress" style="width: 60%;"></div></div>
          </div>
        </div>

        <!-- Instructional Skills -->
        <div class="skills-category">
          <h4><i class="fa-solid fa-chalkboard-user" style="color: var(--primary);"></i> Pedagogical Expertise</h4>
          <div class="skills-flex">
            <span class="skill-pill">Classroom Management</span>
            <span class="skill-pill">Lesson Planning</span>
            <span class="skill-pill">Curriculum Design</span>
            <span class="skill-pill">Public Speaking</span>
            <span class="skill-pill">Cross-Cultural Communication</span>
            <span class="skill-pill">Active Listening</span>
            <span class="skill-pill">Online Teaching Tools</span>
            <span class="skill-pill">Student Assessment</span>
          </div>
        </div>
      </div>
    </section>

    <!-- CERTIFICATIONS -->
    <section class="content-section" id="certifications">
      <h3 class="section-headline">Certifications</h3>
      <div class="cert-grid" style="margin-top: 20px;">
        <div class="cert-card"><div class="cert-icon"><i class="fa-solid fa-graduation-cap"></i></div> TEFL Certification</div>
        <div class="cert-card"><div class="cert-icon"><i class="fa-solid fa-certificate"></i></div> English for Career Development</div>
        <div class="cert-card"><div class="cert-icon"><i class="fa-solid fa-certificate"></i></div> Teaching English in Primary Education</div>
        <div class="cert-card"><div class="cert-icon"><i class="fa-solid fa-certificate"></i></div> Supporting Learning in Primary Education</div>
        <div class="cert-card"><div class="cert-icon"><i class="fa-solid fa-certificate"></i></div> Teaching English to Refugees</div>
        <div class="cert-card"><div class="cert-icon"><i class="fa-solid fa-certificate"></i></div> Supporting Children's Mental Health</div>
      </div>
    </section>

    <!-- PORTFOLIO SHOWCASE -->
    <section class="content-section" id="portfolio">
      <h3 class="section-headline">Portfolio Showcase</h3>
      <p style="color: var(--text-muted); margin-bottom: 25px;">Explore my teaching modules, class materials, and community projects below:</p>
      
      <!-- Filter Category Buttons -->
      <div class="portfolio-filters">
        <button class="filter-btn active" data-filter="all">All Projects</button>
        <button class="filter-btn" data-filter="teaching">Teaching & Classes</button>
        <button class="filter-btn" data-filter="volunteering">Volunteering & Projects</button>
      </div>

      <!-- Showcase Cards Grid -->
      <div class="portfolio-grid">
        
        <!-- CARD 1 -->
        <div class="portfolio-item" data-category="teaching" onclick="openModal('modal-p1')">
          <img src="1p.jpg" alt="Online Teaching Module" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Interactive English Modules</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Interactive English Modules</h4>
            <p>Teaching & Classes • Video & Lesson Logs</p>
          </div>
        </div>

        <!-- CARD 2 -->
        <div class="portfolio-item" data-category="teaching" onclick="openModal('modal-p2')">
          <img src="2p.jpg" alt="Poy English Program Delivery" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Poy English Program</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Poy English Program Delivery</h4>
            <p>Teaching & Classes • Conversational Fluency</p>
          </div>
        </div>

        <!-- CARD 3 -->
        <div class="portfolio-item" data-category="volunteering" onclick="openModal('modal-p3')">
          <img src="3p.jpg" alt="Chiang Rai Kindergarten Volunteer" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Volunteer Language Workshops</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Volunteer Language Workshops</h4>
            <p>Volunteering & Projects • Chiang Rai Kindergarten</p>
          </div>
        </div>

      </div>
    </section>

    <!-- MODAL POPUPS -->
    <div id="modal-p1" class="modal-overlay" onclick="closeModal('modal-p1')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p1')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Interactive English Modules</h3>
        
        <video controls style="width: 100%; border-radius: 16px; background: #000; margin-bottom: 15px;">
          <source src="1vp.mp4" type="video/mp4">
          Your browser does not support HTML video playback.
        </video>
        
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Designed engaging online modules focusing on practical everyday conversational English, vocabulary expansion, and student-centered pronunciation practices.
        </p>
      </div>
    </div>

    <div id="modal-p2" class="modal-overlay" onclick="closeModal('modal-p2')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p2')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Poy English Program Delivery</h3>
        
        <img src="2p.jpg" alt="Poy English Program Detail" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'600\' height=\'400\' viewBox=\'0 0 600 400\'><rect width=\'600\' height=\'400\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'20\' fill=\'%231E40AF\'>Poy English Program Preview</text></svg>';">
        
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Delivered inclusive online English lessons structured around communicative teaching methods, conversational fluency lesson designs, and tech-integrated assessments.
        </p>
      </div>
    </div>

    <div id="modal-p3" class="modal-overlay" onclick="closeModal('modal-p3')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p3')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Volunteer Language Workshops</h3>
        
        <img src="3p.jpg" alt="Chiang Rai Kindergarten Detail" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'600\' height=\'400\' viewBox=\'0 0 600 400\'><rect width=\'600\' height=\'400\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'20\' fill=\'%231E40AF\'>Chiang Rai Volunteer Preview</text></svg>';">

        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Interactive educational games and storytelling sessions organized for young learners in Chiang Rai to encourage active participation and cultivate early foreign language confidence.
        </p>
      </div>
    </div>

    <!-- CONNECT WITH ME -->
    <section class="content-section" id="connect">
      <h3 class="section-headline">Connect with Me</h3>
      <div class="contact-grid" style="margin-top: 20px;">
        <a href="mailto:miayemonsan34@gmail.com" class="contact-card">
          <span class="icon">✉️</span>
          <h4>Email</h4>
          <p>miayemonsan34@gmail.com</p>
        </a>

        <div class="contact-card">
          <span class="icon">📍</span>
          <h4>Location</h4>
          <p>Chiang Mai, Thailand</p>
        </div>

        <div class="contact-card">
          <span class="icon">💼</span>
          <h4>Status</h4>
          <p>Available for Teaching Roles</p>
        </div>
      </div>
    </section>

    <!-- FOOTER -->
    <footer>
      &copy; 2026 Aye Mon San. All rights reserved.
    </footer>

  </div>

  <!-- JAVASCRIPT ENGINE FOR FILTERING & MODALS -->
  <script>
    // Navigation active highlights
    const links = document.querySelectorAll('.nav-links a');
    links.forEach(link => {
      link.addEventListener('click', function() {
        links.forEach(l => l.classList.remove('active'));
        this.classList.add('active');
      });
    });

    // Portfolio Filtering
    const filterButtons = document.querySelectorAll('.filter-btn');
    const portfolioItems = document.querySelectorAll('.portfolio-item');

    filterButtons.forEach(button => {
      button.addEventListener('click', () => {
        filterButtons.forEach(btn => btn.classList.remove('active'));
        button.classList.add('active');

        const filterValue = button.getAttribute('data-filter');

        portfolioItems.forEach(item => {
          if (filterValue === 'all' || item.getAttribute('data-category') === filterValue) {
            item.style.display = 'block';
          } else {
            item.style.display = 'none';
          }
        });
      });
    });

    // Modal Opening & Video Handler
    function openModal(id) {
      const modal = document.getElementById(id);
      if (modal) modal.classList.add("active");
    }

    function closeModal(id) {
      const modal = document.getElementById(id);
      if (modal) {
        modal.classList.remove("active");
        const video = modal.querySelector('video');
        if (video) video.pause();
      }
    }
  </script>
