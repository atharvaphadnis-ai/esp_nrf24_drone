<!DOCTYPE html>
<html>
<head>
    <title>Inspire Award Build - README</title>
    <style>
        /* Optional: clean background and font for readability */
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            line-height: 1.5;
            max-width: 900px;
            margin: 2rem auto;
            padding: 0 20px;
            background: #fefefe;
            color: #111;
        }
        /* Spacing between sentences is handled by <br><br> tags,
           but we also add a little extra care for headings */
        h1, h2, h3 {
            margin-top: 1.8em;
            margin-bottom: 0.5em;
            border-bottom: 1px solid #eaecef;
            padding-bottom: 0.3em;
        }
        code {
            background: #f6f8fa;
            padding: 0.2em 0.4em;
            border-radius: 3px;
            font-size: 85%;
        }
        .star-badge {
            background: #ffd700;
            display: inline-block;
            padding: 0.2em 0.6em;
            border-radius: 20px;
            font-weight: bold;
            font-size: 0.9rem;
        }
        hr {
            margin: 2em 0;
        }
    </style>
</head>
<body>

<!-- 
    This README uses explicit HTML line breaks (<br><br>) between every sentence 
    to ensure maximum visual spacing and neatness, as requested.
    All credits to Pratik Phadte, and full compatibility for any 6-channel PWM TX/RX.
    Optional sensors: barometer, GPS, compass.
    Built for the Inspire Award project – please star the repo!
-->

<h1>✨ Inspire Award Build – PWM Flight Controller ✨</h1>

<br>

<strong>🔹 Based on Pratik Phadte's resources & Instructables PWM protocol 🔹</strong><br><br>

This repository contains all the code, calibration routines, and wiring guidance for a robust PWM‑based control system.<br><br>
It uses <strong>Pratik Phadte's calibration</strong> routine to get precise stick ranges and servo outputs.<br><br>
The <strong>light controller code</strong> from Pratik Phadte is included – perfect for LED indicators or visual feedback.<br><br>
Transmitter and receiver implementation follows the <strong>PWM protocol</strong> originally shared on Instructables.<br><br>
You can use <strong>any 6‑channel transmitter and receiver</strong> as long as they output standard PWM signals (1–2 ms pulse width).<br><br>
Make sure to <strong>give full credit to Pratik Phadte</strong> for the foundational work on calibration, light controller, and PWM communication.<br><br>
Optionally, you can <strong>add a barometer, GPS module, and compass</strong> to expand functionality (altitude hold, navigation, heading).<br><br>
This repository is <strong>dedicated to my Inspire Award build</strong> – a project that showcases innovation in remote‑controlled systems.<br><br>
If this helps you with your own science or engineering project, <strong>please ⭐ star this repository ⭐</strong> to support further development and updates.<br><br>

<hr>

<h2>📌 Key Features & Components</h2>

<br>

✅ <strong>Calibration routine</strong> – based directly on Pratik Phadte's method, ensures accurate PWM mapping.<br><br>
✅ <strong>Light controller code</strong> – drives LEDs, status lights, or visual alerts using PWM outputs.<br><br>
✅ <strong>PWM protocol implementation</strong> – reliable communication between any 6‑channel PWM receiver and your microcontroller.<br><br>
✅ <strong>Universal TX/RX compatibility</strong> – works with FlySky, Radiolink, FrSky, or any 6‑channel set that outputs PWM.<br><br>
✅ <strong>Optional sensor expansion</strong> – barometer (altitude), GPS (position/waypoints), compass (magnetometer for yaw).<br><br>

<hr>

<h2>🧰 Pratik Phadte Resources – Credits & Acknowledgment</h2>

<br>

This project would not be possible without the open work shared by <strong>Pratik Phadte</strong> on Instructables.<br><br>
The <strong>calibration logic, light controller code, and transmitter/receiver PWM protocol</strong> are adapted from his excellent tutorials.<br><br>
Please <strong>respect the original license</strong> and always provide attribution when reusing or redistributing these components.<br><br>
You can find the original Instructables articles by searching "Pratik Phadte PWM protocol" or "Pratik Phadte light controller".<br><br>
🙏 <strong>Big thanks to Pratik Phadte</strong> for making RC and drone development accessible to everyone!<br><br>

