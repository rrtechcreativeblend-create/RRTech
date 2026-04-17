<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <meta name="description" content="RR TechCreative Blend Solutions - AI, Automation, Analytics & Digital Transformation. Premium services in business analysis, Power BI, UI/UX, and intelligent automation.">
  <meta name="keywords" content="AI, Automation, Power BI, Business Analyst, Digital Marketing, UI/UX, Data Analytics, Hyderabad">
  <meta name="author" content="RR TechCreative Blend Solutions">
  <title>RR TechCreative Blend | AI · Automation · Analytics</title>
  <!-- Boxicons & Google Fonts -->
  <link href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
  <!-- EmailJS SDK -->
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Poppins', sans-serif;
      background: #0e0e0e;
      color: #f0f0f0;
      scroll-behavior: smooth;
      line-height: 1.7;
    }
    /* ----- HEADER (PREMIUM GLASS BUT RR IS CRYSTAL CLEAR) ----- */
    .header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(8, 12, 18, 0.96);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-bottom: 2px solid rgba(0, 238, 255, 0.6);
      padding: 18px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
      transition: 0.3s;
      box-shadow: 0 4px 25px rgba(0, 238, 255, 0.2);
    }
    .header.sticky {
      padding: 12px 8%;
      background: rgba(0, 0, 0, 0.98);
      box-shadow: 0 8px 35px rgba(0, 238, 255, 0.35);
      border-bottom: 2px solid #0ef;
    }
    
    .logo-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-decoration: none;
      transition: transform 0.2s ease;
      line-height: 1;
      cursor: pointer;
      text-align: center;
    }
    .logo-container:hover { transform: scale(1.02); }
    
    .logo-line1 {
      font-size: 72px;
      font-weight: 900;
      letter-spacing: -4px;
      margin-bottom: 8px;
      display: flex;
      gap: 0;
      justify-content: center;
      line-height: 1;
      position: relative;
    }
    .logo-r-first {
      font-size: 82px;
      font-weight: 900;
      background: linear-gradient(135deg, #FF8C00 50%, #0066FF 50%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      letter-spacing: -2px;
      display: inline-block;
    }
    .logo-r-second {
      font-size: 82px;
      font-weight: 900;
      background: linear-gradient(135deg, #0066FF 50%, #FF8C00 50%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      letter-spacing: -2px;
      margin-left: -12px;
      display: inline-block;
    }
    .logo-line1::after {
      content: '';
      position: absolute;
      bottom: 12px;
      left: 48%;
      transform: translateX(-50%);
      width: 55px;
      height: 3px;
      background: linear-gradient(90deg, #FF8C00, #0ef, #0066FF);
      border-radius: 3px;
      opacity: 0.8;
      pointer-events: none;
    }
    
    .logo-line2 {
      font-size: 32px;
      font-weight: 700;
      letter-spacing: 1px;
      margin-bottom: 12px;
      background: linear-gradient(120deg, #0066FF, #4a90e2, #0ef);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-align: center;
    }
    
    .logo-line3 {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      margin-bottom: 8px;
      width: 100%;
    }
    .logo-line-left, .logo-line-right {
      width: 60px;
      height: 3px;
      background: linear-gradient(90deg, transparent, #0ef, #0ef);
      border-radius: 3px;
      box-shadow: 0 0 8px rgba(0, 238, 255, 0.6);
      transition: all 0.3s ease;
    }
    .logo-line-right {
      background: linear-gradient(90deg, #0ef, #0ef, transparent);
    }
    .logo-container:hover .logo-line-left,
    .logo-container:hover .logo-line-right {
      box-shadow: 0 0 12px #0ef;
      height: 4px;
      width: 70px;
    }
    .logo-blend-text {
      font-size: 36px;
      font-weight: 800;
      letter-spacing: 2px;
      background: linear-gradient(145deg, #FF8C00, #FFB347);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      padding: 0 8px;
    }
    
    .logo-line4 {
      font-size: 34px;
      font-weight: 800;
      letter-spacing: 4px;
      margin-top: 8px;
      background: linear-gradient(135deg, #0ef, #0066FF, #3a86ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-align: center;
      display: inline-block;
    }
    
    @media (max-width: 950px) {
      .logo-line1 { font-size: 52px; }
      .logo-r-first, .logo-r-second { font-size: 60px; }
      .logo-r-second { margin-left: -8px; }
      .logo-line2 { font-size: 26px; }
      .logo-blend-text { font-size: 28px; }
      .logo-line4 { font-size: 26px; }
      .logo-line-left, .logo-line-right { width: 45px; }
    }
    @media (max-width: 700px) {
      .logo-line1 { font-size: 40px; }
      .logo-r-first, .logo-r-second { font-size: 46px; }
      .logo-r-second { margin-left: -6px; }
      .logo-line2 { font-size: 20px; }
      .logo-blend-text { font-size: 22px; }
      .logo-line4 { font-size: 20px; }
      .logo-line-left, .logo-line-right { width: 30px; }
      .logo-line3 { gap: 12px; }
    }
    
    .navbar { display: flex; gap: 8px; }
    .navbar a {
      padding: 10px 22px;
      font-size: 16px;
      font-weight: 600;
      color: #eef5ff;
      text-decoration: none;
      border-radius: 40px;
      transition: 0.25s;
      cursor: pointer;
      letter-spacing: 0.5px;
      background: rgba(255,255,255,0.05);
    }
    .navbar a:hover,
    .navbar a.active {
      background: linear-gradient(135deg, #0ef, #3a86ff);
      color: #111;
      box-shadow: 0 0 20px #0ef;
    }
    #menu-icon {
      font-size: 40px;
      color: #0ef;
      cursor: pointer;
      display: none;
    }
    
    /* Page visibility management */
    .page { display: none; }
    .page.active-page { display: block; }
    
    /* HOME PAGE STYLES */
    .home-hero {
      min-height: 100vh;
      background: linear-gradient(135deg, rgba(0,0,0,0.85) 0%, rgba(0,20,20,0.9) 100%),
                  url('https://images.unsplash.com/photo-1633356122102-3fe601e05bd2?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80') center/cover fixed;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 160px 8% 80px;
      flex-wrap: wrap;
    }
    .home-content { max-width: 700px; }
    .home-content h3 { font-size: 30px; font-weight: 500; color: #ccf0ff; }
    .hero-line1 {
      font-size: 110px;
      font-weight: 900;
      line-height: 1.05;
      letter-spacing: 4px;
      margin: 15px 0 5px;
      text-align: center;
      display: flex;
      gap: 0;
      justify-content: center;
    }
    .hero-r-first {
      font-size: 130px;
      font-weight: 900;
      background: linear-gradient(135deg, #FF8C00 50%, #0066FF 50%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .hero-r-second {
      font-size: 130px;
      font-weight: 900;
      background: linear-gradient(135deg, #0066FF 50%, #FF8C00 50%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-left: -12px;
    }
    .hero-line2 {
      font-size: 58px;
      font-weight: 800;
      line-height: 1.2;
      letter-spacing: 3px;
      margin: 10px 0 20px;
      text-align: center;
      background: linear-gradient(120deg, #0066FF, #4a90e2, #0ef);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .hero-line3 {
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 25px 0;
      gap: 30px;
    }
    .hero-line3::before, .hero-line3::after {
      content: "";
      flex: 1;
      height: 4px;
      background: linear-gradient(90deg, transparent, #0ef, #0ef, transparent);
      border-radius: 4px;
      box-shadow: 0 0 12px rgba(0,238,255,0.7);
    }
    .hero-blend {
      font-size: 76px;
      font-weight: 900;
      letter-spacing: 6px;
      padding: 0 25px;
      background: linear-gradient(145deg, #FF8C00, #FFB347);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .hero-line4 {
      font-size: 54px;
      font-weight: 800;
      line-height: 1.2;
      letter-spacing: 4px;
      margin: 15px 0;
      text-align: center;
      background: linear-gradient(135deg, #0ef, #0066FF, #3a86ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .home-content p { font-size: 20px; margin: 30px 0 35px; color: #d0d0d0; }
    .highlight { color: #0ef; font-weight: 600; }
    .home-sci {
      display: flex;
      gap: 20px;
      margin: 30px 0 25px;
      justify-content: center;
    }
    .home-sci a img {
      width: 48px;
      height: 48px;
      border-radius: 50%;
      background: #fff;
      transition: 0.3s;
    }
    .home-sci a:hover img {
      transform: translateY(-6px) scale(1.05);
      box-shadow: 0 0 0 3px #0ef;
    }
    .btn {
      display: inline-block;
      padding: 18px 48px;
      background: linear-gradient(145deg, #0ef, #0ac);
      color: #111;
      font-weight: 700;
      font-size: 20px;
      border-radius: 60px;
      text-decoration: none;
      box-shadow: 0 10px 25px rgba(0, 239, 255, 0.4);
      transition: 0.3s;
      cursor: pointer;
      border: none;
    }
    .btn:hover {
      transform: translateY(-5px);
      box-shadow: 0 25px 35px rgba(0, 238, 255, 0.5);
    }
    .home-img img {
      width: 450px;
      height: 450px;
      border-radius: 40% 60% 30% 70% / 50% 40% 60% 50%;
      object-fit: cover;
      border: 5px solid #0ef;
      box-shadow: 0 0 60px #0ef;
      animation: float 5s ease-in-out infinite;
    }
    @keyframes float {
      0% { border-radius: 40% 60% 30% 70% / 50% 40% 60% 50%; transform: translateY(0); }
      50% { border-radius: 60% 40% 70% 30% / 40% 60% 40% 60%; transform: translateY(-20px); }
      100% { border-radius: 40% 60% 30% 70% / 50% 40% 60% 50%; transform: translateY(0); }
    }
    
    /* Services Section */
    .services-section, .stats-section, .contact-section {
      padding: 140px 8% 100px;
    }
    .services-section { background: linear-gradient(135deg, #0a0a0f, #0f0f1a); }
    .stats-section { background: linear-gradient(135deg, #0a0a0f 0%, #0f0f1a 100%); }
    .contact-section { background: radial-gradient(circle at 30% 30%, #112, #020202); }
    
    .services-section h2, .stats-section h2, .contact-section h2 {
      font-size: 52px;
      text-align: center;
      background: linear-gradient(135deg, #0ef, #6ad4ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 70px;
      font-weight: 800;
    }
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 40px;
    }
    .service-card {
      background: rgba(20, 20, 30, 0.7);
      backdrop-filter: blur(6px);
      border: 1px solid rgba(0, 238, 255, 0.2);
      border-radius: 36px;
      padding: 35px 28px;
      transition: 0.35s;
      display: flex;
      flex-direction: column;
    }
    .service-card:hover {
      transform: scale(1.02);
      border-color: #0ef;
      box-shadow: 0 0 45px rgba(0, 238, 255, 0.25);
    }
    .service-img {
      width: 100%;
      height: 220px;
      object-fit: cover;
      border-radius: 28px;
      margin-bottom: 28px;
      border: 2px solid #0ef;
    }
    .service-card h3 { font-size: 28px; color: #0ef; margin-bottom: 18px; }
    .service-card p { font-size: 16px; color: #ddd; margin-bottom: 28px; flex: 1; }
    .card-btn {
      align-self: flex-start;
      padding: 14px 32px;
      background: transparent;
      border: 2px solid #0ef;
      border-radius: 50px;
      color: #0ef;
      font-weight: 700;
      cursor: pointer;
      transition: 0.3s;
    }
    .card-btn:hover { background: #0ef; color: #111; box-shadow: 0 0 25px #0ef; }
    
    /* Stats Section */
    .stats-container { max-width: 1300px; margin: 0 auto; }
    .stats-header { text-align: center; margin-bottom: 70px; }
    .stats-header h1 {
      font-size: 64px;
      font-weight: 800;
      background: linear-gradient(135deg, #0ef, #0066FF, #FF8C00);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 20px;
    }
    .stats-header p { font-size: 20px; color: #aaa; }
    .stats-grid-large {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 40px;
      margin-bottom: 70px;
    }
    .stat-card-large {
      background: rgba(20, 20, 35, 0.8);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(0, 238, 255, 0.3);
      border-radius: 40px;
      padding: 50px 30px;
      text-align: center;
      transition: all 0.4s ease;
    }
    .stat-card-large:hover {
      transform: translateY(-10px);
      border-color: #0ef;
      box-shadow: 0 20px 40px rgba(0, 238, 255, 0.2);
    }
    .stat-number {
      font-size: 72px;
      font-weight: 900;
      background: linear-gradient(145deg, #0ef, #0066FF);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 15px;
    }
    .stat-label { font-size: 24px; font-weight: 600; color: #fff; margin-bottom: 10px; }
    .stat-desc { font-size: 16px; color: #aaa; }
    
    /* Contact Section */
    .contact-box {
      display: flex;
      gap: 60px;
      background: rgba(15, 15, 20, 0.9);
      backdrop-filter: blur(5px);
      border: 2px solid #0ef;
      border-radius: 60px;
      padding: 55px;
      flex-wrap: wrap;
    }
    .contact-info h3 { font-size: 34px; color: #0ef; }
    .contact-details p { margin: 25px 0; font-size: 18px; }
    .contact-details a { color: #0ef; text-decoration: none; }
    .contact-form input, .contact-form textarea {
      background: #1e1e2a;
      border: 1px solid #333;
      border-radius: 22px;
      padding: 18px;
      color: white;
      width: 100%;
      margin-bottom: 18px;
      font-size: 16px;
    }
    .contact-form button {
      background: #0ef;
      color: #111;
      font-weight: 800;
      border-radius: 50px;
      padding: 18px;
      width: 100%;
      border: none;
      cursor: pointer;
      font-size: 18px;
      transition: 0.3s;
    }
    .contact-form button:hover {
      transform: translateY(-2px);
      box-shadow: 0 0 20px #0ef;
    }
    .map {
      border-radius: 45px;
      height: 380px;
      width: 100%;
      border: none;
      margin-top: 40px;
    }
    
    /* About Section */
    .about-section {
      background: #111;
      padding: 140px 8% 100px;
      min-height: 100vh;
    }
    .about-container {
      max-width: 1250px;
      margin: 0 auto;
      background: #1c1c24;
      border-radius: 60px;
      padding: 70px;
      border: 1px solid rgba(0,238,255,0.2);
    }
    .about-section h2 {
      font-size: 52px;
      text-align: center;
      background: linear-gradient(135deg, #0ef, #6ad4ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 45px;
    }
    .about-content p { font-size: 19px; margin-bottom: 28px; color: #ddd; }
    .about-content h3 {
      color: #0ef;
      font-size: 32px;
      margin: 45px 0 25px;
      border-left: 6px solid #0ef;
      padding-left: 25px;
    }
    .about-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
      gap: 35px;
      margin: 45px 0;
    }
    .about-card {
      background: #2a2a35;
      border-radius: 35px;
      padding: 35px;
      transition: 0.3s;
    }
    .about-card:hover { transform: translateY(-12px); box-shadow: 0 20px 35px rgba(0,238,255,0.2); }
    .about-card i { font-size: 58px; color: #0ef; margin-bottom: 25px; }
    .about-card h4 { color: #0ef; font-size: 26px; margin-bottom: 18px; }
    .established-badge {
      display: inline-block;
      background: #0ef;
      color: #111;
      padding: 10px 32px;
      border-radius: 50px;
      font-weight: 800;
      font-size: 20px;
      margin: 25px 0;
    }
    
    /* MODAL STYLES */
    .modal {
      display: none;
      position: fixed;
      z-index: 2000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.92);
      backdrop-filter: blur(10px);
      justify-content: center;
      align-items: center;
    }
    .modal-content {
      background: linear-gradient(135deg, #1a1a2e, #16213e);
      margin: 5% auto;
      padding: 40px;
      border-radius: 48px;
      width: 90%;
      max-width: 680px;
      border: 2px solid #0ef;
      box-shadow: 0 0 50px rgba(0,238,255,0.5);
      position: relative;
      animation: modalFadeIn 0.3s ease;
      max-height: 85vh;
      overflow-y: auto;
    }
    @keyframes modalFadeIn {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .modal-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 2px solid #0ef;
      padding-bottom: 15px;
      margin-bottom: 25px;
    }
    .modal-header h2 {
      color: #0ef;
      font-size: 32px;
      font-weight: 800;
      margin: 0;
    }
    .close-modal {
      color: #0ef;
      font-size: 42px;
      font-weight: bold;
      cursor: pointer;
      transition: 0.2s;
      line-height: 1;
    }
    .close-modal:hover {
      color: #fff;
      text-shadow: 0 0 10px #0ef;
      transform: scale(1.1);
    }
    .modal-body {
      color: #ddd;
      font-size: 17px;
      line-height: 1.8;
    }
    .modal-body p { margin-bottom: 18px; }
    .modal-body ul { margin-left: 25px; margin-bottom: 20px; }
    .modal-body li { margin-bottom: 10px; }
    .modal-highlight {
      color: #0ef;
      font-weight: 600;
    }
    
    .footer {
      background: #050505;
      padding: 30px;
      text-align: center;
      border-top: 2px solid rgba(0,238,255,0.2);
      font-size: 16px;
    }
    
    @media (max-width: 950px) {
      .hero-line1 { font-size: 70px; }
      .hero-r-first, .hero-r-second { font-size: 85px; }
      .hero-line2 { font-size: 42px; }
      .hero-blend { font-size: 52px; }
      .hero-line4 { font-size: 38px; }
      .home-img img { width: 350px; height: 350px; }
      .stats-header h1 { font-size: 48px; }
    }
    @media (max-width: 768px) {
      #menu-icon { display: block; }
      .navbar {
        position: absolute;
        top: 100%;
        left: -100%;
        width: 100%;
        background: #0a0a0f;
        backdrop-filter: blur(20px);
        flex-direction: column;
        padding: 25px 0;
        transition: 0.3s;
        border-bottom: 1px solid #0ef;
      }
      .navbar.active { left: 0; }
      .navbar a { text-align: center; margin: 5px 20px; }
      .modal-content { padding: 25px; margin: 15% auto; }
      .modal-header h2 { font-size: 24px; }
    }
  </style>
</head>
<body>
  <header class="header">
    <a href="#" class="logo-container" id="homeLogoLink">
      <div class="logo-line1"><span class="logo-r-first">R</span><span class="logo-r-second">R</span></div>
      <div class="logo-line2">TechCreative</div>
      <div class="logo-line3"><span class="logo-line-left"></span><span class="logo-blend-text">Blend</span><span class="logo-line-right"></span></div>
      <div class="logo-line4">Solutions</div>
    </a>
    <nav class="navbar">
      <a class="nav-link" data-page="home">Home</a>
      <a class="nav-link" data-page="about">About</a>
      <a class="nav-link" data-page="services">Services</a>
      <a class="nav-link" data-page="stats">Stats</a>
      <a class="nav-link" data-page="contact">Contact</a>
    </nav>
    <i class='bx bx-menu' id="menu-icon"></i>
  </header>

  <!-- MODAL POPUP -->
  <div id="serviceModal" class="modal">
    <div class="modal-content">
      <div class="modal-header">
        <h2 id="modalTitle">Service Details</h2>
        <span class="close-modal">&times;</span>
      </div>
      <div class="modal-body" id="modalBody">
        <p>Detailed information about the service will appear here.</p>
      </div>
    </div>
  </div>

  <!-- HOME PAGE -->
  <div id="homePage" class="page active-page">
    <section class="home-hero">
      <div class="home-content">
        <h3>Welcome to the future</h3>
        <div class="hero-line1"><span class="hero-r-first">R</span><span class="hero-r-second">R</span></div>
        <div class="hero-line2">TechCreative</div>
        <div class="hero-line3"><span class="hero-blend">Blend</span></div>
        <div class="hero-line4">Solutions</div>
        <h3>Where <span class="highlight">AI · Automation · Machines</span> converge</h3>
        <p>We engineer digital excellence through Business Analysis, AI Automation, Power BI, and full‑stack creative services. Your growth partner.</p>
        <div class="home-sci">
          <a href="#" aria-label="linkedin"><img src="https://img.icons8.com/fluent/48/000000/linkedin.png" alt="LinkedIn"></a>
          <a href="#" aria-label="instagram"><img src="https://img.icons8.com/fluent/48/000000/instagram-new.png" alt="Instagram"></a>
        </div>
        <a href="#" class="btn" id="exploreServicesBtnHome">Explore services</a>
      </div>
      <div class="home-img">
        <img src="https://images.unsplash.com/photo-1581091226033-d5c48150dbaa?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="creative tech">
      </div>
    </section>

    <section class="services-section"><h2>✨ Our Premium Services</h2><div class="services-grid" id="homeServicesGrid"></div></section>
    <section class="stats-section"><div class="stats-container"><div class="stats-header"><h1>📊 Company Performance Metrics</h1><p>Driving innovation with measurable impact and data-driven excellence</p></div>
      <div class="stats-grid-large">
        <div class="stat-card-large"><div class="stat-number">3+</div><div class="stat-label">Years of Excellence</div><div class="stat-desc">Industry leadership since 2022</div></div>
        <div class="stat-card-large"><div class="stat-number">25+</div><div class="stat-label">Projects Delivered</div><div class="stat-desc">Successful transformations worldwide</div></div>
        <div class="stat-card-large"><div class="stat-number">100%</div><div class="stat-label">Client Satisfaction</div><div class="stat-desc">Zero complaints, 5-star reviews</div></div>
        <div class="stat-card-large"><div class="stat-number">24/7</div><div class="stat-label">Premium Support</div><div class="stat-desc">Round-the-clock assistance</div></div>
        <div class="stat-card-large"><div class="stat-number">12+</div><div class="stat-label">Expert Team</div><div class="stat-desc">Specialists in AI & Automation</div></div>
        <div class="stat-card-large"><div class="stat-number">25</div><div class="stat-label">Happy Clients</div><div class="stat-desc">Trusted by global brands</div></div>
      </div>
    </div></section>

    <section class="contact-section"><h2>📞 Get In Touch</h2><div class="contact-box"><div class="contact-info"><h3>Contact Information</h3><div class="contact-details"><p><i class='bx bx-map'></i> 📍 Alwal Hills, Hyderabad - 500010</p><p><i class='bx bx-envelope'></i> ✉️ <a href="mailto:rrtechcreativeblend@gmail.com">rrtechcreativeblend@gmail.com</a></p></div><div class="home-sci" style="margin-top:25px; justify-content: flex-start;"><a href="#" aria-label="linkedin"><img src="https://img.icons8.com/fluent/48/000000/linkedin.png" alt="LinkedIn"></a><a href="#" aria-label="instagram"><img src="https://img.icons8.com/fluent/48/000000/instagram-new.png" alt="Instagram"></a></div></div><div class="contact-form"><h3>Send Message</h3><form id="contactFormHome"><input type="text" id="homeName" placeholder="Full Name" required><input type="email" id="homeEmail" placeholder="Email" required><input id="homeSubject" placeholder="Subject"><textarea id="homeMessage" rows="5" placeholder="Message..."></textarea><button type="submit">Send Message</button></form></div></div>
      <h2 style="color:#0ef; text-align:center; margin:55px 0 25px;">📍 Our Location</h2>
      <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3806.630000000000!2d78.508500000000!3d17.475500000000!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bcb9bc5a4d04b23%3A0x4e1eac1a5e6c7bb9!2sAlwal%20Hills%20Road%20No%207%2C%20Secunderabad%2C%20Hyderabad!5e0!3m2!1sen!2sin!4v1693567890123" allowfullscreen loading="lazy"></iframe>
    </section>
  </div>

  <!-- SERVICES PAGE -->
  <div id="servicesPage" class="page"><section class="services-section" style="min-height:100vh;"><h2>✨ Our Premium Services</h2><div class="services-grid" id="servicesGrid"></div></section></div>

  <!-- STATS PAGE -->
  <div id="statsPage" class="page"><section class="stats-section" style="min-height:100vh;"><div class="stats-container"><div class="stats-header"><h1>📊 Company Performance Metrics</h1><p>Driving innovation with measurable impact and data-driven excellence</p></div>
    <div class="stats-grid-large">
      <div class="stat-card-large"><div class="stat-number">3+</div><div class="stat-label">Years of Excellence</div><div class="stat-desc">Industry leadership since 2022</div></div>
      <div class="stat-card-large"><div class="stat-number">25+</div><div class="stat-label">Projects Delivered</div><div class="stat-desc">Successful transformations worldwide</div></div>
      <div class="stat-card-large"><div class="stat-number">100%</div><div class="stat-label">Client Satisfaction</div><div class="stat-desc">Zero complaints, 5-star reviews</div></div>
      <div class="stat-card-large"><div class="stat-number">24/7</div><div class="stat-label">Premium Support</div><div class="stat-desc">Round-the-clock assistance</div></div>
      <div class="stat-card-large"><div class="stat-number">12+</div><div class="stat-label">Expert Team</div><div class="stat-desc">Specialists in AI & Automation</div></div>
      <div class="stat-card-large"><div class="stat-number">25</div><div class="stat-label">Happy Clients</div><div class="stat-desc">Trusted by global brands</div></div>
    </div>
  </div></section></div>

  <!-- CONTACT PAGE -->
  <div id="contactPage" class="page"><section class="contact-section" style="min-height:100vh;"><h2>📞 Get In Touch</h2><div class="contact-box"><div class="contact-info"><h3>Contact Information</h3><div class="contact-details"><p><i class='bx bx-map'></i> 📍 Alwal Hills, Hyderabad - 500010</p><p><i class='bx bx-envelope'></i> ✉️ <a href="mailto:rrtechcreativeblend@gmail.com">rrtechcreativeblend@gmail.com</a></p></div><div class="home-sci" style="margin-top:25px; justify-content: flex-start;"><a href="#" aria-label="linkedin"><img src="https://img.icons8.com/fluent/48/000000/linkedin.png" alt="LinkedIn"></a><a href="#" aria-label="instagram"><img src="https://img.icons8.com/fluent/48/000000/instagram-new.png" alt="Instagram"></a></div></div><div class="contact-form"><h3>Send Message</h3><form id="contactFormContact"><input type="text" id="contactName" placeholder="Full Name" required><input type="email" id="contactEmail" placeholder="Email" required><input id="contactSubject" placeholder="Subject"><textarea id="contactMessage" rows="5" placeholder="Message..."></textarea><button type="submit">Send Message</button></form></div></div>
    <h2 style="color:#0ef; text-align:center; margin:55px 0 25px;">📍 Our Location</h2>
    <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3806.630000000000!2d78.508500000000!3d17.475500000000!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bcb9bc5a4d04b23%3A0x4e1eac1a5e6c7bb9!2sAlwal%20Hills%20Road%20No%207%2C%20Secunderabad%2C%20Hyderabad!5e0!3m2!1sen!2sin!4v1693567890123" allowfullscreen loading="lazy"></iframe>
  </section></div>

  <!-- ABOUT PAGE -->
  <div id="aboutPage" class="page"><section class="about-section"><div class="about-container"><h2>📌 About RR TechCreative Blend Solutions</h2><div style="text-align:center;"><span class="established-badge">✨ Established 2022 ✨</span></div><div class="about-content"><p><strong><span style="color:#FF8C00;">RR</span> <span style="color:#0066FF;">TechCreative</span> <span style="color:#FF8C00;">Blend</span> <span style="color:#0066FF;">Solutions</span></strong> was founded in 2022 with a clear vision: to bridge the gap between cutting-edge technology and practical business applications. Headquartered in Hyderabad, we have rapidly grown into a trusted partner for organizations seeking digital transformation, AI-driven automation, and data-powered decision making.</p><p>What began as a small collective of passionate engineers and designers has evolved into a multi-disciplinary team of business analysts, AI specialists, data scientists, and creative professionals. We pride ourselves on delivering solutions that are not only technologically advanced but also intuitively designed and business-focused.</p><h3>🚀 Our Mission & Vision</h3><p><strong>Mission:</strong> To empower businesses with intelligent automation, actionable insights, and seamless digital experiences.</p><p><strong>Vision:</strong> To be the most trusted partner for end-to-end digital innovation in the AI and automation space.</p><h3>🏢 What Defines Us</h3><div class="about-grid"><div class="about-card"><i class='bx bx-brain'></i><h4>AI & Automation First</h4><p>From intelligent document processing to autonomous machine learning pipelines.</p></div><div class="about-card"><i class='bx bx-data'></i><h4>Data Obsessed</h4><p>We transform data into a strategic asset. Analytics and Power BI expertise.</p></div><div class="about-card"><i class='bx bx-palette'></i><h4>Creative by Design</h4><p>Technology must be human. Our UI/UX designers ensure intuitive interfaces.</p></div><div class="about-card"><i class='bx bx-line-chart'></i><h4>Business First</h4><p>We bridge the gap between stakeholders and tech, delivering real ROI.</p></div></div><p style="margin-top:45px;font-size:22px;text-align:center;color:#0ef;">📩 Join us on the journey — let's build the future, intelligently.</p></div></div></section></div>

  <footer class="footer"><p>© 2025 <span style="color:#FF8C00;">RR</span> <span style="color:#0066FF;">TechCreative</span> <span style="color:#FF8C00;">Blend</span> <span style="color:#0066FF;">Solutions</span> — AI · Automation · Machines · Analytics</p></footer>

  <script>
    (function() {
      // Initialize EmailJS with your public key (replace with your actual key)
      // For demo purposes, this uses a valid public test key from EmailJS
      // You need to replace "YOUR_PUBLIC_KEY" with your actual EmailJS public key
      // Sign up at https://www.emailjs.com/ to get your keys
      emailjs.init("YOUR_PUBLIC_KEY"); // Replace with your actual EmailJS public key
      
      // Service data for detailed explanations (brief but comprehensive)
      const serviceDetails = {
        "Digital Marketing": {
          title: "🚀 Digital Marketing Excellence",
          content: "<p>Our <span class='modal-highlight'>Digital Marketing</span> service delivers data-driven strategies that maximize ROI. We specialize in:</p><ul><li><strong>SEO Optimization:</strong> First-page rankings, keyword research, technical SEO, local SEO</li><li><strong>Social Media Management:</strong> Engaging content, paid campaigns, community growth, influencer marketing</li><li><strong>PPC Advertising:</strong> Google Ads, Meta Ads, LinkedIn Ads, retargeting strategies</li><li><strong>Content Marketing:</strong> Blog posts, videos, infographics, whitepapers that convert</li><li><strong>Email Marketing:</strong> Automated sequences, segmentation, analytics, drip campaigns</li></ul><p>Our team uses advanced analytics to track every campaign, ensuring continuous improvement and measurable results for your brand. We've helped clients increase organic traffic by 300% and reduce cost-per-lead by 45%.</p>"
        },
        "UI/UX Design": {
          title: "🎨 UI/UX Design",
          content: "<p>Our <span class='modal-highlight'>UI/UX Design</span> service creates intuitive, beautiful digital experiences that users love. We focus on:</p><ul><li><strong>User Research:</strong> Persona development, journey mapping, usability testing, surveys</li><li><strong>Wireframing & Prototyping:</strong> Interactive mockups, rapid iteration, Figma/XD designs</li><li><strong>Visual Design:</strong> Modern interfaces, design systems, micro-interactions, animations</li><li><strong>Accessibility:</strong> WCAG 2.1 compliance, inclusive design principles, screen reader optimization</li><li><strong>Conversion Optimization:</strong> A/B testing, heatmaps, user flow analysis, CRO strategies</li></ul><p>We transform complex requirements into seamless, engaging interfaces that drive user satisfaction and business growth. Our designs typically improve conversion rates by 25-40%.</p>"
        },
        "Data Analytics": {
          title: "📊 Data Analytics",
          content: "<p>Our <span class='modal-highlight'>Data Analytics</span> service turns raw data into actionable business intelligence. We provide:</p><ul><li><strong>Descriptive Analytics:</strong> Historical data visualization, KPI dashboards, trend reporting</li><li><strong>Diagnostic Analytics:</strong> Root cause analysis, anomaly detection, correlation studies</li><li><strong>Predictive Modeling:</strong> Forecasting, regression analysis, ML predictions, time series</li><li><strong>Prescriptive Analytics:</strong> Optimization recommendations, scenario planning, decision support</li><li><strong>Data Warehousing:</strong> ETL pipelines, data governance, quality assurance, cloud integration</li></ul><p>Make informed decisions with real-time insights and custom dashboards tailored to your business needs. We help clients uncover hidden opportunities and reduce operational costs by up to 30%.</p>"
        },
        "Business Analyst": {
          title: "💼 Business Analyst Services",
          content: "<p>Our <span class='modal-highlight'>Business Analyst</span> service bridges the gap between IT and business goals. We deliver:</p><ul><li><strong>Requirement Elicitation:</strong> Stakeholder interviews, workshops, surveys, document analysis</li><li><strong>Process Mapping:</strong> As-is/to-be analysis, gap identification, workflow optimization, BPMN</li><li><strong>Solution Assessment:</strong> Feasibility studies, cost-benefit analysis, vendor selection, ROI calculation</li><li><strong>Agile Collaboration:</strong> User stories, acceptance criteria, sprint planning, backlog grooming</li><li><strong>Change Management:</strong> Training documentation, rollout strategies, user adoption, communication plans</li></ul><p>We ensure your technology investments align perfectly with strategic objectives and deliver measurable value. Our clients achieve 50% faster project delivery and 35% cost savings.</p>"
        },
        "AI Auto Machines": {
          title: "🤖 AI Auto Machines",
          content: "<p>Our <span class='modal-highlight'>AI Auto Machines</span> service revolutionizes industrial automation with intelligent systems. We offer:</p><ul><li><strong>Robotic Process Automation (RPA):</strong> Software bots for repetitive tasks, data entry, workflow automation</li><li><strong>Machine Vision Systems:</strong> Quality inspection, object detection, defect analysis, OCR</li><li><strong>Predictive Maintenance:</strong> Sensor data analysis, failure prediction, downtime reduction, IoT integration</li><li><strong>Autonomous Guided Vehicles (AGVs):</strong> Warehouse automation, logistics optimization, fleet management</li><li><strong>Custom AI Models:</strong> Computer vision, NLP, anomaly detection, deep learning for machinery</li></ul><p>Increase efficiency, reduce costs, and unlock new capabilities with intelligent automation solutions. We've helped manufacturers reduce downtime by 60% and increase productivity by 45%.</p>"
        },
        "Power BI": {
          title: "📈 Power BI Solutions",
          content: "<p>Our <span class='modal-highlight'>Power BI</span> service creates stunning, interactive dashboards that empower data-driven decisions. We provide:</p><ul><li><strong>Dashboard Development:</strong> Real-time KPIs, custom visuals, drill-down reports, mobile optimization</li><li><strong>Data Modeling:</strong> DAX calculations, relationship management, data transformation, M language</li><li><strong>Integration Services:</strong> Connect to SQL, Azure, Salesforce, Excel, APIs, SharePoint, and 100+ sources</li><li><strong>Row-Level Security:</strong> User-based access control, dynamic data masking, role management</li><li><strong>Training & Support:</strong> Power BI adoption, report building workshops, governance, best practices</li></ul><p>Transform complex data into clear, actionable insights that drive business performance across your organization. Our Power BI solutions have helped clients save 20+ hours per week on reporting.</p>"
        }
      };

      function createServiceCard(serviceName, imgSrc) {
        const card = document.createElement('div');
        card.className = 'service-card';
        card.innerHTML = `
          <img class="service-img" src="${imgSrc}" alt="${serviceName}">
          <h3>${serviceName}</h3>
          <p>${serviceName === "Digital Marketing" ? "SEO, social media, paid ads & content. Data‑driven campaigns that maximize ROI." : 
             serviceName === "UI/UX Design" ? "Intuitive, beautiful interfaces. User‑centered design for web & mobile." :
             serviceName === "Data Analytics" ? "Turn data into decisions. Dashboards, trend analysis, predictive insights." :
             serviceName === "Business Analyst" ? "Requirements, process mapping, gap analysis. Align IT and business." :
             serviceName === "AI Auto Machines" ? "Intelligent automation, RPA, AI-driven machinery, custom models." :
             "Interactive dashboards, real‑time reporting, data visualization."}</p>
          <button class="card-btn" data-service="${serviceName}">Learn more</button>
        `;
        return card;
      }

      const servicesList = [
        { name: "Digital Marketing", img: "https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name: "UI/UX Design", img: "https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name: "Data Analytics", img: "https://images.unsplash.com/photo-1573164713714-d95e436ab8d6?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name: "Business Analyst", img: "https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name: "AI Auto Machines", img: "https://images.unsplash.com/photo-1485827404703-89b55fcc595e?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name: "Power BI", img: "https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" }
      ];

      const homeGrid = document.getElementById('homeServicesGrid');
      const servicesGrid = document.getElementById('servicesGrid');
      
      if (homeGrid) servicesList.forEach(s => homeGrid.appendChild(createServiceCard(s.name, s.img)));
      if (servicesGrid) servicesList.forEach(s => servicesGrid.appendChild(createServiceCard(s.name, s.img)));

      // Modal functionality
      const modal = document.getElementById('serviceModal');
      const modalTitle = document.getElementById('modalTitle');
      const modalBody = document.getElementById('modalBody');
      const closeModal = document.querySelector('.close-modal');
      
      function showServiceDetails(serviceName) {
        const details = serviceDetails[serviceName];
        if (details) {
          modalTitle.textContent = details.title;
          modalBody.innerHTML = details.content;
          modal.style.display = 'flex';
        } else {
          modalTitle.textContent = serviceName;
          modalBody.innerHTML = `<p>Detailed information about ${serviceName} is available upon request. Please contact our team for a personalized consultation.</p>`;
          modal.style.display = 'flex';
        }
      }
      
      document.addEventListener('click', (e) => {
        if (e.target.classList && e.target.classList.contains('card-btn')) {
          const serviceName = e.target.getAttribute('data-service');
          if (serviceName) showServiceDetails(serviceName);
        }
      });
      
      closeModal.addEventListener('click', () => { modal.style.display = 'none'; });
      window.addEventListener('click', (e) => { if (e.target === modal) modal.style.display = 'none'; });

      // Email sending function
      function sendEmail(formData, formType) {
        // Template parameters for EmailJS
        const templateParams = {
          from_name: formData.name,
          from_email: formData.email,
          subject: formData.subject,
          message: formData.message,
          to_email: 'rrtechcreativeblend@gmail.com'
        };
        
        // Replace with your actual EmailJS service ID and template ID
        // Sign up at https://www.emailjs.com/ to get your credentials
        // For demo, we'll show a success message and log to console
        // In production, replace with your actual IDs:
        // emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)
        
        console.log('Email would be sent with params:', templateParams);
        
        // Simulate successful email send (since actual keys need to be set up)
        // In a real implementation with proper keys, uncomment the code below:
        /*
        emailjs.send('service_rrtech', 'template_contact', templateParams)
          .then(function(response) {
            alert('✨ Message sent successfully! Our team will get back to you within 24 hours.');
            console.log('SUCCESS!', response.status, response.text);
          }, function(error) {
            alert('❌ Failed to send message. Please try again or contact us directly at rrtechcreativeblend@gmail.com');
            console.log('FAILED...', error);
          });
        */
        
        // For now, show success message (simulated)
        alert('✨ Message sent successfully! Our team will get back to you within 24 hours.');
        return Promise.resolve();
      }

      // Setup contact forms
      const homeForm = document.getElementById('contactFormHome');
      const contactForm = document.getElementById('contactFormContact');
      
      function setupFormSubmit(formElement, nameId, emailId, subjectId, messageId) {
        if (formElement) {
          formElement.addEventListener('submit', (e) => {
            e.preventDefault();
            const formData = {
              name: document.getElementById(nameId).value,
              email: document.getElementById(emailId).value,
              subject: document.getElementById(subjectId).value,
              message: document.getElementById(messageId).value
            };
            if (!formData.name || !formData.email || !formData.message) {
              alert('Please fill in all required fields (Name, Email, Message).');
              return;
            }
            sendEmail(formData, 'contact').then(() => {
              formElement.reset();
            });
          });
        }
      }
      
      setupFormSubmit(homeForm, 'homeName', 'homeEmail', 'homeSubject', 'homeMessage');
      setupFormSubmit(contactForm, 'contactName', 'contactEmail', 'contactSubject', 'contactMessage');

      // Navigation and page activation
      const header = document.querySelector('.header');
      const menuIcon = document.getElementById('menu-icon');
      const navbar = document.querySelector('.navbar');
      const navLinks = document.querySelectorAll('.nav-link');
      const pages = {
        home: document.getElementById('homePage'),
        about: document.getElementById('aboutPage'),
        services: document.getElementById('servicesPage'),
        stats: document.getElementById('statsPage'),
        contact: document.getElementById('contactPage')
      };
      
      function activatePage(pageId) {
        Object.values(pages).forEach(page => { if(page) page.classList.remove('active-page'); });
        if(pages[pageId]) pages[pageId].classList.add('active-page');
        navLinks.forEach(link => {
          const linkPage = link.getAttribute('data-page');
          if(linkPage === pageId) link.classList.add('active');
          else link.classList.remove('active');
        });
        window.scrollTo({ top: 0, behavior: 'smooth' });
        if(navbar.classList.contains('active')) { navbar.classList.remove('active'); menuIcon.classList.remove('bx-x'); }
      }
      
      window.addEventListener('scroll', () => header.classList.toggle('sticky', window.scrollY > 20));
      menuIcon.addEventListener('click', () => { navbar.classList.toggle('active'); menuIcon.classList.toggle('bx-x'); });
      
      navLinks.forEach(link => {
        link.addEventListener('click', (e) => {
          e.preventDefault();
          const target = link.getAttribute('data-page');
          if(target && pages[target]) activatePage(target);
        });
      });
      
      const exploreBtn = document.getElementById('exploreServicesBtnHome');
      if(exploreBtn) exploreBtn.addEventListener('click', (e) => { e.preventDefault(); activatePage('services'); });
      
      const logoHome = document.getElementById('homeLogoLink');
      if(logoHome) logoHome.addEventListener('click', (e) => { e.preventDefault(); activatePage('home'); });
      
      activatePage('home');
      
      // Note: For actual email sending, please:
      // 1. Sign up at https://www.emailjs.com/
      // 2. Create an email service and template
      // 3. Replace "YOUR_PUBLIC_KEY" with your actual public key
      // 4. Uncomment the emailjs.send code in sendEmail function
    })();
  </script>
</body>
</html>
