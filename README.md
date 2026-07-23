
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aye Mon San | Portfolio Website</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #1F4E79;           /* Deep Ocean Blue */
      --primary-light: #EBF2F7;     /* Soft Muted Blue Accent */
      --text-dark: #101828;         /* Crisp Dark Text */
      --text-muted: #475467;        /* Soft Charcoal Secondary Text */
      --bg-outer: #0F172A;          /* Elegant Dark Slate/Navy Canvas */
      --card-bg: #ffffff;           /* Main Card Background */
      --border-color: #EAECF0;
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

    /* Main Modern Canvas Wrapper */
    .app-container {
      width: 100%;
      max-width: 1200px;
      background: var(--card-bg);
      border-radius: 40px;
      box-shadow: 0 30px 60px rgba(0, 0, 0, 0.4);
      padding: 40px 60px 60px 60px;
      position: relative;
    }

    /* Sticky/Fixed-style Navigation Bar */
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
      background: var(--primary);
      color: #fff;
      width: 32px;
      height: 32px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.75em;
    }

    .logo span {
      color: var(--primary);
    }

    .nav-links {
      display: flex;
      align-items: center;
      list-style: none;
      gap: 8px;
      background: #fdfdfd;
      padding: 6px 12px;
      border-radius: 30px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.02);
      border: 1px solid var(--border-color);
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text-muted);
      font-size: 0.9em;
      font-weight: 500;
      padding: 8px 18px;
      border-radius: 20px;
      transition: all 0.2s ease;
    }

    .nav-links a:hover, .nav-links a.active {
      color: var(--primary);
      background: var(--primary-light);
    }

    .btn-contact-nav {
      background: var(--primary);
      color: #fff;
      padding: 12px 28px;
      border-radius: 14px;
      font-weight: 500;
      text-decoration: none;
      font-size: 0.9em;
      box-shadow: 0 10px 20px rgba(31, 78, 121, 0.25);
    }

    /* Section Component Layout Container */
    .content-section {
      padding: 80px 0 40px 0;
      border-bottom: 1px solid var(--border-color);
    }

    .content-section:last-of-type {
      border-bottom: none;
    }

    /* Section Headline Styling */
    .section-headline {
      font-size: 2em;
      font-weight: 700;
      color: var(--text-dark);
      margin-bottom: 40px;
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

    /* SECTION 1: HERO HOME */
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
      background: var(--primary);
      margin-bottom: 24px;
      border-radius: 2px;
    }

    .hero-content h1 {
      font-size: 3.4em;
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
      font-size: 0.95em;
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
      background: var(--primary);
      color: #fff;
      box-shadow: 0 12px 24px rgba(31, 78, 121, 0.3);
    }

    .btn-secondary {
      background: #ffffff;
      color: var(--primary);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.04);
      border: 1px solid rgba(0,0,0,0.08);
    }

    .btn-primary:hover, .btn-secondary:hover {
      transform: translateY(-2px);
    }

    /* Mockup-Accurate Ring Visual Layout with Masking Fix */
    .hero-visual {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .circle-wrapper {
      position: relative;
      width: 400px;
      height: 400px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .purple-ring {
      position: absolute;
      width: 320px;
      height: 320px;
      border: 32px solid var(--primary);
      border-radius: 50%;
      box-shadow: 0 20px 40px rgba(31, 78, 121, 0.15);
      z-index: 1;
    }

    .outer-ring-line {
      position: absolute;
      width: 380px;
      height: 380px;
      border: 1px solid rgba(31, 78, 121, 0.2);
      border-radius: 50%;
      z-index: 0;
    }

    .avatar-img {
      position: absolute;
      z-index: 2;
      border-radius: 50%;
      clip-path: circle(50% at 50% 50%);
      object-fit: cover;
      aspect-ratio: 1/1;
      bottom: 55px;
      width: 260px;
      height: 260px;
    }

    /* SECTION 2: ABOUT */
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

    /* SECTION 3 & 4: TIMELINES (EDUCATION & EXPERIENCES) */
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
      position: relative;
      transition: all 0.3s ease;
    }

    .timeline-card:hover {
      transform: translateY(-5px);
      border-color: var(--primary);
      box-shadow: 0 15px 30px rgba(31, 78, 121, 0.08);
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

    /* SECTION 5: PORTFOLIO */
    .portfolio-intro {
      color: var(--text-muted);
      margin-bottom: 30px;
      max-width: 750px;
      line-height: 1.6;
    }

    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 16px;
    }

    .portfolio-item-card {
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

    .portfolio-item-card:hover {
      border-color: var(--primary);
      background: var(--primary-light);
      color: var(--primary);
      transform: scale(1.02);
    }

    .portfolio-icon {
      background: #ffffff;
      width: 32px;
      height: 32px;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.03);
    }

    footer {
      text-align: center;
      margin-top: 60px;
      padding-top: 30px;
      border-top: 1px solid var(--border-color);
      font-size: 0.85em;
      color: var(--text-muted);
    }

    /* Layout Responsiveness Rules */
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
    
    <!-- HEADER WEBSITE NAVIGATION -->
    <nav>
      <div class="logo">
        <div class="logo-icon">C</div>
        instructor<span>.</span>
      </div>
      
      <ul class="nav-links">
        <li><a href="#home" class="active">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#education">Education</a></li>
        <li><a href="#experiences">Experiences</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
      </ul>

      <a href="mailto:miayemonsan34@gmail.com" class="btn-contact-nav">Contact</a>
    </nav>

    <!-- 1. HOME SECTION -->
    <section class="content-section hero-layout" id="home">
      <div class="hero-content">
        <div class="accent-line"></div>
        <h1>I'm <span>Aye Mon San</span>,<br>an <span>English Instructor</span></h1>
        <div class="hero-tagline">English Instructor | TEFL Certified | Passionate Educator</div>
        <p>
          Passionate about creating inclusive and engaging learning environments where students can develop strong English communication skills while building cultural awareness and confidence.
        </p>
        <div class="cta-group">
          <a href="mailto:miayemonsan34@gmail.com" class="btn-primary">Contact Me</a>
          <a href="#portfolio" class="btn-secondary">Browse Portfolio</a>
        </div>
      </div>

      <div class="hero-visual">
        <div class="circle-wrapper">
          <div class="outer-ring-line"></div>
          <div class="purple-ring"></div>
          <img src="amscvphoto.jpg" alt="Aye Mon San Portrait" class="avatar-img">
        </div>
      </div>
    </section>

    <!-- 2. ABOUT SECTION -->
    <section class="content-section" id="about">
      <h3 class="section-headline">About Me</h3>
      <div class="about-grid" style="margin-top: 20px;">
        <div>
          <p style="color: var(--text-muted); line-height: 1.7; margin-bottom: 20px; text-align: justify;">
            I am a passionate English instructor and English Communication student with experience in online teaching, tutoring, and community education. I enjoy helping learners build confidence in English through engaging, student-centered lessons while promoting intercultural understanding and lifelong learning.
          </p>
          <h4 style="font-size: 1.1em; font-weight: 700; color: var(--text-dark); margin-top: 25px;">Core Teaching Competencies</h4>
          <div class="skills-flex">
            <span class="skill-pill">Classroom Management</span>
            <span class="skill-pill">Lesson Planning</span>
            <span class="skill-pill">English Language Instruction</span>
            <span class="skill-pill">Public Speaking</span>
            <span class="skill-pill">Cross-cultural Communication</span>
            <span class="skill-pill">Active Listening</span>
            <span class="skill-pill">Adaptability</span>
          </div>
        </div>
        
        <div class="about-details">
          <div class="about-meta-box"><h4>Nationality</h4><p>Myanmar</p></div>
          <div class="about-meta-box"><h4>Languages</h4><p>Mon, Burmese, English, Thai</p></div>
          <div class="about-meta-box"><h4>Age / Gender</h4><p>27 / Female</p></div>
          <div class="about-meta-box"><h4>Current Base</h4><p>Chiang Mai, Thailand</p></div>
        </div>
      </div>
    </section>

    <!-- 3. EDUCATION SECTION -->
    <section class="content-section" id="education">
      <h3 class="section-headline">Education</h3>
      <div class="timeline-grid" style="margin-top: 20px;">
        
        <div class="timeline-card">
          <span class="card-date-badge">2024 – Present</span>
          <h4 class="card-headline">B.A. in English Communication Arts</h4>
          <p class="card-subheadline">Payap University</p>
        </div>

        <div class="timeline-card">
          <span class="card-date-badge">2021 – 2024</span>
          <h4 class="card-headline">Associate Degree in Mass Media and Journalism</h4>
          <p class="card-subheadline">Mon National College</p>
        </div>

        <div class="timeline-card">
          <span class="card-date-badge">2018 – 2019</span>
          <h4 class="card-headline">B.A. in English</h4>
          <p class="card-subheadline">Hpa-An Distance University</p>
        </div>

      </div>
    </section>

    <!-- 4. EXPERIENCES SECTION -->
    <section class="content-section" id="experiences">
      <h3 class="section-headline">Work Experience</h3>
      <div class="timeline-grid" style="margin-top: 20px;">
        
        <!-- Job 1 -->
        <div class="timeline-card">
          <span class="card-date-badge">2025 – 2026</span>
          <h4 class="card-headline">General English Teacher</h4>
          <p class="card-subheadline">Poy English Program (Online)</p>
          <ul class="card-bullet-list">
            <li>Delivered engaging online English lessons in a supportive and inclusive learning environment.</li>
            <li>Designed interactive lessons focusing on practical communication skills, grammar, vocabulary, and pronunciation.</li>
          </ul>
        </div>

        <!-- Job 2 -->
        <div class="timeline-card">
          <span class="card-date-badge">Sep 2024 – Jul 2025</span>
          <h4 class="card-headline">Freelance English Tutor</h4>
          <p class="card-subheadline">Online Marketplace</p>
          <ul class="card-bullet-list">
            <li>Delivered personalized one-on-one and small-group English lessons to learners from diverse cultural backgrounds.</li>
            <li>Helped students improve speaking fluency, pronunciation, vocabulary, and grammar through interactive learning activities.</li>
          </ul>
        </div>

        <!-- Job 3 -->
        <div class="timeline-card">
          <span class="card-date-badge">Jan 2025</span>
          <h4 class="card-headline">Volunteer Teacher</h4>
          <p class="card-subheadline">Chiang Rai Kindergarten</p>
          <ul class="card-bullet-list">
            <li>Assisted teachers in classroom activities and supported English learning through interactive games and creative lessons.</li>
            <li>Organized educational games and activities to encourage student participation and active learning.</li>
          </ul>
        </div>

        <!-- Job 4 -->
        <div class="timeline-card">
          <span class="card-date-badge">Nov 2018 – Jan 2019</span>
          <h4 class="card-headline">Accountant</h4>
          <p class="card-subheadline">Nay La Kabar Co., Ltd.</p>
          <ul class="card-bullet-list">
            <li>Recorded daily financial transactions and prepared accurate financial reports.</li>
            <li>Reconciled accounts, verified invoices, and maintained accurate financial records.</li>
          </ul>
        </div>

      </div>
    </section>

    <!-- 5. PORTFOLIO SECTION -->
    <section class="content-section" id="portfolio">
      <h3 class="section-headline">Certifications & Achievements</h3>
      <p class="portfolio-intro">A collection of professional certifications, training programs, and academic achievements that reflect my commitment to continuous learning and professional development:</p>
      
      <div class="portfolio-grid">
        <div class="portfolio-item-card"><div class="portfolio-icon">🎓</div> TEFL Certification</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> English for Career Development</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> Teaching English in Primary Education</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> Supporting Learning in Primary Education</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> Teaching English to Refugees and Displaced Learners</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> Supporting Children's Mental Health</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> Gender in Language Education</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> Teaching Pronunciation and Listening Skills</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> Understanding English Language Systems</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> Listening and Observation in Primary Education</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">📜</div> Young Children, Nature, and Outdoor Learning</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">💼</div> Business Knowledge Sharing Workshop</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">💼</div> Career Planning and Job Search</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">🏫</div> Mon Intensive English Program</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">🏫</div> General English – Elementary Level</div>
        <div class="portfolio-item-card"><div class="portfolio-icon">🎓</div> High School Certificate</div>
      </div>
    </section>

    <!-- FOOTER -->
    <footer>
      &copy; 2026 Aye Mon San. All rights reserved.
    </footer>

  </div>

  <!-- Optional Script to handle active tab swapping while clicking links -->
  <script>
    const links = document.querySelectorAll('.nav-links a');
    links.forEach(link => {
      link.addEventListener('click', function() {
        links.forEach(l => l.classList.remove('active'));
        this.classList.add('active');
      });
    });
  </script>
