<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Inspire Award Build – PWM Flight Controller (Atharva Phadnis, 13)</title>
    <style>
        /* clean, modern, "non-shabby" styling – neat spacing, soft shadows, readable */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
            background: #f8fafc;
            color: #0a0c10;
            line-height: 1.5;
            padding: 2rem 1rem;
        }

        .readme-container {
            max-width: 880px;
            margin: 0 auto;
            background: #ffffff;
            border-radius: 28px;
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.05), 0 4px 8px rgba(0, 0, 0, 0.02);
            padding: 2rem 2rem 2.5rem 2rem;
            transition: all 0.2s ease;
        }

        /* each sentence gets its own block with clean spacing */
        .sentence {
            display: block;
            margin-bottom: 0.75rem;
            line-height: 1.5;
        }

        /* for inline grouping when needed, but we keep sentence spacing */
        h1, h2, h3 {
            margin-top: 1.6em;
            margin-bottom: 0.75em;
            font-weight: 600;
            letter-spacing: -0.01em;
            border-bottom: 2px solid #eef2f6;
            padding-bottom: 0.3em;
        }

        h1 {
            font-size: 2rem;
            margin-top: 0.2em;
            border-bottom: none;
            background: linear-gradient(135deg, #1e2b3c, #0f3b4f);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            display: inline-block;
            border-bottom: 2px solid #cbd5e1;
            padding-bottom: 0.2rem;
        }

        .intro-card {
            background: #eef4ff;
            border-radius: 20px;
            padding: 1.2rem 1.6rem;
            margin: 1.5rem 0 2rem 0;
            border-left: 6px solid #1e6fdf;
            box-shadow: 0 2px 6px rgba(0,0,0,0.02);
        }

        .star-badge {
            background: #f5b042;
            color: #1e2a2e;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            padding: 0.3rem 0.9rem;
            border-radius: 40px;
            font-weight: 700;
            font-size: 0.85rem;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }

        .badge-icon {
            font-size: 1.1rem;
        }

        hr {
            margin: 2rem 0;
            border: none;
            height: 1px;
            background: linear-gradient(to right, #e2e8f0, #cbd5e1, #e2e8f0);
        }

        code {
            background: #f1f5f9;
            padding: 0.2rem 0.4rem;
            border-radius: 8px;
            font-family: 'SF Mono', 'Fira Code', monospace;
            font-size: 0.85em;
            color: #0f172a;
        }

        .footer-note {
            margin-top: 2rem;
            text-align: center;
            font-size: 0.85rem;
            color: #334155;
            border-top: 1px solid #eef2f6;
            padding-top: 1.8rem;
        }

        /* Responsive */
        @media (max-width: 600px) {
            .readme-container {
                padding: 1.5rem;
            }
            h1 {
                font-size: 1.7rem;
            }
        }
    </style>
</head>
<body>
<div class="readme-container">
    
    <!-- main heading -->
    <h1>✨ Inspire Award Build – PWM Flight Controller ✨</h1>
    <div style="height: 0.5rem;"></div>
    
    <!-- intro card: Atharva Phadnis, 13 years old, first Inspire Award -->
    <div class="intro-card">
        <span class="sentence"><strong>👋 Hey everyone, I'm Atharva Phadnis.</strong></span>
        <span class="sentence">I am <strong>13 years old</strong> and this is my <strong>first Inspire Award project</strong> – I'm incredibly excited to participate! 🚀</span>
        <span class="sentence">Building drones and RC systems has been my passion since I was 10, and now I'm sharing my work with the world.</span>
        <span class="sentence">Please support a young maker: <strong>⭐ star this repository ⭐</strong> – it means the world to me!</span>
    </div>
    
    <!-- core description: Pratik Phadte credits + PWM protocol + any 6ch -->
    <span class="sentence"><strong>🔹 Based on Pratik Phadte's resources & Instructables PWM protocol 🔹</strong></span>
    <span class="sentence">This repository contains the complete code, calibration routines, and wiring guidance for a robust PWM‑based control system.</span>
    <span class="sentence">It uses <strong>Pratik Phadte's calibration</strong> routine to get precise stick ranges and servo outputs.</span>
    <span class="sentence">The <strong>light controller code</strong> from Pratik Phadte is included – perfect for LED indicators or visual feedback.</span>
    <span class="sentence">Transmitter and receiver implementation follows the <strong>PWM protocol</strong> originally shared on Instructables.</span>
    <span class="sentence">You can use <strong>any 6‑channel transmitter and receiver</strong> as long as they output standard PWM signals (1–2 ms pulse width).</span>
    <span class="sentence">Make sure to <strong>give full credit to Pratik Phadte</strong> for the foundational work on calibration, light controller, and PWM communication.</span>
    <span class="sentence">Optionally, you can <strong>add a barometer, GPS module, and compass</strong> to expand functionality (altitude hold, navigation, heading).</span>
    <span class="sentence">This repository is <strong>dedicated to my Inspire Award build</strong> – a project that showcases innovation in remote‑controlled systems.</span>
    <span class="sentence">If this helps you with your own science or engineering project, <strong>please ⭐ star this repository ⭐</strong> to support further development and updates.</span>
    
    <hr>
    
    <h2>📌 Key Features & Components</h2>
    <span class="sentence">✅ <strong>Calibration routine</strong> – based directly on Pratik Phadte's method, ensures accurate PWM mapping.</span>
    <span class="sentence">✅ <strong>Light controller code</strong> – drives LEDs, status lights, or visual alerts using PWM outputs.</span>
    <span class="sentence">✅ <strong>PWM protocol implementation</strong> – reliable communication between any 6‑channel PWM receiver and your microcontroller.</span>
    <span class="sentence">✅ <strong>Universal TX/RX compatibility</strong> – works with FlySky, Radiolink, FrSky, or any 6‑channel set that outputs PWM.</span>
    <span class="sentence">✅ <strong>Optional sensor expansion</strong> – barometer (altitude), GPS (position/waypoints), compass (magnetometer for yaw).</span>
    
    <hr>
    
    <h2>🧰 Pratik Phadte Resources – Credits & Acknowledgment</h2>
    <span class="sentence">This project would not be possible without the open work shared by <strong>Pratik Phadte</strong> on Instructables.</span>
    <span class="sentence">The <strong>calibration logic, light controller code, and transmitter/receiver PWM protocol</strong> are adapted from his excellent tutorials.</span>
    <span class="sentence">Please <strong>respect the original license</strong> and always provide attribution when reusing or redistributing these components.</span>
    <span class="sentence">You can find the original Instructables articles by searching "Pratik Phadte PWM protocol" or "Pratik Phadte light controller".</span>
    <span class="sentence">🙏 <strong>Big thanks to Pratik Phadte</strong> for making RC and drone development accessible to everyone!</span>
    
    <hr>
    
    <h2>🕹️ Transmitter & Receiver – PWM Requirements</h2>
    <span class="sentence">Any <strong>6‑channel (or more) transmitter and receiver</strong> can be used as long as the receiver outputs <strong>individual PWM signals</strong> on each channel.</span>
    <span class="sentence">Typical examples: FlySky FS‑i6 with FS‑iA6B receiver, Radiolink AT9S, or any standard RC system in PWM mode.</span>
    <span class="sentence">Do <strong>not</strong> use SBUS, PPM, or other serial protocols unless you convert them to PWM – this code strictly expects separate PWM input pins.</span>
    <span class="sentence">Connect the receiver's PWM outputs (CH1 to CH6) directly to the microcontroller's digital input pins (with appropriate voltage levels).</span>
    <span class="sentence">Then run the <strong>calibration sketch</strong> to map your transmitter's stick movements to the full PWM range.</span>
    
    <hr>
    
    <h2>🧭 Optional Enhancements: Barometer, GPS, Compass</h2>
    <span class="sentence">You are free to <strong>add extra sensors</strong> to make your Inspire Award build even more advanced.</span>
    <span class="sentence">✨ <strong>Barometer</strong> (e.g., BMP280, MS5611) – provides altitude hold, telemetry, and stable height control.</span>
    <span class="sentence">✨ <strong>GPS module</strong> (e.g., NEO‑6M, NEO‑M8N) – enables position tracking, return‑to‑home, and waypoint navigation.</span>
    <span class="sentence">✨ <strong>Compass / magnetometer</strong> (e.g., HMC5883L, QMC5883L) – gives absolute heading (yaw) reference for autonomous flight.</span>
    <span class="sentence">These sensors can be integrated via I2C or UART, and the codebase includes examples for reading them alongside PWM inputs.</span>
    
    <hr>
    
    <h2>🚀 Quick Start – Getting the Code Running</h2>
    <span class="sentence">1️⃣ <strong>Clone this repository</strong> to your local machine or download the ZIP.</span>
    <span class="sentence">2️⃣ <strong>Upload the calibration sketch</strong> first – follow Pratik Phadte's instructions to map your transmitter endpoints.</span>
    <span class="sentence">3️⃣ <strong>Connect your 6‑channel PWM receiver</strong> to the defined pins (check the wiring diagram in /docs).</span>
    <span class="sentence">4️⃣ <strong>Load the main controller code</strong> which includes the light controller and PWM protocol logic.</span>
    <span class="sentence">5️⃣ <strong>Test each channel</strong> – throttle, aileron, elevator, rudder, and aux channels should respond smoothly.</span>
    <span class="sentence">6️⃣ <strong>If you have a barometer/GPS/compass</strong>, uncomment the respective sections in the code and wire them correctly.</span>
    <span class="sentence">7️⃣ <strong>Give proper credit to Pratik Phadte</strong> in any public showcase or derivative work.</span>
    <span class="sentence">8️⃣ Finally, <strong>⭐ star this repository ⭐</strong> to show appreciation and help other makers find it!</span>
    
    <hr>
    
    <h2>👦 About the Creator – Atharva Phadnis (Age 13)</h2>
    <span class="sentence">My name is <strong>Atharva Phadnis</strong>, and I am thrilled to share my <strong>first Inspire Award project</strong> with the world.</span>
    <span class="sentence">I am <strong>13 years old</strong> and I have been passionate about electronics, coding, and RC systems since I was 10.</span>
    <span class="sentence">This project uses Pratik Phadte's amazing PWM resources, and I have added my own calibration tweaks and sensor integrations.</span>
    <span class="sentence">Participating in the <strong>Inspire Award</strong> is a dream come true – I want to inspire other kids my age to build and innovate.</span>
    <span class="sentence">Please <strong>star this repo</strong> to encourage me and show that young makers can create professional‑grade projects!</span>
    
    <hr>
    
    <h2>📜 License & Attribution Requirement</h2>
    <span class="sentence">This repository is provided for educational and non‑commercial Inspire Award projects.</span>
    <span class="sentence"><strong>You must credit Pratik Phadte</strong> for the original calibration, light controller code, and PWM protocol from Instructables.</span>
    <span class="sentence">If you modify or redistribute this code, keep the credits intact and link back to the original sources.</span>
    <span class="sentence">The optional sensor integrations (barometer, GPS, compass) are community contributions – feel free to use them.</span>
    <span class="sentence">Additional credit: <strong>Atharva Phadnis</strong> for the Inspire Award build integration and documentation.</span>
    
    <hr>
    
    <h2>⭐ Star This Repo – Support a 13‑Year‑Old Maker's Inspire Award Journey ⭐</h2>
    <span class="sentence"><strong>This entire repository represents my first Inspire Award project as a 13‑year‑old student.</strong></span>
    <span class="sentence">If you find value in the PWM protocol, calibration tools, or Pratik Phadte's amazing resources, <strong>please hit the ⭐ STAR button</strong> at the top of this page.</span>
    <span class="sentence">Your star will help me gain confidence, motivate me to keep learning, and make this project visible to other young innovators.</span>
    <span class="sentence">Thank you for respecting the work of Pratik Phadte and for supporting a teenager’s dream!</span>
    
    <div class="footer-note">
        <div class="star-badge" style="margin: 0 auto 1rem auto;">
            <span class="badge-icon">⭐</span> PLEASE STAR THIS REPO – SUPPORT A YOUNG MAKER
        </div>
        <span class="sentence" style="margin-bottom: 0.2rem;">🙌 Built by <strong>Atharva Phadnis (age 13)</strong> with respect for Pratik Phadte's contributions 🙌</span>
        <span class="sentence">Any 6‑channel PWM TX/RX | Add barometer, GPS, compass | Inspire Award 2026 – first project!</span>
    </div>
</div>
</body>
</html>
