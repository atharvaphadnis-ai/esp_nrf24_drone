<!DOCTYPE html>
<html>
<body style="font-family: Arial, sans-serif; line-height: 1.8; color: #333; padding: 20px;">

    <h1 style="color: #2c3e50; text-align: center;">IN-DEPTH TECHNICAL DOCUMENTATION: ESP32 FLIGHT PLATFORM</h1>
    <p style="text-align: center; font-style: italic;">A Professional-Grade DIY Multi-Rotor System for the INSPIRE Award</p>

    <br><hr><br>

    <h3 style="color: #e67e22;">1. CORE ARCHITECTURE & LOGIC SOURCE</h3>
    <p>
        The heart of this drone is the <strong>ESP32 DevKit V1</strong>, a dual-core microcontroller running at 240MHz. 
        &nbsp;The flight stabilization logic is based on the <strong>Pratik Phadte</strong> framework, which utilizes the MPU6050 6-axis IMU (Inertial Measurement Unit).
    </p>
    <br>
    <p>
        <strong>Processing Power:</strong> Unlike standard Arduino drones (16MHz), the ESP32 allows us to run the flight control loop at <strong>500Hz to 1kHz</strong>. 
        &nbsp;This means the drone calculates its position and adjusts motor speeds up to 1,000 times every second, resulting in "locked-in" stability.
    </p>

    <br><br>

    <h3 style="color: #e67e22;">2. THE PID CONTROL SYSTEM (THE BRAIN)</h3>
    <p>
        For the INSPIRE judges, the most important part is the <strong>PID (Proportional, Integral, Derivative)</strong> loop. 
        &nbsp;This mathematical algorithm ensures the drone remains level:
    </p>
    <br>
    <ul>
        <li><strong>Proportional (P):</strong> Corrects the current error (if the drone tilts 5 degrees, P pushes it back).</li>
        <br>
        <li><strong>Integral (I):</strong> Corrects errors that build up over time, such as a slight weight imbalance or wind resistance.</li>
        <br>
        <li><strong>Derivative (D):</strong> Predicts future errors by looking at the speed of the tilt, preventing the drone from over-correcting and wobbling.</li>
    </ul>

    <br><br>

    <h3 style="color: #e67e22;">3. SIGNAL PROTOCOL & RECEIVER FLEXIBILITY</h3>
    <p>
        This project implements a versatile <strong>PWM (Pulse Width Modulation)</strong> input system. 
        &nbsp;The receiver code, adapted from <strong>Instructables</strong>, processes incoming signals from the <strong>NRF24L01 PA+LNA</strong> module.
    </p>
    <br>
    <p>
        <strong>Universal Compatibility:</strong> The PCB is designed to be "Radio Agnostic." 
        &nbsp;While we use a custom NRF24L01 transmitter, the hardware can accept signals from any commercial <strong>6-Channel PWM Receiver</strong> (like FlySky or FrSky). 
        &nbsp;Each channel (Roll, Pitch, Yaw, Throttle, Aux1, Aux2) is connected to an interrupt-enabled GPIO on the ESP32 for zero-latency response.
    </p>

    <br><br>

    <h3 style="color: #e67e22;">4. ADVANCED PCB SENSOR EXPANSION</h3>
    <p>
        One of the strongest points for the award is the <strong>PCB's modularity</strong>. It is ready for "Level 2" autonomous flight:
    </p>
    <br>
    <table style="width:100%; border-collapse: collapse;">
        <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong>Magnetometer (HMC5883L)</strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">Uses the I2C Bus (SDA/SCL) to provide North-heading data, essential for long-distance navigation.</td>
        </tr>
        <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong>Barometer (BMP280)</strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">Measures atmospheric pressure to allow "Altitude Hold," letting the drone hover at a fixed height.</td>
        </tr>
        <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong>GPS (Neo-6M)</strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">Connects via UART (TX/RX) to enable autonomous waypoint navigation and fail-safe "Return to Home."</td>
        </tr>
    </table>

    <br><br>

    <h3 style="color: #e67e22;">5. CALIBRATION & FAIL-SAFE PROCEDURES</h3>
    <p>
        <strong>IMU Calibration:</strong> During the first 5 seconds of power-up, the drone samples the MPU6050 data 2,000 times to define its "True Level."
    </p>
    <br>
    <p>
        <strong>Signal Fail-Safe:</strong> If the NRF24L01 loses connection, the ESP32 immediately enters a "Safe Descent" or "Hard Cut" mode. 
        &nbsp;This is a critical safety feature to prevent the drone from flying away or causing injury.
    </p>

    <br><br>

    <h3 style="color: #e67e22;">6. SCIENTIFIC CONTRIBUTION</h3>
    <p>
        By combining the <strong>Pratik Phadte</strong> codebase with custom <strong>NRF24L01</strong> communication, this project proves that high-end flight technology can be built from low-cost, off-the-shelf components. 
        &nbsp;It demonstrates mastery over <strong>I2C communication</strong>, <strong>Interrupt handling</strong>, and <strong>Real-time operating systems (RTOS)</strong>.
    </p>

    <br><br>

</body>
</html>
