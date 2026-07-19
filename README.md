
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

    /* Container matching the card shape in the design */
    .app-container {
      width: 100%;
      max-width: 1200px;
      background: var(--card-bg);
      border-radius: 40px;
      box-shadow: 0 30px 60px rgba(0, 0, 0, 0.2);
      padding: 40px 60px 60px 60px;
      position: relative;
      overflow: hidden;
    }

    /* Navigation Bar */
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
      gap: 24px;
      background: #fdfdfd;
      padding: 6px 24px;
      border-radius: 30px;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text-muted);
      font-size: 0.9em;
      font-weight: 500;
      transition: color 0.2s;
    }

    .nav-links a.active, .nav-links a:hover {
      color: var(--primary);
    }

    .nav-links a.active {
      background: var(--primary-light);
      padding: 6px 16px;
      border-radius: 20px;
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

    /* Main Hero Layout */
    .hero-section {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      align-items: center;
      gap: 40px;
    }

    /* Left Side Content */
    .hero-content {
      max-width: 520px;
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
      border: 1px solid rgba(0,0,0,0.02);
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .btn-primary:hover, .btn-secondary:hover {
      transform: translateY(-2px);
    }

    /* Right Side Portrait Design */
    .hero-visual {
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
    }

    .circle-wrapper {
      position: relative;
      width: 400px;
      height: 400px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    /* The main signature purple ring from the image */
    .purple-ring {
      position: absolute;
      width: 320px;
      height: 320px;
      border: 32px solid var(--primary);
      border-radius: 50%;
      box-shadow: 0 20px 40px rgba(108, 92, 231, 0.15);
      z-index: 1;
    }

    /* Fine outer layout accent lines */
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

    /* Responsive adjustments */
    @media (max-width: 992px) {
      nav {
        margin-bottom: 40px;
      }
      .nav-links {
        display: none; /* Simplifies layout for tablets/mobile */
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
      .circle-wrapper {
        width: 320px;
        height: 320px;
      }
      .purple-ring {
        width: 260px;
        height: 260px;
        border-width: 24px;
      }
      .outer-ring-line {
        width: 300px;
        height: 300px;
      }
      .avatar-img {
        width: 230px;
        bottom: 20px;
      }
      .cta-group {
        justify-content: center;
      }
    }
  </style>
</head>
<body>

  <div class="app-container">
    
    <!-- NAVIGATION -->
    <nav>
      <div class="logo">
        <div class="logo-icon">C</div>
        instructor<span>.</span>
      </div>
      
      <ul class="nav-links">
        <li><a href="#" class="active">home</a></li>
        <li><a href="#">about</a></li>
        <li><a href="#">experience</a></li>
        <li><a href="#">education</a></li>
        <li><a href="#">credentials</a></li>
      </ul>

      <a href="mailto:miayemonsan34@gmail.com" class="btn-contact-nav">contact</a>
    </nav>

    <!-- HERO SECTION -->
    <div class="hero-section">
      
      <!-- Content Column -->
      <div class="hero-content">
        <div class="accent-line"></div>
        <h1>im aye mon san,<br>an <span>english instructor</span></h1>
        <p>
          Motivated and passionate English Communication student with a strong interest in teaching, intercultural communication, and lifelong learning. Experienced in volunteer teaching and community education projects.
        </p>
        <div class="cta-group">
          <a href="mailto:miayemonsan34@gmail.com" class="btn-primary">contact me</a>
          <a href="#" class="btn-secondary">view credentials</a>
        </div>
      </div>

      <!-- Visual Graphic Column -->
      <div class="hero-visual">
        <div class="circle-wrapper">
          <div class="outer-ring-line"></div>
          <div class="purple-ring"></div>
          <!-- Make sure to replace this with your cutout image path -->
          <img src="amscvphoto.png" alt="Aye Mon San Portrait" class="avatar-img">
        </div>
      </div>

    </div>

  </div>
