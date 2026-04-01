<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>heva Philippines | AI-Native Healthcare Platform</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 (free icons) for extra visual polish -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Inter', sans-serif;
      background-color: #ffffff;
      color: #1A2C3E;
      line-height: 1.5;
      scroll-behavior: smooth;
    }
    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 32px;
    }
    .btn {
      display: inline-block;
      font-weight: 600;
      border-radius: 40px;
      padding: 12px 28px;
      text-decoration: none;
      transition: all 0.2s ease;
      font-size: 1rem;
      cursor: pointer;
      border: none;
    }
    .btn-primary {
      background-color: #0A66C2;
      color: white;
      box-shadow: 0 2px 6px rgba(10,102,194,0.2);
    }
    .btn-primary:hover {
      background-color: #004182;
      transform: translateY(-2px);
    }
    .btn-outline {
      background-color: transparent;
      border: 1.5px solid #0A66C2;
      color: #0A66C2;
    }
    .btn-outline:hover {
      background-color: #EFF5FF;
      border-color: #004182;
      color: #004182;
    }
    .navbar {
      padding: 20px 0;
      border-bottom: 1px solid #EFF2F5;
      background: white;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    .nav-container {
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
    }
    .logo a {
      font-size: 1.6rem;
      font-weight: 700;
      text-decoration: none;
      color: #0A66C2;
      letter-spacing: -0.3px;
    }
    .logo span {
      font-weight: 400;
      color: #5A6E7F;
      font-size: 1rem;
    }
    .nav-links {
      display: flex;
      gap: 32px;
      list-style: none;
    }
    .nav-links a {
      text-decoration: none;
      font-weight: 500;
      color: #2C3E50;
      transition: color 0.2s;
    }
    .nav-links a:hover, .nav-links a.active {
      color: #0A66C2;
    }
    .mobile-toggle {
      display: none;
      font-size: 1.8rem;
      background: none;
      border: none;
      cursor: pointer;
    }
    @media (max-width: 768px) {
      .nav-links {
        display: none;
        width: 100%;
        flex-direction: column;
        gap: 16px;
        padding: 20px 0 10px;
      }
      .nav-links.show {
        display: flex;
      }
      .mobile-toggle {
        display: block;
      }
      .container {
        padding: 0 24px;
      }
    }
    .page {
      display: none;
      animation: fadeIn 0.25s ease;
    }
    .active-page {
      display: block;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(8px);}
      to { opacity: 1; transform: translateY(0);}
    }
    .hero {
      padding: 70px 0 50px;
      text-align: center;
    }
    .hero h1 {
      font-size: 3.2rem;
      font-weight: 700;
      line-height: 1.2;
      max-width: 900px;
      margin: 0 auto 24px;
    }
    .hero p {
      font-size: 1.2rem;
      color: #4A5B6E;
      max-width: 650px;
      margin: 0 auto 32px;
    }
    .hero-buttons {
      display: flex;
      gap: 20px;
      justify-content: center;
      flex-wrap: wrap;
    }
    .features-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 40px;
      justify-content: center;
      margin: 70px 0;
    }
    .feature-card {
      flex: 1;
      min-width: 240px;
      background: #F9FBFD;
      padding: 32px 24px;
      border-radius: 28px;
      text-align: center;
      transition: transform 0.2s;
    }
    .feature-card:hover { transform: translateY(-6px);}
    .feature-icon {
      font-size: 2.8rem;
      margin-bottom: 20px;
      color: #0A66C2;
    }
    .feature-card h3 {
      font-size: 1.5rem;
      margin-bottom: 12px;
    }
    .diff-section {
      background: #F0F6FE;
      border-radius: 48px;
      padding: 56px 40px;
      margin: 60px 0;
    }
    .diff-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 32px;
      justify-content: space-between;
      margin-top: 40px;
    }
    .diff-item {
      flex: 1;
      background: white;
      border-radius: 32px;
      padding: 28px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.02);
    }
    .diff-title {
      font-weight: 700;
      font-size: 1.4rem;
      margin-bottom: 16px;
    }
    .diff-compare {
      display: flex;
      justify-content: space-between;
      gap: 16px;
      margin-top: 16px;
    }
    .diff-before, .diff-after {
      background: #F8FAFE;
      border-radius: 24px;
      padding: 16px;
      flex:1;
    }
    .stats-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 24px;
      margin: 60px 0;
      text-align: center;
    }
    .stat-card {
      flex: 1;
      background: #FFFFFF;
      padding: 32px 20px;
      border-radius: 32px;
      box-shadow: 0 12px 24px -12px rgba(0,0,0,0.05);
    }
    .stat-number {
      font-size: 2.8rem;
      font-weight: 800;
      color: #0A66C2;
    }
    .testimonial-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 32px;
      margin: 50px 0;
    }
    .testimonial-card {
      flex: 1;
      background: #F9FBFD;
      border-radius: 32px;
      padding: 28px;
    }
    .partner-logos {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 48px;
      margin: 48px 0;
    }
    .partner-logos img {
      height: 48px;
      opacity: 0.7;
      transition: opacity 0.2s;
    }
    .partner-logos img:hover { opacity: 1; }
    .founder-section {
      text-align: center;
      margin: 70px 0;
    }
    .founder-card {
      max-width: 480px;
      margin: 0 auto;
      background: #FFFFFF;
      border-radius: 36px;
      box-shadow: 0 20px 35px -12px rgba(0,0,0,0.08);
      padding: 32px 28px;
      border: 1px solid #E9EEF3;
    }
    .founder-img {
      width: 140px;
      height: 140px;
      border-radius: 50%;
      margin: 0 auto 20px;
      overflow: hidden;
      background: #D9E6F7;
    }
    .founder-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .specialties-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 32px;
      margin: 50px 0;
    }
    .specialty-card {
      background: #F9FBFD;
      border-radius: 28px;
      padding: 28px;
      transition: all 0.2s;
    }
    .specialty-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 24px;
      margin-bottom: 20px;
    }
    .saving {
      color: #0A66C2;
      font-weight: 700;
      margin: 12px 0;
    }
    .cta-section {
      background: linear-gradient(135deg, #0A2E4D 0%, #0A66C2 100%);
      border-radius: 48px;
      padding: 60px 40px;
      text-align: center;
      color: white;
      margin: 60px 0;
    }
    footer {
      background: #F8FAFE;
      padding: 48px 0 32px;
      margin-top: 60px;
      border-top: 1px solid #E2E8F0;
    }
    .footer-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 40px;
    }
    .footer-col {
      flex: 1;
      min-width: 180px;
    }
    .footer-col h4 {
      margin-bottom: 20px;
      font-size: 1.1rem;
    }
    .footer-col p, .footer-col a {
      color: #4A5B6E;
      text-decoration: none;
      margin-bottom: 12px;
      display: block;
    }
    .copyright {
      text-align: center;
      margin-top: 48px;
      padding-top: 24px;
      border-top: 1px solid #E2E8F0;
      color: #5F6F80;
    }
    .contact-info {
      display: flex;
      flex-wrap: wrap;
      gap: 48px;
      margin: 50px 0;
    }
    .contact-details {
      flex: 1;
    }
    .contact-form {
      flex: 1;
      background: #F9FBFD;
      padding: 32px;
      border-radius: 32px;
    }
    .contact-form input, .contact-form textarea {
      width: 100%;
      padding: 14px;
      margin: 12px 0;
      border: 1px solid #CFDFE9;
      border-radius: 28px;
      font-family: inherit;
    }
    .office-image {
      border-radius: 28px;
      overflow: hidden;
      margin-top: 28px;
    }
    .office-image img {
      width: 100%;
      height: auto;
      display: block;
    }
    h2 {
      font-size: 2rem;
      margin-bottom: 24px;
    }
    .text-center {
      text-align: center;
    }
    .section-subhead {
      color: #5A6E7F;
      max-width: 700px;
      margin: 0 auto 40px;
    }
    img {
      max-width: 100%;
    }
  </style>
