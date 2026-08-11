<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Kebre Institute for Mind & Enterprise</title>
  <meta name="description" content="Kebre Institute for Mind & Enterprise — Premier center for leadership, mindset development, strategic enterprise consulting, and executive training based in Addis Ababa, Ethiopia.">

  <!-- Favicon (inline SVG using brand colors) -->
  <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Crect width='100' height='100' fill='%230b1f3a'/%3E%3Ctext x='50' y='68' font-family='Georgia, serif' font-size='56' font-weight='bold' fill='%23c9a227' text-anchor='middle'%3EK%3C/text%3E%3C/svg%3E">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', Arial, Helvetica, sans-serif;
      line-height: 1.6;
      color: #172033;
      background: #ffffff;
      -webkit-font-smoothing: antialiased;
    }

    :root {
      --navy: #0b1f3a;
      --blue: #153d6f;
      --gold: #c9a227;
      --gold-light: #e0bb39;
      --light: #f5f7fa;
      --white: #ffffff;
      --text: #172033;
      --muted: #687386;
      --serif: 'Cormorant Garamond', Georgia, serif;
      --sans: 'Inter', Arial, sans-serif;
    }

    /* NAVIGATION */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(11, 31, 58, 0.94);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      padding: 18px 7%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-bottom: 1px solid rgba(201, 162, 39, 0.15);
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 12px;
      color: white;
      font-size: 20px;
      font-weight: 700;
      letter-spacing: 2px;
      text-decoration: none;
    }

    .logo-mark {
      width: 42px;
      height: 42px;
      background: var(--gold);
      border-radius: 4px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: var(--serif);
      font-weight: 700;
      font-size: 26px;
      color: var(--navy);
      box-shadow: 0 4px 12px rgba(201, 162, 39, 0.3);
    }

    .logo-text {
      display: flex;
      flex-direction: column;
      line-height: 1;
    }

    .logo-text .primary {
      font-weight: 800;
      font-size: 16px;
      letter-spacing: 3px;
    }

    .logo-text .secondary {
      color: var(--gold);
      font-size: 10px;
      letter-spacing: 4px;
      margin-top: 4px;
      font-weight: 500;
    }

    .nav-links {
      display: flex;
      list-style: none;
      gap: 36px;
    }

    .nav-links a {
      color: white;
      text-decoration: none;
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      transition: 0.3s;
      position: relative;
    }

    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -6px;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--gold);
      transition: width 0.3s;
    }

    .nav-links a:hover {
      color: var(--gold);
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .menu-btn {
      display: none;
      color: white;
      font-size: 28px;
      cursor: pointer;
      background: none;
      border: none;
    }

    /* HERO */
    .hero {
      min-height: 100vh;
      padding: 150px 7% 80px;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
      color: white;
      background: var(--navy);
    }

    .hero::before {
      content: '';
      position: absolute;
      inset: 0;
      background:
        linear-gradient(135deg, rgba(11, 31, 58, 0.88) 0%, rgba(11, 31, 58, 0.75) 50%, rgba(21, 61, 111, 0.65) 100%),
        url('https://images.unsplash.com/photo-1573164713714-d95e436ab8d6?w=1920&q=80') center/cover;
      z-index: 0;
    }

    .hero-content {
      max-width: 850px;
      position: relative;
      z-index: 1;
      animation: fadeUp 1s ease-out;
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .hero-label {
      color: var(--gold);
      font-size: 14px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 4px;
      margin-bottom: 25px;
      display: flex;
      align-items: center;
      gap: 15px;
    }

    .hero-label::before {
      content: '';
      width: 40px;
      height: 1px;
      background: var(--gold);
    }

    .hero h1 {
      font-family: var(--serif);
      font-size: clamp(44px, 7vw, 84px);
      line-height: 1.05;
      font-weight: 600;
      margin-bottom: 30px;
      letter-spacing: -1px;
    }

    .hero h1 span {
      color: var(--gold);
      font-style: italic;
    }

    .hero p {
      max-width: 680px;
      font-size: 19px;
      color: #e4e9f0;
      margin-bottom: 40px;
      line-height: 1.7;
      font-weight: 300;
    }

    .buttons {
      display: flex;
      gap: 18px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-block;
      padding: 16px 32px;
      border-radius: 4px;
      text-decoration: none;
      font-weight: 600;
      font-size: 14px;
      letter-spacing: 1px;
      text-transform: uppercase;
      transition: 0.3s;
      cursor: pointer;
      border: none;
    }

    .btn-primary {
      background: var(--gold);
      color: var(--navy);
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      background: var(--gold-light);
      box-shadow: 0 10px 25px rgba(201, 162, 39, 0.35);
    }

    .btn-outline {
      border: 1.5px solid rgba(255,255,255,0.5);
      color: white;
      background: transparent;
    }

    .btn-outline:hover {
      background: white;
      color: var(--navy);
      border-color: white;
    }

    /* GENERAL */
    section {
      padding: 110px 7%;
    }

    .section-header {
      max-width: 780px;
      margin: 0 auto 70px;
      text-align: center;
    }

    .section-header .small-title {
      color: var(--gold);
      text-transform: uppercase;
      font-size: 12px;
      font-weight: 700;
      letter-spacing: 4px;
      margin-bottom: 18px;
      display: inline-block;
    }

    .section-header h2 {
      font-family: var(--serif);
      font-size: clamp(32px, 4.5vw, 52px);
      line-height: 1.15;
      color: var(--navy);
      margin-bottom: 20px;
      font-weight: 600;
      letter-spacing: -0.5px;
    }

    .section-header p {
      color: var(--muted);
      font-size: 17px;
      line-height: 1.7;
    }

    /* ABOUT */
    .about {
      background: white;
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1.1fr;
      gap: 70px;
      align-items: center;
      max-width: 1200px;
      margin: auto;
    }

    .about-image {
      position: relative;
      border-radius: 6px;
      overflow: hidden;
      aspect-ratio: 4/5;
      box-shadow: 0 30px 60px rgba(11, 31, 58, 0.15);
    }

    .about-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .about-image::after {
      content: '';
      position: absolute;
      top: 25px;
      left: 25px;
      right: -25px;
      bottom: -25px;
      border: 2px solid var(--gold);
      border-radius: 6px;
      z-index: -1;
    }

    .about-text h3 {
      font-family: var(--serif);
      font-size: 36px;
      color: var(--navy);
      margin-bottom: 22px;
      font-weight: 600;
      line-height: 1.2;
    }

    .about-text p {
      color: var(--muted);
      margin-bottom: 18px;
      font-size: 16px;
      line-height: 1.8;
    }

    .mission-box {
      background: var(--light);
      border-left: 4px solid var(--gold);
      padding: 28px 30px;
      border-radius: 4px;
      margin-top: 30px;
    }

    .mission-box h4 {
      color: var(--navy);
      margin-bottom: 12px;
      font-size: 13px;
      text-transform: uppercase;
      letter-spacing: 3px;
      font-weight: 700;
    }

    .mission-box p {
      color: var(--navy);
      font-size: 16px;
      margin: 0;
      line-height: 1.7;
      font-weight: 400;
    }

    /* SERVICES */
    .services {
      background: var(--light);
    }

    .cards {
      max-width: 1200px;
      margin: auto;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 28px;
    }

    .card {
      background: white;
      padding: 40px 32px;
      border-radius: 6px;
      box-shadow: 0 8px 30px rgba(0,0,0,0.05);
      transition: 0.4s;
      border-top: 3px solid transparent;
      position: relative;
      overflow: hidden;
    }

    .card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 3px;
      background: var(--gold);
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.4s;
    }

    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 20px 45px rgba(11, 31, 58, 0.12);
    }

    .card:hover::before {
      transform: scaleX(1);
    }

    .card-icon {
      font-size: 38px;
      margin-bottom: 22px;
      display: inline-block;
      width: 70px;
      height: 70px;
      background: rgba(201, 162, 39, 0.1);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--gold);
    }

    .card h3 {
      color: var(--navy);
      margin-bottom: 14px;
      font-size: 21px;
      font-weight: 700;
    }

    .card p {
      color: var(--muted);
      font-size: 15px;
      line-height: 1.7;
    }

    /* PROGRAMS */
    .programs {
      background: var(--navy);
      color: white;
      position: relative;
      overflow: hidden;
    }

    .programs::before {
      content: '';
      position: absolute;
      inset: 0;
      background:
        linear-gradient(rgba(11, 31, 58, 0.92), rgba(11, 31, 58, 0.95)),
        url('https://images.unsplash.com/photo-1521737604893-daa9c5ee859c?w=1920&q=80') center/cover;
      z-index: 0;
    }

    .programs > * {
      position: relative;
      z-index: 1;
    }

    .programs .section-header h2 {
      color: white;
    }

    .programs .section-header p {
      color: #bdc7d5;
    }

    .program-list {
      max-width: 1100px;
      margin: auto;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
    }

    .program {
      padding: 35px 32px;
      border: 1px solid rgba(255,255,255,0.15);
      border-radius: 6px;
      background: rgba(255,255,255,0.04);
      backdrop-filter: blur(10px);
      transition: 0.3s;
    }

    .program:hover {
      background: rgba(201, 162, 39, 0.08);
      border-color: var(--gold);
      transform: translateY(-4px);
    }

    .program h3 {
      color: var(--gold);
      margin-bottom: 10px;
      font-family: var(--serif);
      font-size: 26px;
      font-weight: 600;
    }

    .program p {
      color: #d0d7e2;
      line-height: 1.7;
      font-size: 15px;
    }

    /* VALUES */
    .values {
      background: white;
    }

    .values-grid {
      max-width: 1150px;
      margin: auto;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 30px;
      text-align: center;
    }

    .value {
      padding: 35px 20px;
      border-radius: 6px;
      transition: 0.3s;
    }

    .value:hover {
      background: var(--light);
    }

    .value-icon {
      width: 60px;
      height: 60px;
      margin: 0 auto 20px;
      background: var(--navy);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 26px;
    }

    .value strong {
      display: block;
      color: var(--navy);
      font-size: 18px;
      margin-bottom: 10px;
      font-weight: 700;
      letter-spacing: 0.5px;
    }

    .value p {
      color: var(--muted);
      font-size: 14px;
      line-height: 1.7;
    }

    /* SHOWCASE / GALLERY */
    .showcase {
      padding: 110px 7%;
      background: var(--light);
    }

    .showcase-grid {
      max-width: 1200px;
      margin: auto;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .showcase-item {
      position: relative;
      aspect-ratio: 1;
      overflow: hidden;
      border-radius: 6px;
      cursor: pointer;
    }

    .showcase-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.6s;
    }

    .showcase-item::after {
      content: '';
      position: absolute;
      inset: 0;
      background: linear-gradient(to top, rgba(11, 31, 58, 0.85), transparent 60%);
      opacity: 0;
      transition: 0.4s;
    }

    .showcase-item .caption {
      position: absolute;
      bottom: 20px;
      left: 20px;
      color: white;
      z-index: 2;
      transform: translateY(20px);
      opacity: 0;
      transition: 0.4s;
    }

    .showcase-item .caption h4 {
      font-family: var(--serif);
      font-size: 22px;
      margin-bottom: 4px;
    }

    .showcase-item .caption p {
      font-size: 13px;
      color: var(--gold);
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .showcase-item:hover img {
      transform: scale(1.08);
    }

    .showcase-item:hover::after {
      opacity: 1;
    }

    .showcase-item:hover .caption {
      transform: translateY(0);
      opacity: 1;
    }

    /* CTA */
    .cta {
      background: linear-gradient(135deg, #153d6f 0%, #0b1f3a 100%);
      text-align: center;
      color: white;
      position: relative;
      overflow: hidden;
      padding: 120px 7%;
    }

    .cta::before {
      content: '';
      position: absolute;
      top: -50%;
      right: -10%;
      width: 500px;
      height: 500px;
      background: radial-gradient(circle, rgba(201, 162, 39, 0.15), transparent 70%);
      border-radius: 50%;
    }

    .cta > * {
      position: relative;
      z-index: 1;
    }

    .cta h2 {
      font-family: var(--serif);
      font-size: clamp(32px, 5vw, 52px);
      margin-bottom: 20px;
      font-weight: 600;
    }

    .cta p {
      max-width: 650px;
      margin: 0 auto 35px;
      color: #d9e0e9;
      font-size: 18px;
      line-height: 1.7;
    }

    /* CONTACT */
    .contact {
      background: var(--light);
    }

    .contact-grid {
      max-width: 1100px;
      margin: auto;
      display: grid;
      grid-template-columns: 1fr 1.2fr;
      gap: 60px;
    }

    .contact-info h3 {
      font-family: var(--serif);
      color: var(--navy);
      font-size: 34px;
      margin-bottom: 18px;
      font-weight: 600;
    }

    .contact-info > p {
      color: var(--muted);
      margin-bottom: 30px;
      line-height: 1.8;
    }

    .contact-item {
      margin-bottom: 22px;
      padding-bottom: 22px;
      border-bottom: 1px solid rgba(11, 31, 58, 0.08);
    }

    .contact-item:last-child {
      border-bottom: none;
    }

    .contact-item .label {
      color: var(--gold);
      font-size: 11px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 3px;
      margin-bottom: 6px;
      display: block;
    }

    .contact-item .value {
      color: var(--navy);
      font-size: 17px;
      font-weight: 500;
      text-decoration: none;
    }

    .contact-item a:hover {
      color: var(--gold);
    }

    form {
      background: white;
      padding: 40px;
      border-radius: 6px;
      box-shadow: 0 10px 40px rgba(0,0,0,0.06);
    }

    .form-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 15px;
    }

    input,
    textarea {
      width: 100%;
      padding: 15px 18px;
      margin-bottom: 16px;
      border: 1.5px solid #e1e5ed;
      border-radius: 4px;
      font-family: inherit;
      font-size: 15px;
      transition: 0.3s;
      background: #fafbfc;
    }

    input:focus,
    textarea:focus {
      outline: none;
      border-color: var(--gold);
      background: white;
      box-shadow: 0 0 0 3px rgba(201, 162, 39, 0.1);
    }

    textarea {
      height: 140px;
      resize: vertical;
    }

    form button {
      width: 100%;
      font-size: 14px;
      letter-spacing: 1.5px;
    }

    /* FOOTER */
    footer {
      background: #061426;
      color: #aeb9c8;
      padding: 70px 7% 30px;
    }

    .footer-grid {
      max-width: 1200px;
      margin: 0 auto 50px;
      display: grid;
      grid-template-columns: 2fr 1fr 1fr 1fr;
      gap: 50px;
    }

    .footer-brand .logo {
      margin-bottom: 20px;
      font-size: 18px;
    }

    .footer-brand p {
      font-size: 14px;
      line-height: 1.7;
      max-width: 320px;
    }

    .footer-col h5 {
      color: white;
      font-size: 13px;
      text-transform: uppercase;
      letter-spacing: 2px;
      margin-bottom: 20px;
      font-weight: 700;
    }

    .footer-col ul {
      list-style: none;
    }

    .footer-col li {
      margin-bottom: 12px;
    }

    .footer-col a {
      color: #aeb9c8;
      text-decoration: none;
      font-size: 14px;
      transition: 0.3s;
    }

    .footer-col a:hover {
      color: var(--gold);
    }

    .social-links {
      display: flex;
      gap: 12px;
      margin-top: 20px;
    }

    .social-links a {
      width: 38px;
      height: 38px;
      border-radius: 50%;
      background: rgba(255,255,255,0.05);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #aeb9c8;
      text-decoration: none;
      transition: 0.3s;
      font-size: 15px;
    }

    .social-links a:hover {
      background: var(--gold);
      color: var(--navy);
      transform: translateY(-3px);
    }

    .footer-bottom {
      max-width: 1200px;
      margin: auto;
      padding-top: 30px;
      border-top: 1px solid rgba(255,255,255,0.08);
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 15px;
    }

    .footer-bottom p {
      font-size: 13px;
    }

    .footer-bottom span {
      color: var(--gold);
    }

    /* MOBILE */
    @media (max-width: 900px) {
      .nav-links {
        display: none;
        position: absolute;
        top: 75px;
        left: 0;
        width: 100%;
        background: var(--navy);
        flex-direction: column;
        padding: 25px 7%;
        gap: 18px;
        border-top: 1px solid rgba(201, 162, 39, 0.2);
      }

      .nav-links.active {
        display: flex;
      }

      .menu-btn {
        display: block;
      }

      .about-grid,
      .contact-grid,
      .footer-grid {
        grid-template-columns: 1fr;
        gap: 40px;
      }

      .cards {
        grid-template-columns: 1fr;
      }

      .program-list {
        grid-template-columns: 1fr;
      }

      .showcase-grid {
        grid-template-columns: 1fr 1fr;
      }

      .values-grid {
        grid-template-columns: 1fr 1fr;
      }

      .footer-bottom {
        flex-direction: column;
        text-align: center;
      }
    }

    @media (max-width: 500px) {
      section {
        padding: 75px 5%;
      }

      .hero {
        padding: 130px 5% 70px;
      }

      .hero h1 {
        font-size: 44px;
      }

      .hero p {
        font-size: 17px;
      }

      .showcase-grid,
      .values-grid,
      .form-row {
        grid-template-columns: 1fr;
      }

      form {
        padding: 28px 22px;
      }
    }

    /* Reveal animations */
    .reveal {
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.8s ease, transform 0.8s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->
  <nav>
    <a href="#home" class="logo">
      <div class="logo-mark">K</div>
      <div class="logo-text">
        <span class="primary">KEBRE</span>
        <span class="secondary">INSTITUTE</span>
      </div>
    </a>

    <button class="menu-btn" onclick="toggleMenu()" aria-label="Toggle menu">☰</button>

    <ul class="nav-links" id="navLinks">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#programs">Programs</a></li>
      <li><a href="#showcase">Gallery</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>


  <!-- HERO -->
  <section class="hero" id="home">
    <div class="hero-content">
      <div class="hero-label">Mindset · Leadership · Enterprise</div>

      <h1>
        Transform Your <span>Mind.</span><br>
        Transform Your <span>Enterprise.</span>
      </h1>

      <p>
        Kebre Institute for Mind & Enterprise is a premier center for leadership and business transformation, dedicated to elevating human potential through advanced mindset development, strategic enterprise consulting, and executive training.
      </p>

      <div class="buttons">
        <a href="#services" class="btn btn-primary">Explore Our Services</a>
        <a href="#contact" class="btn btn-outline">Get in Touch</a>
      </div>
    </div>
  </section>


  <!-- ABOUT -->
  <section class="about reveal" id="about">
    <div class="section-header">
      <div class="small-title">About Kebre</div>
      <h2>Where Human Potential Meets Enterprise Excellence</h2>
      <p>We develop the thinking, leadership capabilities and strategic systems required to create sustainable transformation across Africa and beyond.</p>
    </div>

    <div class="about-grid">
      <div class="about-image">
        <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=900&q=80" alt="Executive leadership team in strategic discussion" loading="lazy">
      </div>

      <div class="about-text">
        <h3>Building Leaders for a Changing World</h3>
        <p>At Kebre Institute for Mind & Enterprise, we believe that extraordinary organizations begin with extraordinary thinking. Founded on the conviction that sustainable growth starts from within, we serve executives, entrepreneurs, and institutions committed to meaningful impact.</p>
        <p>Our approach combines mindset science, leadership development, strategic business thinking and practical enterprise solutions to help individuals and organizations unlock their next level of performance.</p>

        <div class="mission-box">
          <h4>Our Mission</h4>
          <p>To elevate human potential and transform enterprises by developing visionary leaders, powerful mindsets and sustainable strategies.</p>
        </div>
      </div>
    </div>
  </section>


  <!-- SERVICES -->
  <section class="services reveal" id="services">
    <div class="section-header">
      <div class="small-title">What We Do</div>
      <h2>Our Core Services</h2>
      <p>Integrated solutions designed to develop people, strengthen organizations and accelerate meaningful growth.</p>
    </div>

    <div class="cards">
      <div class="card">
        <div class="card-icon">🧠</div>
        <h3>Mindset Development</h3>
        <p>Advanced programs designed to develop resilience, strategic thinking, confidence, emotional intelligence and a high-performance mindset.</p>
      </div>

      <div class="card">
        <div class="card-icon">👑</div>
        <h3>Leadership Development</h3>
        <p>Transformational leadership programs that equip emerging and established leaders to inspire people and create lasting organizational impact.</p>
      </div>

      <div class="card">
        <div class="card-icon">📈</div>
        <h3>Enterprise Consulting</h3>
        <p>Strategic consulting solutions helping businesses improve performance, strengthen operations and identify sustainable growth opportunities.</p>
      </div>

      <div class="card">
        <div class="card-icon">🎯</div>
        <h3>Executive Training</h3>
        <p>High-level training experiences created for executives, entrepreneurs and decision-makers navigating complex business environments.</p>
      </div>

      <div class="card">
        <div class="card-icon">🚀</div>
        <h3>Business Transformation</h3>
        <p>Practical transformation frameworks that connect leadership, strategy, culture and execution for measurable, lasting change.</p>
      </div>

      <div class="card">
        <div class="card-icon">💡</div>
        <h3>Strategic Innovation</h3>
        <p>Helping organizations develop innovative thinking and discover new approaches to growth and competitive advantage.</p>
      </div>
    </div>
  </section>


  <!-- PROGRAMS -->
  <section class="programs reveal" id="programs">
    <div class="section-header">
      <div class="small-title">Our Programs</div>
      <h2>Programs Designed for Transformation</h2>
      <p>From personal growth to enterprise strategy, our programs are built around practical, real-world transformation.</p>
    </div>

    <div class="program-list">
      <div class="program">
        <h3>Executive Leadership Academy</h3>
        <p>A signature leadership development experience for executives and senior professionals seeking to deepen their strategic impact.</p>
      </div>

      <div class="program">
        <h3>Mindset Mastery</h3>
        <p>Develop the mental frameworks required for clarity, resilience and sustained high performance under pressure.</p>
      </div>

      <div class="program">
        <h3>Entrepreneurship & Enterprise</h3>
        <p>Build entrepreneurial thinking and develop strategies for sustainable business growth in dynamic African markets.</p>
      </div>

      <div class="program">
        <h3>Corporate Transformation</h3>
        <p>Customized organizational development and strategic transformation programs tailored to your institution's unique needs.</p>
      </div>
    </div>
  </section>


  <!-- VALUES -->
  <section class="values reveal">
    <div class="section-header">
      <div class="small-title">Our Philosophy</div>
      <h2>Principles That Guide Us</h2>
    </div>

    <div class="values-grid">
      <div class="value">
        <div class="value-icon">✦</div>
        <strong>Human Potential</strong>
        <p>Every person has the capacity to grow, lead and create meaningful impact.</p>
      </div>

      <div class="value">
        <div class="value-icon">◈</div>
        <strong>Strategic Thinking</strong>
        <p>Great results begin with clarity, intentionality, and purposeful decisions.</p>
      </div>

      <div class="value">
        <div class="value-icon">✧</div>
        <strong>Excellence</strong>
        <p>We pursue meaningful standards in every engagement and every interaction.</p>
      </div>

      <div class="value">
        <div class="value-icon">◆</div>
        <strong>Transformation</strong>
        <p>We focus on sustainable, lasting change rather than temporary results.</p>
      </div>
    </div>
  </section>


  <!-- SHOWCASE -->
  <section class="showcase reveal" id="showcase">
    <div class="section-header">
      <div class="small-title">In Action</div>
      <h2>Moments That Shape Leaders</h2>
      <p>Glimpses from our training sessions, retreats, and executive engagements across Africa.</p>
    </div>

    <div class="showcase-grid">
      <div class="showcase-item">
        <img src="https://images.unsplash.com/photo-1515169067868-5387ec357754?w=800&q=80" alt="Executive workshop session" loading="lazy">
        <div class="caption">
          <h4>Executive Retreat</h4>
          <p>Leadership</p>
        </div>
      </div>

      <div class="showcase-item">
        <img src="https://images.unsplash.com/photo-1519052537078-e6302a4968d4?w=800&q=80" alt="Strategic planning session" loading="lazy">
        <div class="caption">
          <h4>Strategic Dialogue</h4>
          <p>Consulting</p>
        </div>
      </div>

      <div class="showcase-item">
        <img src="https://images.unsplash.com/photo-1540575467063-178a50c2df87?w=800&q=80" alt="Leadership conference" loading="lazy">
        <div class="caption">
          <h4>Leadership Summit</h4>
          <p>Training</p>
        </div>
      </div>

      <div class="showcase-item">
        <img src="https://images.unsplash.com/photo-1600880292203-757bb62b4baf?w=800&q=80" alt="Team collaboration" loading="lazy">
        <div class="caption">
          <h4>Team Transformation</h4>
          <p>Enterprise</p>
        </div>
      </div>

      <div class="showcase-item">
        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=800&q=80" alt="One-on-one coaching" loading="lazy">
        <div class="caption">
          <h4>Executive Coaching</h4>
          <p>Mindset</p>
        </div>
      </div>

      <div class="showcase-item">
        <img src="https://images.unsplash.com/photo-1573164713714-d95e436ab8d6?w=800&q=80" alt="Innovation workshop" loading="lazy">
        <div class="caption">
          <h4>Innovation Lab</h4>
          <p>Strategy</p>
        </div>
      </div>
    </div>
  </section>


  <!-- CTA -->
  <section class="cta reveal">
    <h2>Ready to Elevate Your Potential?</h2>
    <p>Whether you are an executive, entrepreneur, professional or organization, Kebre Institute can help you move from potential to performance.</p>
    <a href="#contact" class="btn btn-primary">Start the Conversation</a>
  </section>


  <!-- CONTACT -->
  <section class="contact reveal" id="contact">
    <div class="section-header">
      <div class="small-title">Connect With Us</div>
      <h2>Let's Build the Future Together</h2>
      <p>Contact Kebre Institute for leadership programs, consulting, executive training and partnership opportunities.</p>
    </div>

    <div class="contact-grid">
      <div class="contact-info">
        <h3>Kebre Institute for Mind &amp; Enterprise</h3>
        <p>A center dedicated to developing people, leaders and enterprises for meaningful and sustainable transformation.</p>

        <div class="contact-item">
          <span class="label">Email</span>
          <a href="mailto:mekonnenchirotaw11@gmail.com" class="value">mekonnenchirotaw11@gmail.com</a>
        </div>

        <div class="contact-item">
          <span class="label">Phone</span>
          <a href="tel:+251961689615" class="value">+251 961 689 615</a>
        </div>

        <div class="contact-item">
          <span class="label">Location</span>
          <span class="value">Addis Ababa, Ethiopia</span>
        </div>

        <div class="contact-item">
          <span class="label">Hours</span>
          <span class="value">Monday – Friday · 8:30 AM – 6:00 PM</span>
        </div>
      </div>

      <form onsubmit="sendMessage(event)">
        <div class="form-row">
          <input type="text" id="name" placeholder="Your Name" required>
          <input type="email" id="email" placeholder="Your Email" required>
        </div>
        <input type="text" id="subject" placeholder="Subject" required>
        <textarea id="message" placeholder="How can we help you?" required></textarea>
        <button class="btn btn-primary" type="submit">Send Message</button>
      </form>
    </div>
  </section>


  <!-- FOOTER -->
  <footer>
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="logo">
          <div class="logo-mark">K</div>
          <div class="logo-text">
            <span class="primary">KEBRE</span>
            <span class="secondary">INSTITUTE</span>
          </div>
        </div>
        <p>Elevating human potential and transforming enterprises through visionary leadership, powerful mindsets, and sustainable strategies.</p>
        <div class="social-links">
          <a href="#" aria-label="LinkedIn">in</a>
          <a href="#" aria-label="Twitter">𝕏</a>
          <a href="#" aria-label="Facebook">f</a>
          <a href="#" aria-label="Instagram">◎</a>
        </div>
      </div>

      <div class="footer-col">
        <h5>Institute</h5>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#programs">Programs</a></li>
          <li><a href="#showcase">Gallery</a></li>
        </ul>
      </div>

      <div class="footer-col">
        <h5>Services</h5>
        <ul>
          <li><a href="#services">Mindset Development</a></li>
          <li><a href="#services">Leadership</a></li>
          <li><a href="#services">Consulting</a></li>
          <li><a href="#services">Executive Training</a></li>
        </ul>
      </div>

      <div class="footer-col">
        <h5>Contact</h5>
        <ul>
          <li><a href="mailto:mekonnenchirotaw11@gmail.com">Email Us</a></li>
          <li><a href="tel:+251961689615">+251 961 689 615</a></li>
          <li>Addis Ababa, Ethiopia</li>
        </ul>
      </div>
    </div>

    <div class="footer-bottom">
      <p>© 2026 Kebre Institute for Mind & Enterprise. <span>All Rights Reserved.</span></p>
      <p>Leadership · Mindset · Enterprise Transformation</p>
    </div>
  </footer>


  <script>
    function toggleMenu() {
      document.getElementById("navLinks").classList.toggle("active");
    }

    document.querySelectorAll(".nav-links a").forEach(function(link) {
      link.addEventListener("click", function() {
        document.getElementById("navLinks").classList.remove("active");
      });
    });

    function sendMessage(event) {
      event.preventDefault();
      const name = document.getElementById("name").value;
      const email = document.getElementById("email").value;
      const subject = document.getElementById("subject").value;
      const message = document.getElementById("message").value;

      // Build mailto link with form data
      const body = "Name: " + name + "%0D%0AEmail: " + email + "%0D%0A%0D%0A" + encodeURIComponent(message);
      window.location.href = "mailto:mekonnenchirotaw11@gmail.com?subject=" + encodeURIComponent(subject) + "&body=" + body;

      alert("Thank you, " + name + "! Opening your email client to send your message.");
    }

    // Reveal on scroll
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, { threshold: 0.12 });

    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
  </script>

</body>
</html>
