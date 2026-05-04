<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Inspire Award Build – PWM Flight Controller | Atharva Phadnis</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;600;700&family=IBM+Plex+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<style>
  :root {
    --bg: #0c0f14;
    --bg2: #12161e;
    --card: #181d28;
    --card-hover: #1e2533;
    --border: #2a3040;
    --fg: #e8ecf4;
    --muted: #8892a4;
    --accent: #00e59b;
    --accent2: #00c483;
    --accent-glow: rgba(0, 229, 155, 0.15);
    --warn: #ff6b4a;
    --gold: #ffc53d;
    --code-bg: #0f1318;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'IBM Plex Sans', sans-serif;
    background: var(--bg);
    color: var(--fg);
    line-height: 1.8;
    font-size: 16px;
    overflow-x: hidden;
  }

  /* Animated background */
  .bg-grid {
    position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    z-index: 0;
    pointer-events: none;
    background-image:
      radial-gradient(ellipse 600px 400px at 20% 10%, rgba(0,229,155,0.06), transparent),
      radial-gradient(ellipse 500px 500px at 80% 80%, rgba(0,196,131,0.04), transparent),
      linear-gradient(rgba(42,48,64,0.3) 1px, transparent 1px),
      linear-gradient(90deg, rgba(42,48,64,0.3) 1px, transparent 1px);
    background-size: 100% 100%, 100% 100%, 60px 60px, 60px 60px;
  }

  .floating-orb {
    position: fixed;
    border-radius: 50%;
    filter: blur(80px);
    pointer-events: none;
    z-index: 0;
    animation: orbFloat 12s ease-in-out infinite alternate;
  }
  .floating-orb.one { width: 300px; height: 300px; background: rgba(0,229,155,0.07); top: 5%; left: -5%; }
  .floating-orb.two { width: 250px; height: 250px; background: rgba(255,197,61,0.05); bottom: 10%; right: -5%; animation-delay: -4s; }
  .floating-orb.three { width: 200px; height: 200px; background: rgba(0,229,155,0.04); top: 50%; left: 60%; animation-delay: -8s; }

  @keyframes orbFloat {
    0% { transform: translate(0, 0) scale(1); }
    100% { transform: translate(30px, -40px) scale(1.15); }
  }

  .container {
    position: relative;
    z-index: 1;
    max-width: 860px;
    margin: 0 auto;
    padding: 0 24px;
  }

  /* ===== HERO ===== */
  .hero {
    padding: 80px 0 60px;
    text-align: center;
    position: relative;
  }

  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--accent-glow);
    border: 1px solid rgba(0,229,155,0.25);
    color: var(--accent);
    padding: 6px 18px;
    border-radius: 100px;
    font-size: 0.85rem;
    font-weight: 600;
    margin-bottom: 28px;
    letter-spacing: 0.5px;
  }
  .hero-badge i { font-size: 0.75rem; }

  .hero h1 {
    font-family: 'Space Grotesk', sans-serif;
    font-size: clamp(2.2rem, 5vw, 3.4rem);
    font-weight: 700;
    line-height: 1.15;
    margin-bottom: 20px;
    color: #fff;
  }
  .hero h1 .accent { color: var(--accent); }

  .hero-sub {
    font-size: 1.1rem;
    color: var(--muted);
    max-width: 600px;
    margin: 0 auto 32px;
    font-weight: 300;
  }

  .hero-cta {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: var(--accent);
    color: #0c0f14;
    font-weight: 600;
    font-size: 1rem;
    padding: 14px 32px;
    border-radius: 12px;
    text-decoration: none;
    transition: all 0.25s;
    box-shadow: 0 0 30px rgba(0,229,155,0.25);
  }
  .hero-cta:hover {
    transform: translateY(-2px);
    box-shadow: 0 0 50px rgba(0,229,155,0.35);
    background: #00ffaa;
  }

  /* Hero image */
  .hero-image-wrapper {
    margin: 48px auto 0;
    max-width: 700px;
    border-radius: 16px;
    overflow: hidden;
    border: 1px solid var(--border);
    position: relative;
  }
  .hero-image-wrapper img {
    width: 100%;
    display: block;
    aspect-ratio: 16/9;
    object-fit: cover;
  }
  .hero-image-caption {
    position: absolute;
    bottom: 0; left: 0; right: 0;
    background: linear-gradient(transparent, rgba(12,15,20,0.9));
    padding: 40px 20px 16px;
    font-size: 0.82rem;
    color: var(--muted);
    text-align: left;
  }

  /* ===== SECTIONS ===== */
  section {
    padding: 48px 0;
  }

  .section-label {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-size: 0.78rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1.5px;
    color: var(--accent);
    margin-bottom: 12px;
  }
  .section-label::before {
    content: '';
    width: 20px;
    height: 2px;
    background: var(--accent);
    border-radius: 2px;
  }

  h2 {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 1.85rem;
    font-weight: 700;
    color: #fff;
    margin-bottom: 16px;
    line-height: 1.25;
  }

  h3 {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 1.2rem;
    font-weight: 600;
    color: #fff;
    margin-bottom: 10px;
  }

  p {
    color: var(--muted);
    margin-bottom: 20px;
    font-size: 0.97rem;
  }

  /* ===== CARDS ===== */
  .card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 28px;
    margin-bottom: 20px;
    transition: border-color 0.3s, background 0.3s;
  }
  .card:hover {
    border-color: rgba(0,229,155,0.3);
    background: var(--card-hover);
  }

  .card-icon {
    width: 44px;
    height: 44px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.15rem;
    margin-bottom: 16px;
  }
  .card-icon.green { background: rgba(0,229,155,0.12); color: var(--accent); }
  .card-icon.gold { background: rgba(255,197,61,0.12); color: var(--gold); }
  .card-icon.red { background: rgba(255,107,74,0.12); color: var(--warn); }
  .card-icon.blue { background: rgba(56,152,255,0.12); color: #3898ff; }

  .card p { margin-bottom: 0; font-size: 0.92rem; }

  .card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 16px;
    margin-top: 24px;
  }

  /* ===== CREDIT BOX ===== */
  .credit-box {
    background: linear-gradient(135deg, rgba(255,197,61,0.08), rgba(255,197,61,0.02));
    border: 1px solid rgba(255,197,61,0.2);
    border-radius: 14px;
    padding: 28px 32px;
    margin: 24px 0;
  }
  .credit-box h3 { color: var(--gold); }
  .credit-box p { color: #b0a080; }
  .credit-box a { color: var(--gold); text-decoration: underline; text-underline-offset: 3px; }

  /* ===== IMAGE BLOCKS ===== */
  .img-block {
    margin: 32px 0;
    border-radius: 14px;
    overflow: hidden;
    border: 1px solid var(--border);
  }
  .img-block img {
    width: 100%;
    display: block;
    aspect-ratio: 16/10;
    object-fit: cover;
  }
  .img-block-caption {
    background: var(--card);
    padding: 12px 18px;
    font-size: 0.82rem;
    color: var(--muted);
    border-top: 1px solid var(--border);
  }

  .img-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin: 32px 0;
  }
  .img-grid .img-block { margin: 0; }
  @media (max-width: 600px) {
    .img-grid { grid-template-columns: 1fr; }
  }

  /* ===== STEPS ===== */
  .steps {
    counter-reset: step;
    list-style: none;
    padding: 0;
    margin: 24px 0;
  }
  .steps li {
    counter-increment: step;
    display: flex;
    gap: 18px;
    padding: 18px 0;
    border-bottom: 1px solid var(--border);
    align-items: flex-start;
  }
  .steps li:last-child { border-bottom: none; }
  .steps li::before {
    content: counter(step);
    flex-shrink: 0;
    width: 36px;
    height: 36px;
    background: var(--accent-glow);
    border: 1px solid rgba(0,229,155,0.25);
    color: var(--accent);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Space Grotesk', sans-serif;
    font-weight: 700;
    font-size: 0.9rem;
    margin-top: 2px;
  }
  .steps li strong { color: #fff; }
  .steps li span { color: var(--muted); font-size: 0.93rem; }

  /* ===== CODE BLOCK ===== */
  .code-block {
    background: var(--code-bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 24px;
    margin: 20px 0;
    overflow-x: auto;
    font-family: 'Courier New', monospace;
    font-size: 0.85rem;
    color: #c9d1d9;
    line-height: 1.7;
  }
  .code-block .comment { color: #6a737d; }
  .code-block .keyword { color: var(--accent); }
  .code-block .string { color: #ffc53d; }
  .code-block .number { color: #ff6b4a; }

  /* ===== DIAGRAM ===== */
  .wiring-diagram {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 32px;
    margin: 28px 0;
    overflow-x: auto;
  }
  .wiring-diagram table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.9rem;
  }
  .wiring-diagram th {
    background: rgba(0,229,155,0.08);
    color: var(--accent);
    padding: 12px 16px;
    text-align: left;
    font-weight: 600;
    font-size: 0.82rem;
    text-transform: uppercase;
    letter-spacing: 0.8px;
    border-bottom: 1px solid var(--border);
  }
  .wiring-diagram td {
    padding: 11px 16px;
    border-bottom: 1px solid rgba(42,48,64,0.5);
    color: var(--muted);
  }
  .wiring-diagram tr:last-child td { border-bottom: none; }
  .wiring-diagram .pin { color: #fff; font-family: 'Courier New', monospace; font-weight: 600; }

  /* ===== CHECKLIST ===== */
  .checklist {
    list-style: none;
    padding: 0;
    margin: 16px 0;
  }
  .checklist li {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    padding: 8px 0;
    color: var(--muted);
    font-size: 0.94rem;
  }
  .checklist li i {
    color: var(--accent);
    margin-top: 4px;
    font-size: 0.8rem;
    flex-shrink: 0;
  }

  /* ===== SENSOR GRID ===== */
  .sensor-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    overflow: hidden;
    transition: border-color 0.3s, transform 0.3s;
  }
  .sensor-card:hover {
    border-color: rgba(0,229,155,0.3);
    transform: translateY(-3px);
  }
  .sensor-card-img {
    width: 100%;
    aspect-ratio: 16/9;
    object-fit: cover;
    display: block;
  }
  .sensor-card-body { padding: 20px; }
  .sensor-card-body h3 { margin-bottom: 6px; }
  .sensor-card-body p { font-size: 0.88rem; margin-bottom: 0; }
  .sensor-tag {
    display: inline-block;
    background: rgba(0,229,155,0.1);
    color: var(--accent);
    padding: 3px 10px;
    border-radius: 6px;
    font-size: 0.75rem;
    font-weight: 600;
    margin-bottom: 10px;
  }

  /* ===== ABOUT ===== */
  .about-section {
    background: linear-gradient(135deg, var(--card), var(--bg2));
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 40px;
    margin: 32px 0;
    display: flex;
    gap: 32px;
    align-items: center;
  }
  .about-avatar {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 2.4rem;
    font-weight: 700;
    color: var(--bg);
    flex-shrink: 0;
    border: 3px solid rgba(0,229,155,0.3);
  }
  .about-text h2 { margin-bottom: 8px; }
  .about-text p { margin-bottom: 8px; font-size: 0.95rem; }
  @media (max-width: 600px) {
    .about-section { flex-direction: column; text-align: center; padding: 28px; }
  }

  /* ===== STAR BANNER ===== */
  .star-banner {
    background: linear-gradient(135deg, rgba(255,197,61,0.1), rgba(255,197,61,0.03));
    border: 1px solid rgba(255,197,61,0.2);
    border-radius: 16px;
    padding: 36px 40px;
    text-align: center;
    margin: 40px 0;
  }
  .star-banner h2 { color: var(--gold); margin-bottom: 12px; }
  .star-banner p { color: #b0a080; max-width: 560px; margin: 0 auto 20px; }
  .star-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: var(--gold);
    color: #1a1200;
    font-weight: 700;
    font-size: 1rem;
    padding: 14px 36px;
    border-radius: 12px;
    text-decoration: none;
    transition: all 0.25s;
    box-shadow: 0 0 30px rgba(255,197,61,0.2);
  }
  .star-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 0 50px rgba(255,197,61,0.35);
    background: #ffd866;
  }

  /* ===== LICENSE ===== */
  .license-box {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 28px;
    margin: 24px 0;
  }
  .license-box p { font-size: 0.88rem; margin-bottom: 10px; }
  .license-box p:last-child { margin-bottom: 0; }

  /* ===== FOOTER ===== */
  footer {
    text-align: center;
    padding: 40px 0 60px;
    border-top: 1px solid var(--border);
    margin-top: 40px;
  }
  footer p { color: var(--muted); font-size: 0.85rem; margin-bottom: 4px; }
  footer .accent-text { color: var(--accent); font-weight: 600; }

  /* ===== DIVIDER ===== */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 16px 0;
  }

  /* ===== ANIMATIONS ===== */
  .fade-up {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .fade-up.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* ===== NAV ===== */
  .top-nav {
    position: sticky;
    top: 0;
    z-index: 100;
    background: rgba(12,15,20,0.85);
    backdrop-filter: blur(16px);
    border-bottom: 1px solid var(--border);
    padding: 0 24px;
  }
  .top-nav-inner {
    max-width: 860px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 56px;
  }
  .top-nav-logo {
    font-family: 'Space Grotesk', sans-serif;
    font-weight: 700;
    font-size: 0.95rem;
    color: #fff;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .top-nav-logo i { color: var(--accent); }
  .top-nav-links {
    display: flex;
    gap: 6px;
    list-style: none;
  }
  .top-nav-links a {
    color: var(--muted);
    text-decoration: none;
    font-size: 0.82rem;
    padding: 6px 12px;
    border-radius: 8px;
    transition: all 0.2s;
    font-weight: 500;
  }
  .top-nav-links a:hover {
    color: var(--accent);
    background: var(--accent-glow);
  }
  @media (max-width: 640px) {
    .top-nav-links { display: none; }
  }

  /* Scrollbar */
  ::-webkit-scrollbar { width: 8px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--border); border-radius: 4px; }
  ::-webkit-scrollbar-thumb:hover { background: #3a4255; }

  /* Toast */
  .toast {
    position: fixed;
    bottom: 30px;
    right: 30px;
    background: var(--card);
    border: 1px solid var(--border);
    color: var(--fg);
    padding: 14px 22px;
    border-radius: 12px;
    font-size: 0.88rem;
    z-index: 999;
    opacity: 0;
    transform: translateY(20px);
    transition: all 0.35s;
    pointer-events: none;
    box-shadow: 0 8px 32px rgba(0,0,0,0.4);
  }
  .toast.show {
    opacity: 1;
    transform: translateY(0);
    pointer-events: auto;
  }
</style>
</head>
<body>

<div class="bg-grid"></div>
<div class="floating-orb one"></div>
<div class="floating-orb two"></div>
<div class="floating-orb three"></div>

<!-- Navigation -->
<nav class="top-nav">
  <div class="top-nav-inner">
    <div class="top-nav-logo"><i class="fas fa-microchip"></i> PWM Flight Controller</div>
    <ul class="top-nav-links">
      <li><a href="#features">Features</a></li>
      <li><a href="#wiring">Wiring</a></li>
      <li><a href="#sensors">Sensors</a></li>
      <li><a href="#quickstart">Quick Start</a></li>
      <li><a href="#about">About</a></li>
    </ul>
  </div>
</nav>

<!-- Hero -->
<header class="hero">
  <div class="container">
    <div class="hero-badge"><i class="fas fa-trophy"></i> INSPIRE AWARD 2026</div>
    <h1>PWM-Based<br><span class="accent">Flight Controller</span></h1>
    <p class="hero-sub">A complete open-source control system for RC aircraft and drones — built with Arduino, calibrated for precision, and ready for sensor expansion.</p>
    <a href="#" class="hero-cta" id="starBtn"><i class="fas fa-star"></i> Star This Repository</a>

    <div class="hero-image-wrapper fade-up">
      <img src="https://picsum.photos/seed/drone-circuit-pwm/800/450.jpg" alt="PWM Flight Controller Build">
      <div class="hero-image-caption"><i class="fas fa-camera" style="margin-right:6px;"></i> Prototype setup — Arduino Nano connected to a 6-channel PWM receiver with ESC and servo outputs</div>
    </div>
  </div>
</header>

<main>
<div class="container">

  <!-- What This Is -->
  <section class="fade-up">
    <div class="section-label">Overview</div>
    <h2>What Is This Project?</h2>
    <p>This repository contains everything you need to build a PWM-based flight controller from scratch. It includes the full calibration routine, light controller code, and a reliable PWM communication protocol — all adapted from <strong style="color:#fff;">Pratik Phadte's</strong> excellent Instructables tutorials, with additional sensor integrations and documentation for the Inspire Award.</p>
    <p>The system reads standard 1–2 ms PWM pulses from any 6-channel RC receiver, maps them to precise control values through a calibration process, and outputs signals to ESCs (electronic speed controllers) and servos. You can optionally add a barometer, GPS module, and compass for advanced autonomous flight features.</p>

    <div class="img-grid">
      <div class="img-block fade-up">
        <img src="https://picsum.photos/seed/arduino-nano-esc/500/312.jpg" alt="Arduino Nano with ESC connections">
        <div class="img-block-caption"><i class="fas fa-bolt" style="margin-right:6px;color:var(--warn);"></i> Arduino Nano wired to ESC signal pins</div>
      </div>
      <div class="img-block fade-up">
        <img src="https://picsum.photos/seed/rc-transmitter-fs/500/312.jpg" alt="6-channel RC transmitter">
        <div class="img-block-caption"><i class="fas fa-gamepad" style="margin-right:6px;color:var(--accent);"></i> Any 6-channel PWM transmitter works</div>
      </div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- Features -->
  <section id="features" class="fade-up">
    <div class="section-label">Capabilities</div>
    <h2>Key Features</h2>
    <p>Every component in this build serves a specific purpose. Here's what's included and why it matters:</p>

    <div class="card-grid">
      <div class="card">
        <div class="card-icon green"><i class="fas fa-sliders-h"></i></div>
        <h3>Precision Calibration</h3>
        <p>Pratik Phadte's calibration routine maps your exact transmitter stick endpoints — no guessing, no drift. Every channel gets min/max/center values stored in EEPROM.</p>
      </div>
      <div class="card">
        <div class="card-icon gold"><i class="fas fa-lightbulb"></i></div>
        <h3>Light Controller</h3>
        <p>Drives LED strips, status indicators, and visual alerts through PWM outputs. Useful for orientation cues during flight and low-light visibility.</p>
      </div>
      <div class="card">
        <div class="card-icon blue"><i class="fas fa-wave-square"></i></div>
        <h3>PWM Protocol</h3>
        <p>Reliable pulse-width reading on 6 independent channels. Uses <code style="background:var(--code-bg);padding:2px 6px;border-radius:4px;color:var(--accent);font-size:0.82rem;">pulseIn()</code> with timeout handling and signal validation.</p>
      </div>
      <div class="card">
        <div class="card-icon red"><i class="fas fa-universal-access"></i></div>
        <h3>Universal TX/RX</h3>
        <p>Compatible with FlySky FS-i6, Radiolink AT9S, FrSky, or any receiver that outputs standard PWM on separate pins. No proprietary protocols needed.</p>
      </div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- Credits -->
  <section class="fade-up">
    <div class="credit-box">
      <h3><i class="fas fa-heart" style="margin-right:8px;"></i>Credits & Acknowledgment</h3>
      <p>This project stands on the shoulders of <strong style="color:var(--gold);">Pratik Phadte's</strong> open-source work. The calibration logic, light controller code, and PWM communication protocol are adapted from his Instructables tutorials.</p>
      <p style="margin-top:12px;">Please respect the original license and always provide attribution when reusing or redistributing these components. Find his articles by searching <a href="#">"Pratik Phadte PWM protocol"</a> or <a href="#">"Pratik Phadte light controller"</a> on Instructables.</p>
    </div>
  </section>

  <div class="divider"></div>

  <!-- Transmitter Requirements -->
  <section class="fade-up">
    <div class="section-label">Hardware</div>
    <h2>Transmitter & Receiver Requirements</h2>
    <p>You need a 6-channel (or more) RC system where the receiver outputs individual PWM signals — one signal wire per channel. This is the most common output mode for budget RC systems.</p>

    <div class="img-block fade-up">
      <img src="https://picsum.photos/seed/pwm-receiver-channels/800/400.jpg" alt="PWM receiver channel layout">
      <div class="img-block-caption"><i class="fas fa-info-circle" style="margin-right:6px;color:#3898ff;"></i> Each channel outputs a separate PWM signal wire — this is what the code expects</div>
    </div>

    <ul class="checklist">
      <li><i class="fas fa-check-circle"></i> <span><strong style="color:#fff;">FlySky FS-i6 + FS-iA6B</strong> — the most affordable option, works perfectly out of the box</span></li>
      <li><i class="fas fa-check-circle"></i> <span><strong style="color:#fff;">Radiolink AT9S + R9DS</strong> — longer range, also outputs PWM by default</span></li>
      <li><i class="fas fa-check-circle"></i> <span><strong style="color:#fff;">FrSky Taranis + X8R</strong> — make sure to set output mode to PWM (not SBUS/PPM)</span></li>
      <li><i class="fas fa-times-circle" style="color:var(--warn);"></i> <span>Do NOT use SBUS, PPM, CRSF, or other serial protocols unless you add a converter — this code reads <strong style="color:#fff;">separate PWM pins only</strong></span></li>
    </ul>
  </section>

  <div class="divider"></div>

  <!-- Wiring Diagram -->
  <section id="wiring" class="fade-up">
    <div class="section-label">Connection Guide</div>
    <h2>Wiring Diagram</h2>
    <p>Connect your PWM receiver channels to the Arduino's digital pins as shown below. The receiver needs 5V power and a common ground with the Arduino.</p>

    <div class="wiring-diagram">
      <table>
        <thead>
          <tr>
            <th>Receiver Channel</th>
            <th>Function</th>
            <th>Arduino Pin</th>
            <th>PWM Range</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><span class="pin">CH1</span></td>
            <td>Aileron (Roll)</td>
            <td><span class="pin">D2</span></td>
            <td>1000 – 2000 μs</td>
          </tr>
          <tr>
            <td><span class="pin">CH2</span></td>
            <td>Elevator (Pitch)</td>
            <td><span class="pin">D3</span></td>
            <td>1000 – 2000 μs</td>
          </tr>
          <tr>
            <td><span class="pin">CH3</span></td>
            <td>Throttle</td>
            <td><span class="pin">D4</span></td>
            <td>1000 – 2000 μs</td>
          </tr>
          <tr>
            <td><span class="pin">CH4</span></td>
            <td>Rudder (Yaw)</td>
            <td><span class="pin">D5</span></td>
            <td>1000 – 2000 μs</td>
          </tr>
          <tr>
            <td><span class="pin">CH5</span></td>
            <td>Aux 1 (Mode/Gear)</td>
            <td><span class="pin">D6</span></td>
            <td>1000 – 2000 μs</td>
          </tr>
          <tr>
            <td><span class="pin">CH6</span></td>
            <td>Aux 2 (Aux Switch)</td>
            <td><span class="pin">D7</span></td>
            <td>1000 – 2000 μs</td>
          </tr>
          <tr>
            <td><span class="pin">5V</span></td>
            <td>Power (from Arduino)</td>
            <td><span class="pin">5V</span></td>
            <td>—</td>
          </tr>
          <tr>
            <td><span class="pin">GND</span></td>
            <td>Common Ground</td>
            <td><span class="pin">GND</span></td>
            <td>—</td>
          </tr>
        </tbody>
      </table>
    </div>

    <div class="img-block fade-up">
      <img src="https://picsum.photos/seed/wiring-breadboard-arduino/800/400.jpg" alt="Breadboard wiring setup">
      <div class="img-block-caption"><i class="fas fa-plug" style="margin-right:6px;color:var(--accent);"></i> Breadboard prototype — receiver signal wires go to D2–D7, power shares 5V and GND</div>
    </div>

    <div class="card" style="border-color:rgba(255,107,74,0.3);background:rgba(255,107,74,0.04);">
      <div class="card-icon red"><i class="fas fa-exclamation-triangle"></i></div>
      <h3>Voltage Warning</h3>
      <p>Most RC receivers operate at 4.8–6V, which matches the Arduino's 5V output. However, if you're using a 3.3V microcontroller (like ESP32 or Raspberry Pi Pico), you <strong style="color:#fff;">must</strong> use a logic level converter on the signal lines, or you risk damaging the pins.</p>
    </div>
  </section>

  <div class="divider"></div>

  <!-- Code Example -->
  <section class="fade-up">
    <div class="section-label">Code</div>
    <h2>How the PWM Reading Works</h2>
    <p>The core of this project is reading PWM pulse widths from the receiver. Here's the fundamental approach used throughout the codebase:</p>

    <div class="code-block">
<span class="comment">// Define pins for each channel</span>
<span class="keyword">const int</span> chPins[<span class="number">6</span>] = {<span class="number">2</span>, <span class="number">3</span>, <span class="number">4</span>, <span class="number">5</span>, <span class="number">6</span>, <span class="number">7</span>};
<span class="keyword">int</span> chValues[<span class="number">6</span>];

<span class="keyword">void</span> <span class="keyword">readChannels</span>() {
  <span class="keyword">for</span> (<span class="keyword">int</span> i = <span class="number">0</span>; i < <span class="number">6</span>; i++) {
    <span class="comment">// Read pulse width in microseconds (timeout: 25000μs)</span>
    chValues[i] = <span class="keyword">pulseIn</span>(chPins[i], <span class="number">HIGH</span>, <span class="number">25000</span>);

    <span class="comment">// Validate signal — if no signal, default to center (1500μs)</span>
    <span class="keyword">if</span> (chValues[i] == <span class="number">0</span>) chValues[i] = <span class="number">1500</span>;

    <span class="comment">// Constrain to safe range</span>
    chValues[i] = <span class="keyword">constrain</span>(chValues[i], <span class="number">1000</span>, <span class="number">2000</span>);
  }
}
    </div>

    <p>After reading raw values, the <strong style="color:#fff;">calibration routine</strong> maps each channel's raw range (which varies between transmitters) to a normalized 0–1000 or -500 to +500 range. This ensures consistent behavior regardless of which TX/RX you use.</p>
  </section>

  <div class="divider"></div>

  <!-- Sensors -->
  <section id="sensors" class="fade-up">
    <div class="section-label">Expansion</div>
    <h2>Optional Sensor Enhancements</h2>
    <p>The base build handles manual RC control. Add these sensors via I2C or UART to unlock autonomous flight capabilities:</p>

    <div class="card-grid" style="grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); margin-top:28px;">
      <div class="sensor-card">
        <img class="sensor-card-img" src="https://picsum.photos/seed/bmp280-sensor-module/400/225.jpg" alt="BMP280 Barometer">
        <div class="sensor-card-body">
          <span class="sensor-tag">I2C</span>
          <h3>Barometer (BMP280)</h3>
          <p>Measures atmospheric pressure to calculate altitude. Essential for altitude hold and vertical speed telemetry.</p>
        </div>
      </div>
      <div class="sensor-card">
        <img class="sensor-card-img" src="https://picsum.photos/seed/neo6m-gps-module/400/225.jpg" alt="NEO-6M GPS Module">
        <div class="sensor-card-body">
          <span class="sensor-tag">UART</span>
          <h3>GPS (NEO-6M / NEO-M8N)</h3>
          <p>Provides latitude, longitude, speed, and heading. Enables return-to-home and waypoint navigation.</p>
        </div>
      </div>
      <div class="sensor-card">
        <img class="sensor-card-img" src="https://picsum.photos/seed/hmc5883l-compass/400/225.jpg" alt="HMC5883L Compass">
        <div class="sensor-card-body">
          <span class="sensor-tag">I2C</span>
          <h3>Compass (HMC5883L)</h3>
          <p>Provides absolute magnetic heading reference. Critical for autonomous yaw control and heading hold.</p>
        </div>
      </div>
    </div>

    <div class="wiring-diagram" style="margin-top:28px;">
      <table>
        <thead>
          <tr>
            <th>Sensor</th>
            <th>Interface</th>
            <th>SDA / TX</th>
            <th>SCL / RX</th>
            <th>VCC</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><span class="pin">BMP280</span></td>
            <td>I2C</td>
            <td><span class="pin">A4</span></td>
            <td><span class="pin">A5</span></td>
            <td><span class="pin">3.3V</span></td>
          </tr>
          <tr>
            <td><span class="pin">NEO-6M</span></td>
            <td>UART</td>
            <td><span class="pin">D10 (RX)</span></td>
            <td><span class="pin">D11 (TX)</span></td>
            <td><span class="pin">3.3V</span></td>
          </tr>
          <tr>
            <td><span class="pin">HMC5883L</span></td>
            <td>I2C</td>
            <td><span class="pin">A4</span></td>
            <td><span class="pin">A5</span></td>
            <td><span class="pin">3.3V</span></td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>

  <div class="divider"></div>

  <!-- Quick Start -->
  <section id="quickstart" class="fade-up">
    <div class="section-label">Setup</div>
    <h2>Quick Start Guide</h2>
    <p>Follow these steps to get the flight controller running from zero:</p>

    <ol class="steps">
      <li>
        <div>
          <strong>Clone or download the repository</strong><br>
          <span>Use <code style="background:var(--code-bg);padding:2px 8px;border-radius:4px;color:var(--accent);font-size:0.85rem;">git clone</code> or download the ZIP from GitHub to your local machine.</span>
        </div>
      </li>
      <li>
        <div>
          <strong>Upload the calibration sketch first</strong><br>
          <span>Open <code style="background:var(--code-bg);padding:2px 8px;border-radius:4px;color:var(--accent);font-size:0.85rem;">/calibration/calibrate_pwm.ino</code> in Arduino IDE. Follow Pratik Phadte's instructions — move each stick to its extremes to record min/max/center values into EEPROM.</span>
        </div>
      </li>
      <li>
        <div>
          <strong>Wire your receiver</strong><br>
          <span>Connect CH1–CH6 signal wires to Arduino pins D2–D7. Share 5V and GND. Double-check polarity before powering on.</span>
        </div>
      </li>
      <li>
        <div>
          <strong>Load the main controller code</strong><br>
          <span>Upload <code style="background:var(--code-bg);padding:2px 8px;border-radius:4px;color:var(--accent);font-size:0.85rem;">/main/flight_controller.ino</code> — this includes PWM reading, calibrated mapping, light controller, and servo/ESC output logic.</span>
        </div>
      </li>
      <li>
        <div>
          <strong>Test each channel</strong><br>
          <span>Open the Serial Monitor (115200 baud). Move each stick and verify that the calibrated values respond smoothly across the full range.</span>
        </div>
      </li>
      <li>
        <div>
          <strong>Add sensors (optional)</strong><br>
          <span>Uncomment the BMP280, GPS, or compass sections in the code. Wire them per the pin table above. Re-upload and verify sensor readings in Serial Monitor.</span>
        </div>
      </li>
      <li>
        <div>
          <strong>Credit Pratik Phadte</strong><br>
          <span>In any public showcase, video, or derivative work, credit Pratik Phadte for the original calibration, light controller, and PWM protocol code from Instructables.</span>
        </div>
      </li>
      <li>
        <div>
          <strong>Star the repository</strong><br>
          <span>If this helped your project, hit the Star button to support further development and help other makers discover it.</span>
        </div>
      </li>
    </ol>

    <div class="img-block fade-up">
      <img src="https://picsum.photos/seed/serial-monitor-output/800/350.jpg" alt="Serial Monitor output showing calibrated PWM values">
      <div class="img-block-caption"><i class="fas fa-terminal" style="margin-right:6px;color:var(--accent);"></i> Serial Monitor output showing calibrated channel values after running the main controller sketch</div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- About -->
  <section id="about" class="fade-up">
    <div class="section-label">Creator</div>
    <div class="about-section">
      <div class="about-avatar">AP</div>
      <div class="about-text">
        <h2>Atharva Phadnis</h2>
        <p style="color:var(--accent);font-weight:600;font-size:0.9rem;margin-bottom:12px;">Age 13 &middot; First Inspire Award Project</p>
        <p>I'm a 13-year-old student who has been passionate about electronics, coding, and RC systems since I was 10. This project uses Pratik Phadte's amazing PWM resources as a foundation, and I've added my own calibration tweaks and sensor integrations to make it competition-ready.</p>
        <p>Participating in the Inspire Award is a dream come true — I want to show other kids my age that building real engineering projects is possible, even without a lab or a big budget. All you need is curiosity and willingness to learn from open-source communities.</p>
      </div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- License -->
  <section class="fade-up">
    <div class="section-label">Legal</div>
    <h2>License & Attribution</h2>
    <div class="license-box">
      <p><i class="fas fa-file-contract" style="color:var(--accent);margin-right:8px;"></i> This repository is provided for <strong style="color:#fff;">educational and non-commercial Inspire Award projects</strong>.</p>
      <p><i class="fas fa-user-check" style="color:var(--gold);margin-right:8px;"></i> You <strong style="color:#fff;">must credit Pratik Phadte</strong> for the original calibration routine, light controller code, and PWM protocol from Instructables.</p>
      <p><i class="fas fa-code-branch" style="color:#3898ff;margin-right:8px;"></i> If you modify or redistribute this code, keep all credits intact and link back to the original sources.</p>
      <p><i class="fas fa-puzzle-piece" style="color:var(--warn);margin-right:8px;"></i> The optional sensor integrations (barometer, GPS, compass) are community contributions — free to use with attribution.</p>
      <p><i class="fas fa-user-graduate" style="color:var(--accent);margin-right:8px;"></i> Additional credit: <strong style="color:#fff;">Atharva Phadnis</strong> for the Inspire Award build integration, documentation, and sensor examples.</p>
    </div>
  </section>

  <div class="divider"></div>

  <!-- Star Banner -->
  <section class="fade-up">
    <div class="star-banner">
      <h2><i class="fas fa-star" style="margin-right:10px;"></i>Support a Young Maker's Journey</h2>
      <p>This repository represents months of learning, debugging, and building as a 13-year-old student. If the PWM protocol, calibration tools, or documentation helped you — please star it. Your support means the world.</p>
      <a href="#" class="star-btn" id="starBtn2"><i class="fas fa-star"></i> Star This Repository</a>
    </div>
  </section>

</div>
</main>

<!-- Footer -->
<footer>
  <div class="container">
    <p>Built with dedication by <span class="accent-text">Atharva Phadnis</span> (age 13)</p>
    <p>With deep respect for <span class="accent-text">Pratik Phadte's</span> open-source contributions</p>
    <p style="margin-top:12px;font-size:0.78rem;color:#555;">Inspire Award 2026 &middot; PWM Flight Controller &middot; Arduino &middot; Open Source</p>
  </div>
</footer>

<!-- Toast notification -->
<div class="toast" id="toast"></div>

<script>
  // Scroll reveal animation
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });

  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

  // Toast notification system
  function showToast(message, duration) {
    const toast = document.getElementById('toast');
    toast.innerHTML = message;
    toast.classList.add('show');
    setTimeout(() => toast.classList.remove('show'), duration || 3000);
  }

  // Star button interactions
  document.getElementById('starBtn').addEventListener('click', function(e) {
    e.preventDefault();
    showToast('<i class="fas fa-heart" style="color:var(--warn);margin-right:8px;"></i> Thank you for your support! Please star the repo on GitHub.', 3500);
  });
  document.getElementById('starBtn2').addEventListener('click', function(e) {
    e.preventDefault();
    showToast('<i class="fas fa-star" style="color:var(--gold);margin-right:8px;"></i> Your star means a lot — thank you!', 3500);
  });

  // Smooth scroll for nav links
  document.querySelectorAll('.top-nav-links a').forEach(link => {
    link.addEventListener('click', function(e) {
      const href = this.getAttribute('href');
      if (href.startsWith('#')) {
        e.preventDefault();
        const target = document.querySelector(href);
        if (target) {
          target.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
      }
    });
  });

  // Subtle parallax on hero image
  window.addEventListener('scroll', () => {
    const scrollY = window.scrollY;
    const heroImg = document.querySelector('.hero-image-wrapper');
    if (heroImg && scrollY < 800) {
      heroImg.style.transform = `translateY(${scrollY * 0.06}px)`;
    }
  }, { passive: true });
</script>

</body>
</html>