<hr>

<h2>🕹️ Transmitter & Receiver – PWM Requirements</h2>

<br>

Any <strong>6‑channel (or more) transmitter and receiver</strong> can be used as long as the receiver outputs <strong>individual PWM signals</strong> on each channel.<br><br>
Typical examples: FlySky FS‑i6 with FS‑iA6B receiver, Radiolink AT9S, or any standard RC system in PWM mode.<br><br>
Do <strong>not</strong> use SBUS, PPM, or other serial protocols unless you convert them to PWM – this code strictly expects separate PWM input pins.<br><br>
Connect the receiver's PWM outputs (CH1 to CH6) directly to the microcontroller's digital input pins (with appropriate voltage levels).<br><br>
Then run the <strong>calibration sketch</strong> to map your transmitter's stick movements to the full PWM range.<br><br>

<hr>

<h2>🧭 Optional Enhancements: Barometer, GPS, Compass</h2>

<br>

You are free to <strong>add extra sensors</strong> to make your Inspire Award build even more advanced.<br><br>
✨ <strong>Barometer</strong> (e.g., BMP280, MS5611) – provides altitude hold, telemetry, and stable height control.<br><br>
✨ <strong>GPS module</strong> (e.g., NEO‑6M, NEO‑M8N) – enables position tracking, return‑to‑home, and waypoint navigation.<br><br>
✨ <strong>Compass / magnetometer</strong> (e.g., HMC5883L, QMC5883L) – gives absolute heading (yaw) reference for autonomous flight.<br><br>
These sensors can be integrated via I2C or UART, and the codebase includes examples for reading them alongside PWM inputs.<br><br>

<hr>

<h2>🚀 Quick Start – Getting the Code Running</h2>

<br>

1️⃣ <strong>Clone this repository</strong> to your local machine or download the ZIP.<br><br>
2️⃣ <strong>Upload the calibration sketch</strong> first – follow Pratik Phadte's instructions to map your transmitter endpoints.<br><br>
3️⃣ <strong>Connect your 6‑channel PWM receiver</strong> to the defined pins (check the wiring diagram in /docs).<br><br>
4️⃣ <strong>Load the main controller code</strong> which includes the light controller and PWM protocol logic.<br><br>
5️⃣ <strong>Test each channel</strong> – throttle, aileron, elevator, rudder, and aux channels should respond smoothly.<br><br>
6️⃣ <strong>If you have a barometer/GPS/compass</strong>, uncomment the respective sections in the code and wire them correctly.<br><br>
7️⃣ <strong>Give proper credit to Pratik Phadte</strong> in any public showcase or derivative work.<br><br>
8️⃣ Finally, <strong>⭐ star this repository ⭐</strong> to show appreciation and help other makers find it!<br><br>

<hr>

<h2>📜 License & Attribution Requirement</h2>

<br>

This repository is provided for educational and non‑commercial Inspire Award projects.<br><br>
<strong>You must credit Pratik Phadte</strong> for the original calibration, light controller code, and PWM protocol from Instructables.<br><br>
If you modify or redistribute this code, keep the credits intact and link back to the original sources.<br><br>
The optional sensor integrations (barometer, GPS, compass) are community contributions – feel free to use them.<br><br>

<hr>

<h2>⭐ Star This Repo – Support the Inspire Award Build ⭐</h2>

<br>

<strong>This entire repository exists to help students, hobbyists, and innovators build their Inspire Award projects.</strong><br><br>
If you find value in the PWM protocol, calibration tools, or Pratik Phadte's amazing resources, <strong>please hit the ⭐ STAR button</strong> at the top of this page.<br><br>
Your star makes the project more visible and encourages further documentation, bug fixes, and new features.<br><br>
Thank you for respecting the work of Pratik Phadte and for supporting open‑source RC development!<br><br>

<hr>

<p style="font-size: 0.9rem; text-align: center; margin-top: 2rem;">
    <strong>🙌 Built with respect for Pratik Phadte's contributions 🙌</strong><br>
    Any 6‑channel PWM TX/RX | Add barometer, GPS, compass | Inspire Award ready<br>
    <span class="star-badge">⭐ PLEASE STAR THIS REPO ⭐</span>
</p>

</body>
</html>