</head>
<body>
<nav class="navbar">
  <div class="container nav-container">
    <div class="logo">
      <a href="#">heva <span>Philippines</span></a>
    </div>
    <button class="mobile-toggle" id="mobileMenuBtn" aria-label="Menu">☰</button>
    <ul class="nav-links" id="navLinks">
      <li><a href="#" data-page="home" class="active">Home</a></li>
      <li><a href="#" data-page="about">About</a></li>
      <li><a href="#" data-page="specialties">Specialties</a></li>
      <li><a href="#" data-page="contact">Contact</a></li>
    </ul>
  </div>
</nav>

<main>
  <!-- HOME PAGE -->
  <div id="home-page" class="page active-page">
    <div class="container">
      <div class="hero">
        <h1>Care Without Borders <br>AI‑Native Healthcare Platform</h1>
        <p>Connect with global patients and discover world‑class medical care in the Philippines. Streamlined, transparent, and powered by AI.</p>
        <div class="hero-buttons">
          <a href="#" class="btn btn-primary" data-page="contact">For Medical Providers</a>
          <a href="#" class="btn btn-outline" data-page="specialties">Discover Quality Care</a>
        </div>
      </div>

      <!-- Features with icons -->
      <div class="features-grid">
        <div class="feature-card">
          <div class="feature-icon"><i class="fas fa-robot"></i></div>
          <h3>Seamless Discovery</h3>
          <p>AI‑powered matching connects you with verified healthcare providers across the Philippines and beyond.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon"><i class="fas fa-heartbeat"></i></div>
          <h3>Personalized Care Journey</h3>
          <p>From inquiry to recovery, enjoy comprehensive support tailored to your unique health needs.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon"><i class="fas fa-shield-alt"></i></div>
          <h3>Trust & Transparency</h3>
          <p>Verified credentials, clear pricing, and authentic patient reviews for confident decisions.</p>
        </div>
      </div>

      <!-- Stats Section (new) -->
      <div class="stats-grid">
        <div class="stat-card"><div class="stat-number">50+</div><p>Partner Hospitals</p></div>
        <div class="stat-card"><div class="stat-number">30+</div><p>Specialties Covered</p></div>
        <div class="stat-card"><div class="stat-number">98%</div><p>Patient Satisfaction</p></div>
        <div class="stat-card"><div class="stat-number">24/7</div><p>AI Support</p></div>
      </div>

      <!-- The heva Difference -->
      <div class="diff-section">
        <h2 class="text-center">The heva Difference</h2>
        <div class="diff-grid">
          <div class="diff-item"><div class="diff-title">Transparent Discovery</div><div class="diff-compare"><div class="diff-before"><span>Before</span>Confusing options</div><div class="diff-after"><span>After</span>Crystal clear choices</div></div></div>
          <div class="diff-item"><div class="diff-title">Automated Processes</div><div class="diff-compare"><div class="diff-before"><span>Before</span>Manual booking</div><div class="diff-after"><span>After</span>Seamless automation</div></div></div>
          <div class="diff-item"><div class="diff-title">Secure Payments</div><div class="diff-compare"><div class="diff-before"><span>Before</span>Payment risks</div><div class="diff-after"><span>After</span>Protected transactions</div></div></div>
        </div>
      </div>

      <!-- Why Philippines? new visual block -->
      <div style="margin: 70px 0;">
        <div style="display: flex; flex-wrap: wrap; gap: 48px; align-items: center;">
          <div style="flex: 1; border-radius: 32px; overflow: hidden;">
            <img src="https://picsum.photos/id/104/600/400" alt="Philippines healthcare" style="width:100%; height: auto; border-radius: 32px;">
          </div>
          <div style="flex:1">
            <h2>Why the Philippines?</h2>
            <p>World-class JCI-accredited hospitals, English-speaking staff, and internationally trained specialists. Combined with warm hospitality and up to 80% cost savings compared to the US or Europe.</p>
            <ul style="margin-top: 24px; list-style: none;">
              <li><i class="fas fa-check-circle" style="color:#0A66C2;"></i> 25+ JCI-accredited hospitals</li>
              <li><i class="fas fa-check-circle" style="color:#0A66C2;"></i> Top medical tourism destination in Asia</li>
              <li><i class="fas fa-check-circle" style="color:#0A66C2;"></i> Seamless travel & accommodation support</li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Founder: Emma Burke (updated portrait) -->
      <div class="founder-section">
        <h2>Leading heva Philippines</h2>
        <div class="founder-card">
          <div class="founder-img"><img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Emma Burke"></div>
          <div class="founder-name">Emma Burke</div>
          <div class="founder-title">Country Director, heva Philippines</div>
          <p>Emma brings over 15 years of experience in cross‑border healthcare and digital health innovation across Southeast Asia. Formerly at leading Manila medical institutions and global health tech, she is dedicated to making quality care accessible to every Filipino and international patient visiting the Philippines.</p>
        </div>
      </div>

      <!-- Partner logos (placeholder images) -->
      <div class="text-center"><h3>Trusted by leading institutions</h3></div>
      <div class="partner-logos">
        <img src="https://placehold.co/120x40/eef2f5/0A66C2?text=St.Luke's" alt="partner">
        <img src="https://placehold.co/120x40/eef2f5/0A66C2?text=MedicalCity" alt="partner">
        <img src="https://placehold.co/120x40/eef2f5/0A66C2?text=AsianHospital" alt="partner">
        <img src="https://placehold.co/120x40/eef2f5/0A66C2?text=GlobalCare" alt="partner">
      </div>

      <!-- Testimonials new -->
      <div><h2 class="text-center">What our patients say</h2>
        <div class="testimonial-grid">
          <div class="testimonial-card"><i class="fas fa-quote-left" style="color:#0A66C2; margin-bottom: 16px; display: block;"></i><p>"heva made my dental trip to Manila seamless. The AI matching found a top clinic and I saved over 60%."</p><p style="margin-top: 16px; font-weight:600;">— Maria L., Australia</p></div>
          <div class="testimonial-card"><i class="fas fa-quote-left" style="color:#0A66C2; margin-bottom: 16px; display: block;"></i><p>"Professional, transparent pricing and genuine care. I had my knee replacement with zero hassle."</p><p style="margin-top: 16px; font-weight:600;">— David R., USA</p></div>
          <div class="testimonial-card"><i class="fas fa-quote-left" style="color:#0A66C2; margin-bottom: 16px; display: block;"></i><p>"Emma and the team provided outstanding support. Highly recommended for medical travel."</p><p style="margin-top: 16px; font-weight:600;">— Fatima A., UAE</p></div>
        </div>
      </div>

      <!-- Popular specialties preview (brief) -->
      <h2 class="text-center">Popular Medical Tourism Specialties</h2>
      <div class="specialties-grid">
        <div class="specialty-card"><img src="https://picsum.photos/id/177/400/250" alt="Dental"><h3>Dental Care</h3><p>Implants, veneers, full mouth reconstruction</p><div class="saving">Save 50-70%</div></div>
        <div class="specialty-card"><img src="https://picsum.photos/id/29/400/250" alt="Cosmetic"><h3>Cosmetic Surgery</h3><p>Facelifts, rhinoplasty, body contouring</p><div class="saving">Save 40-60%</div></div>
        <div class="specialty-card"><img src="https://picsum.photos/id/107/400/250" alt="Orthopedic"><h3>Orthopedic Surgery</h3><p>Joint replacements, sports medicine</p><div class="saving">Save 60-80%</div></div>
      </div>
      <div class="text-center" style="margin: 20px 0 60px;"><a href="#" data-page="specialties" class="btn btn-outline">View all specialties <i class="fas fa-arrow-right"></i></a></div>

      <div class="cta-section">
        <h2>Ready to Transform Cross-Border Healthcare?</h2>
        <p>Whether you're a provider or a patient, heva Philippines is your trusted partner.</p>
        <a href="#" class="btn btn-primary" data-page="contact">Get in Touch</a>
      </div>
    </div>
  </div>

  <!-- ABOUT PAGE (rich with images) -->
  <div id="about-page" class="page">
    <div class="container">
      <div style="padding: 40px 0;">
        <h2 class="text-center">About heva Philippines</h2>
        <div style="display: flex; flex-wrap: wrap; gap: 40px; margin: 40px 0;">
          <div style="flex:1"><img src="https://picsum.photos/id/13/600/400" alt="heva team" style="border-radius: 32px; width:100%"></div>
          <div style="flex:1"><p style="font-size:1.2rem;">heva Philippines is the regional hub of our global AI-native healthcare platform, dedicated to connecting patients and providers with unmatched transparency and care. Based at the heart of Metro Manila, our local team ensures that every patient receives personalized guidance while leveraging heva’s cutting‑edge AI matching.</p></div>
        </div>
        <h3>Our Mission</h3>
        <p>To break down borders in healthcare by making quality medical services accessible, affordable, and seamless—starting in the Philippines, one of the world’s leading medical tourism destinations.</p>
        <div style="margin: 48px 0;"><img src="https://picsum.photos/id/24/1200/300" style="width:100%; border-radius: 32px;" alt="Manila skyline"></div>
        <h3>Meet Emma Burke</h3>
        <div style="display: flex; flex-wrap: wrap; gap: 32px; margin: 32px 0;">
          <div style="flex:1; max-width: 200px;"><img src="https://randomuser.me/api/portraits/women/44.jpg" style="border-radius: 50%; width:100%;" alt="Emma Burke"></div>
          <div style="flex:3"><p>As Country Director, Emma Burke leads heva’s expansion in the Philippines. With a background in healthcare strategy and a passion for innovation, she works closely with local providers to ensure our platform delivers real value to both Filipino and international patients. Emma holds an MBA from Asian Institute of Management and previously directed patient experience programs at top Manila hospitals.</p></div>
        </div>
        <div class="stats-grid" style="margin: 40px 0;">
          <div class="stat-card"><div class="stat-number">10+</div><p>Years of cross-border health experience</p></div>
          <div class="stat-card"><div class="stat-number">500+</div><p>Successful patient journeys</p></div>
        </div>
      </div>
    </div>
  </div>

  <!-- SPECIALTIES PAGE (fully detailed with images) -->
  <div id="specialties-page" class="page">
    <div class="container">
      <div style="padding: 40px 0;">
        <h2 class="text-center">Medical Specialties in the Philippines</h2>
        <p class="text-center section-subhead">The Philippines offers JCI‑accredited hospitals and internationally trained specialists at a fraction of Western costs.</p>
        <div class="specialties-grid">
          <div class="specialty-card"><img src="https://picsum.photos/id/183/400/250" alt="Dental"><h3>Dental Tourism</h3><p>High-quality implants, porcelain veneers, and full smile makeovers with up to 70% savings compared to US prices.</p><div class="saving">From $1,200 for full implant</div></div>
          <div class="specialty-card"><img src="https://picsum.photos/id/106/400/250" alt="Plastic surgery"><h3>Aesthetic & Plastic Surgery</h3><p>Board‑certified surgeons, modern clinics in Manila, Cebu. Breast augmentation, tummy tuck, and facial procedures.</p><div class="saving">Save 40-60%</div></div>
          <div class="specialty-card"><img src="https://picsum.photos/id/26/400/250" alt="Orthopedics"><h3>Orthopedics & Spine</h3><p>Minimally invasive joint replacements, ACL reconstruction, and spinal fusion using advanced robotic assistance.</p><div class="saving">Save 60-80%</div></div>
          <div class="specialty-card"><img src="https://picsum.photos/id/116/400/250" alt="Cardiac"><h3>Cardiovascular Care</h3><p>Top‑notch cardiac centers offering bypass surgery, angioplasty, and preventive programs.</p><div class="saving">Save 60-80%</div></div>
          <div class="specialty-card"><img src="https://picsum.photos/id/124/400/250" alt="Fertility"><h3>Fertility & IVF</h3><p>Leading fertility clinics with high success rates and affordable IVF packages.</p><div class="saving">Save 50%+</div></div>
          <div class="specialty-card"><img src="https://picsum.photos/id/20/400/250" alt="Wellness"><h3>Wellness & Executive Checkups</h3><p>Comprehensive health screenings and integrative wellness packages.</p><div class="saving">Custom plans</div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- CONTACT PAGE with office image -->
  <div id="contact-page" class="page">
    <div class="container">
      <div style="padding: 40px 0;">
        <h2 class="text-center">Contact heva Philippines</h2>
        <div class="contact-info">
          <div class="contact-details">
            <h3>Visit Our Office</h3>
            <p>Seaside Blvd, Mall of Asia Complex #03-15, SM Mall of Asia<br>Pasay City, Metro Manila 1300, Philippines</p>
            <h3 style="margin-top: 32px;">Call / Support</h3>
            <p><i class="fas fa-phone-alt"></i> +63288884532</p>
            <p><i class="fas fa-envelope"></i> <a href="mailto:support@heva.work">support@heva.work</a></p>
            <div class="office-image">
              <img src="https://picsum.photos/id/96/600/300" alt="SM Mall of Asia office">
            </div>
          </div>
          <div class="contact-form">
            <h3>Send a Message</h3>
            <form id="contactForm">
              <input type="text" placeholder="Full Name" required>
              <input type="email" placeholder="Email Address" required>
              <input type="tel" placeholder="Phone (optional)">
              <textarea rows="4" placeholder="How can we help you?"></textarea>
              <button type="submit" class="btn btn-primary" style="width:100%">Send Inquiry</button>
              <p style="font-size:0.8rem; margin-top:12px;">Our team will reply within 24 hours.</p>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</main>

