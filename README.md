# 🛡️ ESP32-Based IoT Honeypot with Attack Detection

## 📌 About the Project

An ESP32-based IoT Honeypot designed to simulate a vulnerable IoT environment and detect suspicious network activities.

The project creates a fake IoT web interface with user and administrator login pages, device configuration pages, and simulated network services. It monitors incoming connections, detects potential SQL injection attempts, tracks failed login attempts, and blocks suspicious IP addresses.

It also integrates with Blynk Cloud to send real-time security alerts when suspicious activities or unauthorized access attempts are detected.

The main objective is to understand IoT security threats, monitor attacker behavior, and demonstrate basic intrusion detection and prevention techniques using an ESP32.

## 🚀 Features

### 1. Fake IoT Web Interface
- Simulated IoT dashboard.
- Fake device status monitoring.
- User login and administrator login.
- IoT configuration page.
- Dark-themed HTML/CSS interface.

### 2. SQL Injection Detection
- Detects common SQL injection patterns.
- Monitors suspicious login inputs.
- Identifies potential credential injection attempts.
- Automatically blocks detected attacking IP addresses.

### 3. Login Security
- Tracks failed login attempts.
- Automatically blocks IP addresses after 5 failed attempts.
- Administrator authentication with 6-digit OTP.
- Limits OTP verification to 3 attempts.

### 4. IP Blocking System
- Permanently blocks detected IP addresses within the application.
- Stores blocked IP addresses using ESP32 SPIFFS.
- Restores blocked IP addresses after device reboot.

### 5. Fake Network Services
Simulates additional network services to monitor incoming connections:

| Port | Service | Purpose |
|---|---|---|
| 80 | HTTP | Fake IoT Web Interface |
| 8080 | HTTP | Alternative Web Server |
| 21 | FTP | Fake FTP Service |
| 22 | SSH | Fake SSH Banner |
| 1883 | MQTT | Fake MQTT Service |

### 6. Blynk Cloud Integration
- Sends real-time security alerts.
- Reports suspicious login attempts.
- Notifies when an IP address is blocked.
- Reports FTP, SSH, and MQTT connections.
- Provides administrator authentication alerts.

### 7. Additional Security Features
- Fake Wi-Fi Access Point.
- Serial Monitor logging.
- Temporary HTTP port shutdown for 5 minutes after triggering a block.
- Attacker monitoring page.
- OTP generation and verification.

## 🛠️ Technologies Used

- ESP32
- Arduino IDE
- Embedded C++
- Wi-Fi Networking
- HTTP Protocol
- FTP / SSH / MQTT Service Simulation
- SPIFFS
- Blynk IoT Cloud
- HTML & CSS

## ⚙️ System Workflow

1. ESP32 connects to the configured Wi-Fi network.
2. Creates a fake Wi-Fi access point.
3. Starts the fake IoT web interface.
4. Monitors incoming user and administrator login requests.
5. Checks input for suspicious SQL injection patterns.
6. Tracks failed login and OTP attempts.
7. Blocks suspicious IP addresses.
8. Saves blocked IP addresses in SPIFFS.
9. Sends security alerts through Blynk Cloud.
10. Monitors connections to simulated FTP, SSH, and MQTT services.

## 📂 Project Structure

```text
ESP32-IoT-Honeypot/
│
├── IoT_Honeypot.ino
└── README.md
```

## 🔌 Hardware Requirements

- ESP32 Development Board
- USB Cable
- Wi-Fi Network
- Computer with Arduino IDE

## 📦 Software Requirements

- Arduino IDE
- ESP32 Board Package
- Blynk IoT Library
- ESP32 Wi-Fi Library
- WebServer Library
- SPIFFS Library

## ▶️ Setup Instructions

**1. Clone the repository**

```bash
git clone https://github.com/Akash-iot/IOT-HONEYPOT.git
```

**2. Open the project**

Open the `.ino` file using Arduino IDE.

**3. Configure Wi-Fi credentials**

Update your Wi-Fi SSID and password in the source code.

**4. Configure Blynk Cloud**

Add your Blynk Template ID, Template Name, and Authentication Token.

**5. Select ESP32 Board**

Choose the appropriate ESP32 board and COM port.

**6. Upload the code**

Upload the sketch to your ESP32 board.

**7. Monitor activity**

Open the Serial Monitor at 115200 baud to observe connection logs and security alerts.

## 🎯 Learning Objectives

- Understanding IoT security vulnerabilities.
- Learning embedded network programming.
- Understanding honeypot architecture.
- Detecting common SQL injection patterns.
- Implementing basic IP-based blocking.
- Understanding authentication and OTP verification.
- Monitoring network services.
- Integrating IoT devices with cloud-based alert systems.

## ⚠️ Security Disclaimer

This project is developed for educational and cybersecurity research purposes.

- Use only in authorized testing environments.
- This is an application-level honeypot, not a network-level firewall.
- SQL injection detection uses basic pattern matching and may produce false positives.
- Do not use hardcoded credentials or expose sensitive tokens in public repositories.
- Fake service banners do not implement complete FTP, SSH, or MQTT protocols.

## 👨‍💻 Author

**M AKASH**

Cybersecurity Enthusiast | Junior Penetration Tester | IoT Security Researcher

GitHub: Akash-iot
