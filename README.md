# 🛡️ Python-Based Network Honeypot

## 📌 About the Project

A simple Python-based network honeypot developed using socket programming to monitor and analyze incoming TCP connections.

The honeypot listens on HTTP port 80 and detects incoming visitors by capturing their IP addresses. When a client connects, it sends a fake HTML response and collects incoming network data for basic monitoring and security analysis.

This project demonstrates how honeypots can be used as a defensive security mechanism to observe suspicious network activity and understand potential attacker interactions.

## 🚀 Features

- **TCP Connection Monitoring:** Listens for incoming TCP connections.
- **IP Address Tracking:** Captures the IP address of connected visitors.
- **Fake HTTP Response:** Sends a simulated HTML response to connected clients.
- **Network Data Collection:** Receives and displays incoming client data.
- **Real-Time Monitoring:** Displays connection information in the terminal.

## 🛠️ Technologies Used

- Python 3
- Socket Programming
- TCP/IP Networking
- HTTP Protocol
- Kali Linux / Linux

## ⚙️ How It Works

1. Creates a TCP socket using Python.
2. Binds the socket to a specified IP address and port 80.
3. Listens for incoming connections.
4. Captures the visitor's IP address.
5. Sends a fake HTML response.
6. Receives and displays client request data.

## 📂 Project Structure

```text
Python-Network-Honeypot/
│
├── honeypot.py
└── README.md
```

## ▶️ Installation & Usage

**1. Clone the repository**

```bash
git clone <your-repository-url>
```

**2. Navigate to the project directory**

```bash
cd Python-Network-Honeypot
```

**3. Run the Python script**

```bash
sudo python3 honeypot.py
```

**Note:** Update the IP address in the script according to your machine's network interface. Port 80 generally requires administrator/root privileges.

## 🎯 Learning Objectives

- Understanding Python socket programming.
- Learning TCP client-server communication.
- Understanding basic honeypot architecture.
- Monitoring incoming network connections.
- Learning basic network security concepts.

## ⚠️ Disclaimer

This project is developed for educational and cybersecurity research purposes only. Use it only in authorized lab environments and networks.

## 👨‍💻 Author

**Akash M**

Cybersecurity Enthusiast | Junior Penetration Tester | CTF Player