<footer>
  <div class="container">
    <div class="footer-grid">
      <div class="footer-col"><h4>heva Philippines</h4><p>Care Without Borders</p><p>AI-Native Healthcare Platform</p></div>
      <div class="footer-col"><h4>Visit</h4><p>Seaside Blvd, MOA Complex #03-15<br>Pasay City, 1300 PH</p><p>📞 +63288884532</p><p>✉️ support@heva.work</p></div>
      <div class="footer-col"><h4>Quick Links</h4><a href="#" data-page="about">About Emma Burke</a><a href="#" data-page="specialties">Specialties</a><a href="#" data-page="contact">Contact</a></div>
      <div class="footer-col"><h4>Legal</h4><a href="#">Privacy Policy</a><a href="#">Cookie Preferences</a></div>
    </div>
    <div class="copyright"><p>© 2025 heva Philippines. All rights reserved. Part of heva Global network.</p><p style="font-size:0.8rem;">We use cookies to improve service.</p></div>
  </div>
</footer>

<script>
  const pages = {
    home: document.getElementById('home-page'),
    about: document.getElementById('about-page'),
    specialties: document.getElementById('specialties-page'),
    contact: document.getElementById('contact-page')
  };
  function showPage(pageId) {
    Object.keys(pages).forEach(id => pages[id].classList.remove('active-page'));
    pages[pageId].classList.add('active-page');
    document.querySelectorAll('.nav-links a').forEach(link => {
      if(link.getAttribute('data-page') === pageId) link.classList.add('active');
      else link.classList.remove('active');
    });
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
  document.querySelectorAll('[data-page]').forEach(el => {
    el.addEventListener('click', (e) => {
      e.preventDefault();
      const page = el.getAttribute('data-page');
      if(page && pages[page]) showPage(page);
    });
  });
  document.getElementById('mobileMenuBtn').addEventListener('click', () => {
    document.getElementById('navLinks').classList.toggle('show');
  });
  const contactForm = document.getElementById('contactForm');
  if(contactForm) {
    contactForm.addEventListener('submit', (e) => {
      e.preventDefault();
      alert('Thank you for reaching out! Our heva Philippines team will respond shortly.');
      contactForm.reset();
    });
  }
  showPage('home');
</script>
</body>
</html>
