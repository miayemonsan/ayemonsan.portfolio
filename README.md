
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aye Mon San | Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #6c5ce7;
      --primary-light: #efecfd;
      --text-dark: #1e1e24;
      --text-muted: #6b7280;
      --bg-outer: #6c5ce7;
      --card-bg: #ffffff;
      --border-color: #f3f4f6;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
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

    /* Main Modern Container Frame */
    .app-container {
      width: 100%;
      max-width: 1200px;
      background: var(--card-bg);
      border-radius: 40px;
      box-shadow: 0 30px 60px rgba(0, 0, 0, 0.2);
      padding: 40px 60px 60px 60px;
      position: relative;
    }

    /* Navigation Bar Layout */
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 60px;
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
      gap: 12px;
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
      padding: 8px 16px;
      border-radius: 20px;
      transition: all 0.2s ease;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    .nav-links a.active {
      background: var(--primary-light);
      color: var(--primary);
    }

    .btn-contact-nav {
      background: var(--primary);
      color: #fff;
      padding: 12px 28px;
      border-radius: 14px;
      font-weight: 500;
      text-decoration: none;
      font-size: 0.9em;
      box-shadow: 0 10px 20px rgba(108, 92, 231, 0.2);
    }

    /* Hero Section Component */
    .hero-section {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      align-items: center;
      gap: 40px;
      margin-bottom: 60px;
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
      margin-bottom: 24px;
      letter-spacing: -1px;
    }

    .hero-content h1 span {
      color: var(--primary);
    }

    .hero-content p {
      color: var(--text-muted);
      font-size: 0.95em;
      line-height: 1.6;
      margin-bottom: 40px;
      text-align: justify;
    }

    .cta-group {
      display: flex;
      gap: 20px;
    }

    .btn-primary {
      background: var(--primary);
      color: #fff;
      padding: 16px 36px;
      border-radius: 16px;
      font-weight: 600;
      text-decoration: none;
      font-size: 0.95em;
      box-shadow: 0 12px 24px rgba(108, 92, 231, 0.3);
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .btn-secondary {
      background: #ffffff;
      color: var(--primary);
      padding: 16px 36px;
      border-radius: 16px;
      font-weight: 600;
      text-decoration: none;
      font-size: 0.95em;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.04);
      border: 1px solid rgba(0,0,0,0.05);
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .btn-primary:hover, .btn-secondary:hover {
      transform: translateY(-2px);
    }

    /* Ring Visual Graphics */
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
      box-shadow: 0 20px 40px rgba(108, 92, 231, 0.15);
      z-index: 1;
    }

    .outer-ring-line {
      position: absolute;
      width: 380px;
      height: 380px;
      border: 1px solid rgba(108, 92, 231, 0.15);
      border-radius: 50%;
      z-index: 0;
    }

    .avatar-img {
      position: absolute;
      bottom: 25px; 
      width: 290px;
      height: auto;
      z-index: 2;
      pointer-events: none;
    }

    /* Core CV Secondary Grid System */
    .cv-details-grid {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 60px;
      border-top: 2px solid var(--border-color);
      padding-top: 60px;
    }

    .section-headline {
      font-size: 1.4em;
      font-weight: 700;
      color: var(--text-dark);
      margin-bottom: 24px;
      position: relative;
      padding-bottom: 8px;
    }

    .section-headline::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: 0;
      width: 35px;
      height: 3px;
      background: var(--primary);
      border-radius: 2px;
    }

    .sidebar-block {
      margin-bottom: 40px;
    }

    /* Sidebar Content Styles */
    .contact-item, .meta-item {
      margin-bottom: 12px;
      font-size: 0.95em;
      color: var(--text-muted);
    }

    .contact-item b, .meta-item b {
      color: var(--text-dark);
    }

    .lang-badge {
      display: flex;
      justify-content: space-between;
      padding: 8px 0;
      border-bottom: 1px dashed var(--border-color);
      font-size: 0.95em;
    }

    .lang-level {
      color: var(--primary);
      font-weight: 500;
    }

    .skills-flex {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .skill-pill {
      background: var(--primary-light);
      color: var(--primary);
      padding: 6px 14px;
      border-radius: 20px;
      font-size: 0.85em;
      font-weight: 500;
    }

    /* Main Experience Timeline Style components */
    .timeline-item {
      position: relative;
      padding-left: 28px;
      border-left: 2px solid var(--primary-light);
      margin-bottom: 35px;
    }

    .timeline-item::before {
      content: '';
      position: absolute;
      left: -7px;
      top: 6px;
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: var(--primary);
    }

    .timeline-meta {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      margin-bottom: 4px;
    }

    .timeline-title {
      font-size: 1.15em;
      font-weight: 700;
      color: var(--text-dark);
    }

    .timeline-date {
      font-size: 0.85em;
      font-weight: 500;
      color: var(--text-light);
    }

    .timeline-org {
      font-weight: 600;
      color: var(--primary);
      font-size: 0.95em;
      margin-bottom: 10px;
    }

    .timeline-desc {
      list-style-position: inside;
      color: var(--text-muted);
      font-size: 0.9em;
    }

    .timeline-desc li {
      margin-bottom: 4px;
      line-height: 1.5;
    }

    /* Dynamic Grid Layout for Credentials */
    .credentials-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
    }

    .cert-item-card {
      background: #fafafa;
      border: 1px solid var(--border-color);
      padding: 12px 16px;
      border-radius: 12px;
      font-size: 0.85em;
      color: var(--text-dark);
      font-weight: 500;
      display: flex;
      align-items: center;
      gap: 10px;
      transition: all 0.2s;
    }

    .cert-item-card:hover {
      border-color: var(--primary);
      background: var(--primary-light);
    }

    .cert-icon {
      color: var(--primary);
      font-weight: bold;
    }

    footer {
      text-align: center;
      margin-top: 60px;
      padding-top: 30px;
      border-top: 1px solid var(--border-color);
      font-size: 0.85em;
      color: var(--text-light);
    }

    /* Full Responsiveness Rule Breaks */
    @media (max-width: 992px) {
      .app-container {
        padding: 30px;
      }
      .nav-links {
        display: none;
      }
      .hero-section {
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
      .cv-details-grid {
        grid-template-columns: 1fr;
        gap: 40px;
      }
      .credentials-grid {
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
        <div class="logo-icon">C</div>
        instructor<span>.</span>
      </div>
      
      <ul class="nav-links">
        <li><a href="#home" class="active">home</a></li>
        <li><a href="#experience">experience</a></li>
        <li><a href="#education">education</a></li>
        <li><a href="#certificates">credentials</a></li>
      </ul>

      <a href="mailto:miayemonsan34@gmail.com" class="btn-contact-nav">contact</a>
    </nav>

    <!-- HERO PROFILE SECTION -->
    <section class="hero-section" id="home">
      <div class="hero-content">
        <div class="accent-line"></div>
        <h1>im aye mon san,<br>an <span>english instructor</span></h1>
        <p>
          Motivated and passionate English Communication student with a strong interest in teaching, intercultural communication, and lifelong learning. Experienced in volunteer teaching and community education projects. Dedicated to fostering inclusive, engaging learning environments that encourage students to develop both linguistic and cultural competence.
        </p>
        <div class="cta-group">
          <a href="mailto:miayemonsan34@gmail.com" class="btn-primary">contact me</a>
          <a href="#certificates" class="btn-secondary">view credentials</a>
        </div>
      </div>

      <div class="hero-visual">
        <div class="circle-wrapper">
          <div class="outer-ring-line"></div>
          <div class="purple-ring"></div>
          <img src="amscvphoto.png" alt="Aye Mon San Portrait" class="avatar-img">
        </div>
      </div>
    </section>

    <!-- METADATA & DATA GRID LAYOUT -->
    <div class="cv-details-grid">
      
      <!-- LEFT COLUMN: SIDEBAR DATA -->
      <aside>
        
        <!-- Contact Block -->
        <div class="sidebar-block">
          <h3 class="section-headline">Contact</h3>
          <div class="contact-item"><b>Phone:</b> 092-396-9849</div>
          <div class="contact-item"><b>Email:</b> <a href="mailto:miayemonsan34@gmail.com">miayemonsan34@gmail.com</a></div>
          <div class="contact-item"><b>Address:</b> Chiang Mai, Thailand</div>
        </div>

        <!-- Personal Info Block -->
        <div class="sidebar-block">
          <h3 class="section-headline">Personal Info</h3>
          <div class="meta-item"><b>Gender:</b> Female</div>
          <div class="meta-item"><b>Age:</b> 27</div>
          <div class="meta-item"><b>Nationality:</b> Myanmar</div>
          <div class="meta-item"><b>Marital Status:</b> Single</div>
        </div>

        <!-- Languages Block -->
        <div class="sidebar-block">
          <h3 class="section-headline">Languages</h3>
          <div class="lang-badge"><span>Mon</span> <span class="lang-level">Native</span></div>
          <div class="lang-badge"><span>Burmese</span> <span class="lang-level">Fluent</span></div>
          <div class="lang-badge"><span>English</span> <span class="lang-level">Proficient</span></div>
          <div class="lang-badge"><span>Thai</span> <span class="lang-level">Intermediate</span></div>
        </div>

        <!-- Skills Block -->
        <div class="sidebar-block">
          <h3 class="section-headline">Core Skills</h3>
          <div class="skills-flex">
            <span class="skill-pill">Classroom Management</span>
            <span class="skill-pill">Communication & Presentation</span>
            <span class="skill-pill">Public Speaking & Leadership</span>
            <span class="skill-pill">Cross-cultural Understanding</span>
            <span class="skill-pill">Active Listening & Adaptability</span>
          </div>
        </div>

      </aside>

      <!-- RIGHT COLUMN: MAIN EXPERIENCE & TIMELINES -->
      <main>
        
        <!-- Work Experience Timeline -->
        <section id="experience" style="margin-bottom: 50px;">
          <h3 class="section-headline">Work Experience</h3>
          
          <!-- Job 1 -->
          <div class="timeline-item">
            <div class="timeline-meta">
              <span class="timeline-title">General English Teacher</span>
              <span class="timeline-date">2025 – 2026</span>
            </div>
            <div class="timeline-org">Poy English Program (Online)</div>
            <ul class="timeline-desc">
              <li>Taught English online, cultivating a welcoming, supportive, and inclusive learning environment.</li>
              <li>Integrated practical conversational skills and foundational grammar structures into modern lesson formats.</li>
            </ul>
          </div>

          <!-- Job 2 -->
          <div class="timeline-item">
            <div class="timeline-meta">
              <span class="timeline-title">Freelance English Tutor</span>
              <span class="timeline-date">Sep 2024 – Jul 2025</span>
            </div>
            <div class="timeline-org">Online Marketplace</div>
            <ul class="timeline-desc">
              <li>Provided specialized 1-on-1 and targeted group English lessons to learners from diverse cultural backgrounds.</li>
              <li>Focused on advancing conversational fluidity, accent reduction, and grammar accuracy via high-engagement interactive sessions.</li>
            </ul>
          </div>

          <!-- Job 3 -->
          <div class="timeline-item">
            <div class="timeline-meta">
              <span class="timeline-title">Volunteer Teacher</span>
              <span class="timeline-date">Jan 2025</span>
            </div>
            <div class="timeline-org">Chiang Rai Kindergarten</div>
            <ul class="timeline-desc">
              <li>Assisted in school-wide development initiatives and executed immersive English learning activities.</li>
              <li>Organized dynamic, educational games designed to maximize classroom engagement and active retention.</li>
              <li>Collaborated closely with lead teachers on targeted lesson execution and strategic classroom management.</li>
            </ul>
          </div>

          <!-- Job 4 -->
          <div class="timeline-item">
            <div class="timeline-meta">
              <span class="timeline-title">Accountant</span>
              <span class="timeline-date">Nov 2018 – Jan 2019</span>
            </div>
            <div class="timeline-org">Nay La Kabar Co., Ltd.</div>
            <ul class="timeline-desc">
              <li>Managed daily financial logging profiles and assisted in the structuring of precise transactional reports.</li>
              <li>Reconciled balance inquiries against incoming vendor invoices while monitoring strict operational budget limits.</li>
              <li>Assisted corporate teams in compiling accurate end-of-month financial summary records.</li>
            </ul>
          </div>
        </section>

        <!-- Education Timeline -->
        <section id="education" style="margin-bottom: 50px;">
          <h3 class="section-headline">Education</h3>
          
          <!-- Edu 1 -->
          <div class="timeline-item">
            <div class="timeline-meta">
              <span class="timeline-title">B.A. in English Communication Arts</span>
              <span class="timeline-date">2024 – Present</span>
            </div>
            <div class="timeline-org">Payap University</div>
          </div>

          <!-- Edu 2 -->
          <div class="timeline-item">
            <div class="timeline-meta">
              <span class="timeline-title">Associate Degree of Arts in Mass Media and Journalism</span>
              <span class="timeline-date">2021 – 2024</span>
            </div>
            <div class="timeline-org">Mon National College</div>
          </div>

          <!-- Edu 3 -->
          <div class="timeline-item">
            <div class="timeline-meta">
              <span class="timeline-title">B.A. in English</span>
              <span class="timeline-date">2018 – 2019</span>
            </div>
            <div class="timeline-org">Hpa-An Distance University</div>
          </div>
        </section>

        <!-- Certifications Layout Grid -->
        <section id="certificates">
          <h3 class="section-headline">Credentials & Certifications</h3>
          <div class="credentials-grid">
            <div class="cert-item-card"><span class="cert-icon">✓</span> TEFL Certification</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> English for Career Development</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Teaching English in Primary Education</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Supporting Learning in Primary Education</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Teaching Refugees & Displaced Learners</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Supporting Children's Mental Health</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Gender in Language Education</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Teaching Pronunciation & Listening Systems</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Understanding Language Systems</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Primary Education: Listening & Observing</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Young Children, the Outdoors, and Nature</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Business Knowledge Sharing Workshop</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Career Planning and Job Search</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> Mon Intensive English Program</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> General English (Elementary Level)</div>
            <div class="cert-item-card"><span class="cert-icon">✓</span> High School Certificate</div>
          </div>
        </section>

      </main>

    </div>

    <!-- FOOTER -->
    <footer>
      &copy; 2026 Aye Mon San. All Rights Reserved.
    </footer>

  </div>
