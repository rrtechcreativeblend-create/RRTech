<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
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
      -webkit-font-smoothing: antialiased;
    }
    /* ----- HEADER (PREMIUM GLASS) ----- */
    .header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(8, 12, 18, 0.96);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-bottom: 2px solid rgba(0, 238, 255, 0.6);
      padding: 18px 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
      transition: 0.3s;
      box-shadow: 0 4px 25px rgba(0, 238, 255, 0.2);
    }
    .header.sticky {
      padding: 12px 5%;
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
      flex-shrink: 0;
    }
    .logo-container:hover { transform: scale(1.02); }
    
    .logo-line1 {
      font-size: clamp(32px, 8vw, 72px);
      font-weight: 900;
      letter-spacing: -4px;
      margin-bottom: 6px;
      display: flex;
      gap: 0;
      justify-content: center;
      line-height: 1;
      position: relative;
    }
    .logo-r-first {
      font-size: clamp(38px, 9vw, 82px);
      font-weight: 900;
      background: linear-gradient(135deg, #FF8C00 50%, #0066FF 50%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      letter-spacing: -2px;
      display: inline-block;
    }
    .logo-r-second {
      font-size: clamp(38px, 9vw, 82px);
      font-weight: 900;
      background: linear-gradient(135deg, #0066FF 50%, #FF8C00 50%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-left: -8px;
      display: inline-block;
    }
    .logo-line1::after {
      content: '';
      position: absolute;
      bottom: 8px;
      left: 48%;
      transform: translateX(-50%);
      width: 45px;
      height: 3px;
      background: linear-gradient(90deg, #FF8C00, #0ef, #0066FF);
      border-radius: 3px;
      opacity: 0.8;
    }
    
    .logo-line2 {
      font-size: clamp(18px, 5vw, 32px);
      font-weight: 700;
      letter-spacing: 1px;
      margin-bottom: 8px;
      background: linear-gradient(120deg, #0066FF, #4a90e2, #0ef);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    
    .logo-line3 {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 12px;
      margin-bottom: 6px;
      width: 100%;
    }
    .logo-line-left, .logo-line-right {
      width: 40px;
      height: 3px;
      background: linear-gradient(90deg, transparent, #0ef, #0ef);
      border-radius: 3px;
      transition: all 0.3s ease;
    }
    .logo-line-right {
      background: linear-gradient(90deg, #0ef, #0ef, transparent);
    }
    .logo-blend-text {
      font-size: clamp(18px, 5vw, 36px);
      font-weight: 800;
      letter-spacing: 2px;
      background: linear-gradient(145deg, #FF8C00, #FFB347);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      padding: 0 6px;
    }
    
    .logo-line4 {
      font-size: clamp(16px, 4.5vw, 34px);
      font-weight: 800;
      letter-spacing: 3px;
      margin-top: 4px;
      background: linear-gradient(135deg, #0ef, #0066FF, #3a86ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      display: inline-block;
    }
    
    .navbar {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
      justify-content: flex-end;
    }
    .navbar a {
      padding: 8px 18px;
      font-size: 15px;
      font-weight: 600;
      color: #eef5ff;
      text-decoration: none;
      border-radius: 40px;
      transition: 0.25s;
      cursor: pointer;
      background: rgba(255,255,255,0.05);
      white-space: nowrap;
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
    
    /* Page visibility */
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
      padding: 140px 5% 80px;
      flex-wrap: wrap;
      gap: 40px;
    }
    .home-content { max-width: 700px; flex: 1; }
    .home-content h3 { font-size: clamp(18px, 4vw, 30px); font-weight: 500; color: #ccf0ff; }
    .hero-line1 {
      font-size: clamp(48px, 12vw, 110px);
      font-weight: 900;
      line-height: 1.05;
      letter-spacing: 2px;
      margin: 15px 0 5px;
      display: flex;
      gap: 0;
      justify-content: center;
    }
    .hero-r-first {
      font-size: clamp(55px, 14vw, 130px);
      font-weight: 900;
      background: linear-gradient(135deg, #FF8C00 50%, #0066FF 50%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .hero-r-second {
      font-size: clamp(55px, 14vw, 130px);
      font-weight: 900;
      background: linear-gradient(135deg, #0066FF 50%, #FF8C00 50%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-left: -8px;
    }
    .hero-line2 {
      font-size: clamp(28px, 7vw, 58px);
      font-weight: 800;
      line-height: 1.2;
      letter-spacing: 2px;
      margin: 10px 0 20px;
      background: linear-gradient(120deg, #0066FF, #4a90e2, #0ef);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-align: center;
    }
    .hero-line3 {
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 25px 0;
      gap: 15px;
      flex-wrap: wrap;
    }
    .hero-line3::before, .hero-line3::after {
      content: "";
      flex: 1;
      height: 3px;
      background: linear-gradient(90deg, transparent, #0ef, #0ef, transparent);
      border-radius: 4px;
    }
    .hero-blend {
      font-size: clamp(32px, 8vw, 76px);
      font-weight: 900;
      letter-spacing: 4px;
      padding: 0 15px;
      background: linear-gradient(145deg, #FF8C00, #FFB347);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .hero-line4 {
      font-size: clamp(24px, 6vw, 54px);
      font-weight: 800;
      line-height: 1.2;
      letter-spacing: 3px;
      margin: 15px 0;
      text-align: center;
      background: linear-gradient(135deg, #0ef, #0066FF, #3a86ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .home-content p { font-size: clamp(16px, 3vw, 20px); margin: 30px 0 35px; color: #d0d0d0; }
    .highlight { color: #0ef; font-weight: 600; }
    .home-sci { display: flex; gap: 20px; margin: 30px 0 25px; justify-content: center; flex-wrap: wrap; }
    .home-sci a img { width: 48px; height: 48px; border-radius: 50%; background: #fff; transition: 0.3s; }
    .home-sci a:hover img { transform: translateY(-6px) scale(1.05); box-shadow: 0 0 0 3px #0ef; }
    .btn {
      display: inline-block;
      padding: 14px 36px;
      background: linear-gradient(145deg, #0ef, #0ac);
      color: #111;
      font-weight: 700;
      font-size: clamp(16px, 4vw, 20px);
      border-radius: 60px;
      text-decoration: none;
      box-shadow: 0 10px 25px rgba(0, 239, 255, 0.4);
      transition: 0.3s;
      cursor: pointer;
      border: none;
    }
    .btn:hover { transform: translateY(-5px); box-shadow: 0 25px 35px rgba(0, 238, 255, 0.5); }
    .home-img img {
      width: min(400px, 80vw);
      height: auto;
      aspect-ratio: 1/1;
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
    
    /* Sections */
    .services-section, .stats-section, .contact-section {
      padding: 120px 5% 90px;
    }
    .services-section { background: linear-gradient(135deg, #0a0a0f, #0f0f1a); }
    .stats-section { background: linear-gradient(135deg, #0a0a0f 0%, #0f0f1a 100%); }
    .contact-section { background: radial-gradient(circle at 30% 30%, #112, #020202); }
    
    .services-section h2, .stats-section h2, .contact-section h2 {
      font-size: clamp(32px, 8vw, 52px);
      text-align: center;
      background: linear-gradient(135deg, #0ef, #6ad4ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 50px;
      font-weight: 800;
    }
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 35px;
    }
    .service-card {
      background: rgba(20, 20, 30, 0.7);
      backdrop-filter: blur(6px);
      border: 1px solid rgba(0, 238, 255, 0.2);
      border-radius: 36px;
      padding: 30px 24px;
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
      height: 200px;
      object-fit: cover;
      border-radius: 28px;
      margin-bottom: 24px;
      border: 2px solid #0ef;
    }
    .service-card h3 { font-size: clamp(22px, 5vw, 28px); color: #0ef; margin-bottom: 18px; }
    .service-card p { font-size: 15px; color: #ddd; margin-bottom: 28px; flex: 1; }
    .card-btn {
      align-self: flex-start;
      padding: 12px 28px;
      background: transparent;
      border: 2px solid #0ef;
      border-radius: 50px;
      color: #0ef;
      font-weight: 700;
      cursor: pointer;
      transition: 0.3s;
    }
    .card-btn:hover { background: #0ef; color: #111; box-shadow: 0 0 25px #0ef; }
    
    /* Stats */
    .stats-container { max-width: 1400px; margin: 0 auto; }
    .stats-header h1 {
      font-size: clamp(32px, 8vw, 64px);
      font-weight: 800;
      background: linear-gradient(135deg, #0ef, #0066FF, #FF8C00);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 20px;
    }
    .stats-grid-large {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 35px;
    }
    .stat-card-large {
      background: rgba(20, 20, 35, 0.8);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(0, 238, 255, 0.3);
      border-radius: 40px;
      padding: 40px 20px;
      text-align: center;
      transition: all 0.4s ease;
    }
    .stat-number { font-size: clamp(42px, 8vw, 72px); font-weight: 900; background: linear-gradient(145deg, #0ef, #0066FF); -webkit-background-clip: text; background-clip: text; color: transparent; }
    .stat-label { font-size: clamp(18px, 4vw, 24px); font-weight: 600; color: #fff; margin: 12px 0 8px; }
    
    /* Contact - iOS safe & auto wrap */
    .contact-box {
      display: flex;
      gap: 45px;
      background: rgba(15, 15, 20, 0.9);
      backdrop-filter: blur(5px);
      border: 2px solid #0ef;
      border-radius: 60px;
      padding: 40px 35px;
      flex-wrap: wrap;
    }
    .contact-info, .contact-form {
      flex: 1 1 280px;
    }
    .contact-info h3 { font-size: clamp(24px, 6vw, 34px); color: #0ef; margin-bottom: 20px; }
    .contact-details p {
      margin: 18px 0;
      font-size: clamp(15px, 4vw, 18px);
      word-break: break-word;
      display: flex;
      align-items: center;
      gap: 12px;
      flex-wrap: wrap;
    }
    .contact-details a {
      color: #0ef;
      text-decoration: none;
      word-break: break-all;
    }
    .contact-form input, .contact-form textarea {
      background: #1e1e2a;
      border: 1px solid #333;
      border-radius: 22px;
      padding: 16px 18px;
      color: white;
      width: 100%;
      margin-bottom: 18px;
      font-size: 16px;
      font-family: inherit;
    }
    .contact-form button {
      background: #0ef;
      color: #111;
      font-weight: 800;
      border-radius: 50px;
      padding: 16px;
      width: 100%;
      border: none;
      cursor: pointer;
      font-size: 18px;
      transition: 0.3s;
    }
    .map {
      border-radius: 45px;
      height: 350px;
      width: 100%;
      border: none;
      margin-top: 50px;
    }
    
    /* About Page */
    .about-section {
      background: #111;
      padding: 140px 5% 100px;
      min-height: 100vh;
    }
    .about-container {
      max-width: 1250px;
      margin: 0 auto;
      background: #1c1c24;
      border-radius: 60px;
      padding: 50px 40px;
      border: 1px solid rgba(0,238,255,0.2);
    }
    .about-container h2 { font-size: clamp(32px, 8vw, 52px); text-align: center; background: linear-gradient(135deg, #0ef, #6ad4ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; margin-bottom: 35px; }
    .about-content p { font-size: clamp(16px, 3vw, 19px); margin-bottom: 25px; color: #ddd; }
    .about-content h3 { color: #0ef; font-size: clamp(24px, 5vw, 32px); margin: 40px 0 20px; border-left: 6px solid #0ef; padding-left: 20px; }
    .about-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 30px;
      margin: 40px 0;
    }
    .about-card {
      background: #2a2a35;
      border-radius: 35px;
      padding: 30px;
      transition: 0.3s;
    }
    .about-card i { font-size: 52px; color: #0ef; margin-bottom: 20px; }
    .about-card h4 { color: #0ef; font-size: 24px; margin-bottom: 15px; }
    .established-badge { display: inline-block; background: #0ef; color: #111; padding: 8px 28px; border-radius: 50px; font-weight: 800; font-size: 18px; margin: 20px 0; }
    
    /* Modal */
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
      margin: 20px;
      padding: 30px;
      border-radius: 48px;
      width: 90%;
      max-width: 680px;
      border: 2px solid #0ef;
      box-shadow: 0 0 50px rgba(0,238,255,0.5);
      max-height: 85vh;
      overflow-y: auto;
    }
    .modal-header { display: flex; justify-content: space-between; align-items: center; border-bottom: 2px solid #0ef; padding-bottom: 12px; margin-bottom: 20px; flex-wrap: wrap; }
    .modal-header h2 { color: #0ef; font-size: clamp(22px, 5vw, 32px); font-weight: 800; }
    .close-modal { color: #0ef; font-size: 42px; cursor: pointer; line-height: 1; }
    .modal-body { color: #ddd; font-size: 16px; line-height: 1.7; }
    .modal-body ul { margin-left: 20px; margin-bottom: 20px; }
    .footer { background: #050505; padding: 25px; text-align: center; border-top: 2px solid rgba(0,238,255,0.2); font-size: 14px; }
    
    /* Responsive adjustments */
    @media (max-width: 850px) {
      .header { padding: 15px 5%; }
      .navbar a { padding: 6px 14px; font-size: 13px; white-space: nowrap; }
      #menu-icon { display: block; }
      .navbar {
        position: absolute;
        top: 100%;
        left: -100%;
        width: 100%;
        background: rgba(0,0,0,0.95);
        backdrop-filter: blur(20px);
        flex-direction: column;
        padding: 20px 0;
        transition: 0.3s;
        border-bottom: 1px solid #0ef;
        gap: 12px;
      }
      .navbar.active { left: 0; }
      .navbar a { text-align: center; margin: 5px 20px; white-space: normal; font-size: 16px; }
      .contact-box { padding: 30px 20px; }
      .about-container { padding: 30px 20px; }
    }
    @media (max-width: 550px) {
      .home-hero { padding-top: 130px; text-align: center; justify-content: center; }
      .home-img { margin-top: 20px; }
      .services-grid { grid-template-columns: 1fr; }
      .stats-grid-large { grid-template-columns: 1fr; }
      .contact-box { flex-direction: column; }
      .modal-content { padding: 20px; }
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

  <!-- MODAL -->
  <div id="serviceModal" class="modal">
    <div class="modal-content">
      <div class="modal-header"><h2 id="modalTitle">Service Details</h2><span class="close-modal">&times;</span></div>
      <div class="modal-body" id="modalBody"><p>Detailed info.</p></div>
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
        <div class="home-sci"><a href="#"><img src="https://img.icons8.com/fluent/48/000000/linkedin.png" alt="LinkedIn"></a><a href="#"><img src="https://img.icons8.com/fluent/48/000000/instagram-new.png" alt="Instagram"></a></div>
        <a href="#" class="btn" id="exploreServicesBtnHome">Explore services</a>
      </div>
      <div class="home-img"><img src="https://images.unsplash.com/photo-1581091226033-d5c48150dbaa?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="creative tech"></div>
    </section>
    <section class="services-section"><h2>✨ Our Premium Services</h2><div class="services-grid" id="homeServicesGrid"></div></section>
    <section class="stats-section"><div class="stats-container"><div class="stats-header"><h1>📊 Performance Metrics</h1><p>Driving innovation with measurable impact</p></div><div class="stats-grid-large" id="statsPreview"></div></div></section>
    <section class="contact-section"><h2>📞 Get In Touch</h2><div class="contact-box"><div class="contact-info"><h3>Contact Info</h3><div class="contact-details"><p><i class='bx bx-map'></i> 📍 Alwal Hills, Hyderabad - 500010</p><p><i class='bx bx-envelope'></i> ✉️ <a href="mailto:rrtechcreativeblend@gmail.com">rrtechcreativeblend@gmail.com</a></p></div><div class="home-sci" style="justify-content: flex-start;"><a href="#"><img src="https://img.icons8.com/fluent/48/000000/linkedin.png" alt="LinkedIn"></a><a href="#"><img src="https://img.icons8.com/fluent/48/000000/instagram-new.png" alt="Instagram"></a></div></div><div class="contact-form"><h3>Send Message</h3><form id="contactFormHome"><input type="text" id="homeName" placeholder="Full Name" required><input type="email" id="homeEmail" placeholder="Email" required><input id="homeSubject" placeholder="Subject"><textarea id="homeMessage" rows="4" placeholder="Message..."></textarea><button type="submit">Send Message</button></form></div></div>
      <h2 style="color:#0ef; text-align:center; margin:55px 0 20px;">📍 Our Location</h2>
      <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3806.630000000000!2d78.508500000000!3d17.475500000000!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bcb9bc5a4d04b23%3A0x4e1eac1a5e6c7bb9!2sAlwal%20Hills%20Road%20No%207%2C%20Secunderabad%2C%20Hyderabad!5e0!3m2!1sen!2sin!4v1693567890123" allowfullscreen loading="lazy"></iframe>
    </section>
  </div>

  <!-- SERVICES PAGE -->
  <div id="servicesPage" class="page"><section class="services-section" style="min-height:100vh;"><h2>✨ Our Premium Services</h2><div class="services-grid" id="servicesGrid"></div></section></div>

  <!-- STATS PAGE -->
  <div id="statsPage" class="page"><section class="stats-section"><div class="stats-container"><div class="stats-header"><h1>📊 Company Performance Metrics</h1><p>Driving innovation with data-driven excellence</p></div><div class="stats-grid-large" id="fullStatsGrid"></div></div></section></div>

  <!-- CONTACT PAGE (standalone, auto-wrap) -->
  <div id="contactPage" class="page"><section class="contact-section"><h2>📞 Get In Touch</h2><div class="contact-box"><div class="contact-info"><h3>Contact Information</h3><div class="contact-details"><p><i class='bx bx-map'></i> 📍 Alwal Hills, Hyderabad - 500010</p><p><i class='bx bx-envelope'></i> ✉️ <a href="mailto:rrtechcreativeblend@gmail.com">rrtechcreativeblend@gmail.com</a></p></div><div class="home-sci" style="justify-content: flex-start;"><a href="#"><img src="https://img.icons8.com/fluent/48/000000/linkedin.png" alt="LinkedIn"></a><a href="https://www.linkedin.com/in/rr-techcreativeblendsolutions-3b1157404/ "><img src="https://img.icons8.com/fluent/48/000000/instagram-new.png" alt="Instagram"></a></div></div><div class="contact-form"><h3>Send Message</h3><form id="contactFormContact"><input type="text" id="contactName" placeholder="Full Name" required><input type="email" id="contactEmail" placeholder="Email" required><input id="contactSubject" placeholder="Subject"><textarea id="contactMessage" rows="4" placeholder="Message..."></textarea><button type="submit">Send Message</button></form></div></div>
    <h2 style="color:#0ef; text-align:center; margin:55px 0 20px;">📍 Our Location</h2><iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3806.630000000000!2d78.508500000000!3d17.475500000000!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bcb9bc5a4d04b23%3A0x4e1eac1a5e6c7bb9!2sAlwal%20Hills%20Road%20No%207%2C%20Secunderabad%2C%20Hyderabad!5e0!3m2!1sen!2sin!4v1693567890123" allowfullscreen loading="lazy"></iframe>
  </section></div>

  <!-- ABOUT PAGE -->
  <div id="aboutPage" class="page"><section class="about-section"><div class="about-container"><h2>📌 About RR TechCreative Blend</h2><div style="text-align:center;"><span class="established-badge">✨ Established 2022 ✨</span></div><div class="about-content"><p><strong><span style="color:#FF8C00;">RR</span> <span style="color:#0066FF;">TechCreative</span> <span style="color:#FF8C00;">Blend</span> <span style="color:#0066FF;">Solutions</span></strong> was founded in 2022 with a clear vision: to bridge cutting-edge technology and practical business applications. Headquartered in Hyderabad, we deliver AI-driven automation, data-powered decisions, and creative digital solutions.</p><h3>🚀 Our Mission & Vision</h3><p><strong>Mission:</strong> Empower businesses with intelligent automation, actionable insights, and seamless digital experiences.<br><strong>Vision:</strong> Most trusted partner for end-to-end digital innovation.</p><h3>🏆 What Defines Us</h3><div class="about-grid"><div class="about-card"><i class='bx bx-brain'></i><h4>AI & Automation First</h4><p>Intelligent document processing, RPA, ML pipelines.</p></div><div class="about-card"><i class='bx bx-data'></i><h4>Data Obsessed</h4><p>Power BI, advanced analytics, data strategy.</p></div><div class="about-card"><i class='bx bx-palette'></i><h4>Creative by Design</h4><p>UI/UX that delights and converts.</p></div><div class="about-card"><i class='bx bx-line-chart'></i><h4>Business First</h4><p>Real ROI, bridging stakeholders and tech.</p></div></div><p style="text-align:center;color:#0ef;">📩 Join us — let's build the future, intelligently.</p></div></div></section></div>

  <footer class="footer"><p>© 2025 <span style="color:#FF8C00;">RR</span> <span style="color:#0066FF;">TechCreative</span> <span style="color:#FF8C00;">Blend</span> <span style="color:#0066FF;">Solutions</span> — AI · Automation · Analytics</p></footer>

  <script>
    (function(){
      emailjs.init("YOUR_PUBLIC_KEY"); // Replace with actual EmailJS public key for production
      const serviceDetails = {
        "Digital Marketing":{title:"🚀 Digital Marketing Excellence",content:"<p><span class='modal-highlight'>Digital Marketing</span>: SEO, social media, PPC, content & email marketing. Data-driven ROI maximization.</p><ul><li>SEO: first-page rankings, technical audits</li><li>Social Media: paid campaigns, community growth</li><li>PPC: Google/Meta Ads, retargeting</li><li>Email automation, drip campaigns</li></ul>"},
        "UI/UX Design":{title:"🎨 UI/UX Design",content:"<p>User research, wireframing, prototyping, visual design, accessibility, conversion optimization. Intuitive interfaces loved by users.</p>"},
        "Data Analytics":{title:"📊 Data Analytics",content:"<p>Descriptive, diagnostic, predictive & prescriptive analytics. Custom dashboards, data warehousing, real-time insights.</p>"},
        "Business Analyst":{title:"💼 Business Analyst",content:"<p>Requirement elicitation, process mapping, solution assessment, agile collaboration, change management. Bridge IT & business goals.</p>"},
        "AI Auto Machines":{title:"🤖 AI Auto Machines",content:"<p>RPA, machine vision, predictive maintenance, AGVs, custom AI models. Reduce downtime, boost efficiency.</p>"},
        "Power BI":{title:"📈 Power BI Solutions",content:"<p>Interactive dashboards, DAX modeling, data integration (100+ sources), row-level security, training. Turn data into decisions.</p>"}
      };
      const statsData = [
        {num:"3+",label:"Years of Excellence",desc:"Industry leadership since 2022"},
        {num:"25+",label:"Projects Delivered",desc:"Successful transformations"},
        {num:"100%",label:"Client Satisfaction",desc:"Zero complaints, 5-star reviews"},
        {num:"24/7",label:"Premium Support",desc:"Round-the-clock assistance"},
        {num:"12+",label:"Expert Team",desc:"AI & Automation specialists"},
        {num:"25",label:"Happy Clients",desc:"Trusted by global brands"}
      ];
      function buildStatsGrid(containerId){
        const container = document.getElementById(containerId);
        if(!container) return;
        container.innerHTML = "";
        statsData.forEach(s=>{
          const div = document.createElement('div'); div.className = 'stat-card-large';
          div.innerHTML = `<div class="stat-number">${s.num}</div><div class="stat-label">${s.label}</div><div class="stat-desc">${s.desc}</div>`;
          container.appendChild(div);
        });
      }
      function createServiceCard(serviceName, imgSrc){
        const card = document.createElement('div'); card.className = 'service-card';
        card.innerHTML = `<img class="service-img" src="${imgSrc}" alt="${serviceName}"><h3>${serviceName}</h3><p>${serviceName === "Digital Marketing" ? "Data-driven campaigns, SEO, social & PPC." : serviceName === "UI/UX Design" ? "Intuitive interfaces, user-centered design." : serviceName === "Data Analytics" ? "Turn data into decisions with dashboards." : serviceName === "Business Analyst" ? "Align IT & business, process optimization." : serviceName === "AI Auto Machines" ? "Intelligent automation & RPA solutions." : "Real-time dashboards, Power BI expertise."}</p><button class="card-btn" data-service="${serviceName}">Learn more</button>`;
        return card;
      }
      const servicesList = [
        { name:"Digital Marketing", img:"https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name:"UI/UX Design", img:"https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name:"Data Analytics", img:"https://images.unsplash.com/photo-1573164713714-d95e436ab8d6?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name:"Business Analyst", img:"https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name:"AI Auto Machines", img:"https://images.unsplash.com/photo-1485827404703-89b55fcc595e?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" },
        { name:"Power BI", img:"https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" }
      ];
      const homeGrid = document.getElementById('homeServicesGrid');
      const servicesGrid = document.getElementById('servicesGrid');
      if(homeGrid) servicesList.forEach(s=>homeGrid.appendChild(createServiceCard(s.name,s.img)));
      if(servicesGrid) servicesList.forEach(s=>servicesGrid.appendChild(createServiceCard(s.name,s.img)));
      buildStatsGrid('statsPreview');
      buildStatsGrid('fullStatsGrid');
      
      // modal
      const modal = document.getElementById('serviceModal');
      const modalTitle = document.getElementById('modalTitle');
      const modalBody = document.getElementById('modalBody');
      const closeModal = document.querySelector('.close-modal');
      document.addEventListener('click',(e)=>{
        if(e.target.classList?.contains('card-btn')){
          const sn = e.target.getAttribute('data-service');
          if(serviceDetails[sn]){ modalTitle.textContent=serviceDetails[sn].title; modalBody.innerHTML=serviceDetails[sn].content; }
          else { modalTitle.textContent=sn; modalBody.innerHTML=`<p>Contact us for custom ${sn} solutions.</p>`; }
          modal.style.display='flex';
        }
      });
      closeModal.onclick = ()=> modal.style.display='none';
      window.onclick = e=>{ if(e.target===modal) modal.style.display='none'; };
      
      // Email simulation (actual integration placeholder)
      function sendEmailSim(formData){
        console.log("Email send:",formData);
        alert("✨ Message sent! Our team will respond within 24 hours. (Demo mode)");
        return Promise.resolve();
      }
      function setupForm(form, nameId,emailId,subjectId,msgId){
        if(!form) return;
        form.addEventListener('submit',(e)=>{
          e.preventDefault();
          const data = { name:document.getElementById(nameId).value, email:document.getElementById(emailId).value, subject:document.getElementById(subjectId).value, message:document.getElementById(msgId).value };
          if(!data.name||!data.email||!data.message){ alert("Please fill required fields."); return; }
          sendEmailSim(data).then(()=>form.reset());
        });
      }
      setupForm(document.getElementById('contactFormHome'),'homeName','homeEmail','homeSubject','homeMessage');
      setupForm(document.getElementById('contactFormContact'),'contactName','contactEmail','contactSubject','contactMessage');
      
      // navigation
      const header=document.querySelector('.header');
      const menuIcon=document.getElementById('menu-icon');
      const navbar=document.querySelector('.navbar');
      const navLinks=document.querySelectorAll('.nav-link');
      const pages={home:document.getElementById('homePage'),about:document.getElementById('aboutPage'),services:document.getElementById('servicesPage'),stats:document.getElementById('statsPage'),contact:document.getElementById('contactPage')};
      function activatePage(pageId){
        Object.values(pages).forEach(p=>{if(p)p.classList.remove('active-page');});
        if(pages[pageId])pages[pageId].classList.add('active-page');
        navLinks.forEach(l=>{if(l.getAttribute('data-page')===pageId)l.classList.add('active');else l.classList.remove('active');});
        window.scrollTo({top:0,behavior:'smooth'});
        if(navbar.classList.contains('active')){navbar.classList.remove('active');menuIcon.classList.remove('bx-x');}
      }
      window.addEventListener('scroll',()=>header.classList.toggle('sticky',window.scrollY>20));
      menuIcon.addEventListener('click',()=>{navbar.classList.toggle('active');menuIcon.classList.toggle('bx-x');});
      navLinks.forEach(link=>{link.addEventListener('click',(e)=>{e.preventDefault();activatePage(link.getAttribute('data-page'));});});
      document.getElementById('exploreServicesBtnHome')?.addEventListener('click',(e)=>{e.preventDefault();activatePage('services');});
      document.getElementById('homeLogoLink')?.addEventListener('click',(e)=>{e.preventDefault();activatePage('home');});
      activatePage('home');
    })();
  </script>
</body>
</html>
