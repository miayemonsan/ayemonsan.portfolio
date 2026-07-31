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
      margin-bottom: 30px;
    }

    /* NEW LINK ACTION BUTTONS SECTION */
    .hero-links-group {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      align-items: center;
    }

    .action-link {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 12px 24px;
      border-radius: 14px;
      font-weight: 600;
      font-size: 0.9em;
      text-decoration: none;
      transition: all 0.25s ease;
    }

    .action-link-primary {
      background: var(--primary-gradient);
      color: #ffffff;
      box-shadow: 0 8px 20px rgba(30, 64, 175, 0.25);
    }

    .action-link-outline {
      background: #ffffff;
      color: var(--primary);
      border: 1px solid rgba(30, 64, 175, 0.25);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
    }

    .action-link:hover {
      transform: translateY(-2px);
    }

    .action-link-outline:hover {
      background: var(--primary-light);
      border-color: var(--primary);
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
      .hero-links-group {
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
        
        <!-- NEW QUICK LINKS SECTION (Replaces old button boxes) -->
        <div class="hero-links-group">
          <!-- CV / Resume Link (REPLACE href="cv.pdf" with your file path or link) -->
          <a href="https://miayemonsan.github.io/ayemonsan.cv/" target="_blank" class="action-link action-link-outline">
            <i class="fa-solid fa-file-pdf"></i> CV / Resume
          </a>

          <!-- LinkedIn Link (REPLACE with your actual LinkedIn profile URL) -->
          <a href="https://linkedin.com" target="_blank" class="action-link action-link-outline">
            <i class="fa-brands fa-linkedin"></i> LinkedIn
          </a>

          <!-- Connect with Me smooth scroll button -->
          <a href="#connect" class="action-link action-link-primary">
            <i class="fa-solid fa-paper-plane"></i> Connect With Me
          </a>
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
        </div>
      </div>
    </section>

    <!-- ABOUT ME -->
    <section class="content-section" id="about">
      <h3 class="section-headline">About Me</h3>
      <div class="about-grid" style="margin-top: 20px;">
        <div>
          <p style="color: var(--text-muted); line-height: 1.7; margin-bottom: 20px; text-align: justify;">
            I am a passionate English instructor with two-year experience in online teaching, tutoring, and community education. I enjoy helping learners build confidence in English through engaging, student-centered lessons while promoting intercultural understanding and lifelong learning.
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
        
        <!-- TEACHING & CLASSES (p1 to p7) -->
        <!-- CARD 1 -->
        <div class="portfolio-item" data-category="teaching" onclick="openModal('modal-p1')">
          <img src="T1.jpg" alt="Interactive English Modules" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Interactive English Modules</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Interactive English Modules</h4>
            <p>Teaching & Classes • Lesson Materials</p>
          </div>
        </div>

        <!-- CARD 2 -->
        <div class="portfolio-item" data-category="teaching" onclick="openModal('modal-p2')">
          <img src="T2.jpg" alt="Poy English Program Delivery" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Poy English Program</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Poy English Program Delivery</h4>
            <p>Teaching & Classes • Online Instruction</p>
          </div>
        </div>

        <!-- CARD 3 -->
        <div class="portfolio-item" data-category="teaching" onclick="openModal('modal-p3')">
          <img src="T3.jpg" alt="Conversational Practice Sessions" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Conversational Practice</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Conversational Practice Sessions</h4>
            <p>Teaching & Classes • Group Tutoring</p>
          </div>
        </div>

        <!-- CARD 4 -->
        <div class="portfolio-item" data-category="teaching" onclick="openModal('modal-p4')">
          <img src="T4.jpg" alt="Grammar & Vocabulary Builder" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Grammar & Vocabulary</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Grammar & Vocabulary Builder</h4>
            <p>Teaching & Classes • Interactive Slides</p>
          </div>
        </div>

        <!-- CARD 5 -->
        <div class="portfolio-item" data-category="teaching" onclick="openModal('modal-p5')">
          <img src="T5.jpg" alt="Student Assessment & Feedback" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Assessment & Feedback</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Student Assessment & Feedback</h4>
            <p>Teaching & Classes • Progress Evaluation</p>
          </div>
        </div>

        <!-- CARD 6 -->
        <div class="portfolio-item" data-category="teaching" onclick="openModal('modal-p6')">
          <img src="T6.png" alt="Pronunciation & Listening Systems" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Pronunciation Practice</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Pronunciation & Listening Systems</h4>
            <p>Teaching & Classes • Audio-Visual Media</p>
          </div>
        </div>

        <!-- CARD 7 -->
        <div class="portfolio-item" data-category="teaching" onclick="openModal('modal-p7')">
          <img src="T7.png" alt="Curriculum & Course Outline" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Curriculum Design</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Curriculum & Course Planning</h4>
            <p>Teaching & Classes • Lesson Frameworks</p>
          </div>
        </div>


        <!-- VOLUNTEERING & PROJECTS (p8 to p13) -->
        <!-- CARD 8 -->
        <div class="portfolio-item" data-category="volunteering" onclick="openModal('modal-p8')">
          <img src="V1.JPG" alt="Chiang Rai Volunteer Teaching" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Kindergarten Volunteering</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Chiang Rai Kindergarten Project</h4>
            <p>Volunteering & Projects • Early Childhood</p>
          </div>
        </div>

        <!-- CARD 9 -->
        <div class="portfolio-item" data-category="volunteering" onclick="openModal('modal-p9')">
          <img src="V10.JPG" alt="Interactive Classroom Activities" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Classroom Activities</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Interactive Classroom Activities</h4>
            <p>Volunteering & Projects • Group Engagement</p>
          </div>
        </div>

        <!-- CARD 10 -->
        <div class="portfolio-item" data-category="volunteering" onclick="openModal('modal-p10')">
          <img src="V11.jpg" alt="Educational Games & Storytelling" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Educational Games</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Educational Games & Storytelling</h4>
            <p>Volunteering & Projects • Active Learning</p>
          </div>
        </div>

        <!-- CARD 11 -->
        <div class="portfolio-item" data-category="volunteering" onclick="openModal('modal-p11')">
          <img src="V12.JPG" alt="Community Outreach & Workshops" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Community Outreach</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Community Outreach & Workshops</h4>
            <p>Volunteering & Projects • Educational Support</p>
          </div>
        </div>

        <!-- CARD 12 -->
        <div class="portfolio-item" data-category="volunteering" onclick="openModal('modal-p12')">
          <img src="V13.jpg" alt="Outdoor & Experiential Learning" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Outdoor Learning</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Outdoor & Experiential Learning</h4>
            <p>Volunteering & Projects • Nature Activities</p>
          </div>
        </div>

        <!-- CARD 13 -->
        <div class="portfolio-item" data-category="volunteering" onclick="openModal('modal-p13')">
          <img src="V9.JPG" alt="Cultural Exchange Sessions" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'400\' height=\'300\' viewBox=\'0 0 400 300\'><rect width=\'400\' height=\'300\' fill=\'%23EFF6FF\'/><text x=\'50%\' y=\'50%\' dominant-baseline=\'middle\' text-anchor=\'middle\' font-family=\'sans-serif\' font-size=\'16\' fill=\'%231E40AF\'>Cultural Exchange</text></svg>';">
          <div class="portfolio-overlay">
            <h4>Cultural Exchange Sessions</h4>
            <p>Volunteering & Projects • Intercultural Learning</p>
          </div>
        </div>

      </div>
    </section>

    <!-- MODAL POPUPS (MODAL 1 TO 13) -->
    <!-- Modal 1 -->
    <div id="modal-p1" class="modal-overlay" onclick="closeModal('modal-p1')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p1')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Interactive English Modules</h3>
        <img src="p1.JPG.jpg" alt="Detail View 1" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Designed engaging online modules focusing on practical everyday conversational English, vocabulary expansion, and student-centered pronunciation practices.
        </p>
      </div>
    </div>

    <!-- Modal 2 -->
    <div id="modal-p2" class="modal-overlay" onclick="closeModal('modal-p2')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p2')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Poy English Program Delivery</h3>
        <img src="p2.JPG.jpg" alt="Detail View 2" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Delivered inclusive online English lessons structured around communicative teaching methods, conversational fluency lesson designs, and tech-integrated assessments.
        </p>
      </div>
    </div>

    <!-- Modal 3 -->
    <div id="modal-p3" class="modal-overlay" onclick="closeModal('modal-p3')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p3')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Conversational Practice Sessions</h3>
        <img src="p3.JPG.jpg" alt="Detail View 3" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Facilitated guided one-on-one and group speaking sessions aimed at boosting student confidence, accent reduction, and real-time error correction.
        </p>
      </div>
    </div>

    <!-- Modal 4 -->
    <div id="modal-p4" class="modal-overlay" onclick="closeModal('modal-p4')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p4')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Grammar & Vocabulary Builder</h3>
        <img src="p4.JPG.jpg" alt="Detail View 4" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Structured slide decks and interactive visual worksheets to help non-native learners grasp essential grammar structures and contextual vocabulary.
        </p>
      </div>
    </div>

    <!-- Modal 5 -->
    <div id="modal-p5" class="modal-overlay" onclick="closeModal('modal-p5')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p5')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Student Assessment & Feedback</h3>
        <img src="p5.JPG.jpg" alt="Detail View 5" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Continuous evaluation frameworks and personalized feedback logs designed to track individual learner progression across reading, writing, and speaking.
        </p>
      </div>
    </div>

    <!-- Modal 6 -->
    <div id="modal-p6" class="modal-overlay" onclick="closeModal('modal-p6')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p6')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Pronunciation & Listening Systems</h3>
        <img src="p6.JPG.png" alt="Detail View 6" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Audio-guided phonetics exercises and listening activities focusing on natural speech patterns, intonation, and listening comprehension techniques.
        </p>
      </div>
    </div>

    <!-- Modal 7 -->
    <div id="modal-p7" class="modal-overlay" onclick="closeModal('modal-p7')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p7')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Curriculum & Course Planning</h3>
        <img src="p7.JPG.png" alt="Detail View 7" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Comprehensive syllabus designs and structured lesson outlines tailored for online marketplaces and diverse learner demographics.
        </p>
      </div>
    </div>

    <!-- Modal 8 -->
    <div id="modal-p8" class="modal-overlay" onclick="closeModal('modal-p8')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p8')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Chiang Rai Kindergarten Project</h3>
        <img src="p8.JPG.JPG" alt="Detail View 8" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Volunteered in Chiang Rai assisting lead teachers in executing immersive English activities and school-wide educational development initiatives.
        </p>
      </div>
    </div>

    <!-- Modal 9 -->
    <div id="modal-p9" class="modal-overlay" onclick="closeModal('modal-p9')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p9')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Interactive Classroom Activities</h3>
        <img src="p9.JPG.JPG" alt="Detail View 9" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Organized dynamic group learning games designed to maximize student engagement, active participation, and language retention.
        </p>
      </div>
    </div>

    <!-- Modal 10 -->
    <div id="modal-p10" class="modal-overlay" onclick="closeModal('modal-p10')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p10')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Educational Games & Storytelling</h3>
        <img src="p10.JPG.JPG" alt="Detail View 10" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Utilized creative storytelling, visual props, and educational games to foster a fun, supportive learning environment for young learners.
        </p>
      </div>
    </div>

    <!-- Modal 11 -->
    <div id="modal-p11" class="modal-overlay" onclick="closeModal('modal-p11')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p11')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Community Outreach & Workshops</h3>
        <img src="p11.JPG.jpg" alt="Detail View 11" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Engaged in community language workshops providing supplementary educational support and mentoring to displaced and young learners.
        </p>
      </div>
    </div>

    <!-- Modal 12 -->
    <div id="modal-p12" class="modal-overlay" onclick="closeModal('modal-p12')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p12')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Outdoor & Experiential Learning</h3>
        <img src="p12.JPG.JPG" alt="Detail View 12" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Integrated outdoor learning sessions linking language acquisition with nature, physical activity, and practical observational tasks.
        </p>
      </div>
    </div>

    <!-- Modal 13 -->
    <div id="modal-p13" class="modal-overlay" onclick="closeModal('modal-p13')">
      <div class="modal-card" onclick="event.stopPropagation()">
        <span class="close-modal" onclick="closeModal('modal-p13')">&times;</span>
        <h3 style="margin-bottom: 15px; color: var(--text-dark);">Cultural Exchange Sessions</h3>
        <img src="p13.JPG.jpg" alt="Detail View 13" style="width: 100%; border-radius: 16px; margin-bottom: 15px;" onerror="this.onerror=null; this.style.display='none';">
        <p style="color: var(--text-muted); line-height: 1.6; font-size: 0.95em;">
          Promoted intercultural competence through shared stories, regional traditions, and collaborative language exercises among diverse student backgrounds.
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
