# Deep Packet Inspection (DPI) Platform

A full-stack **Deep Packet Inspection (DPI)** web application built with **Python, Django REST Framework, React, HTML, CSS, and JavaScript**. The platform captures live network traffic, analyzes packets in real time, detects suspicious activities, and visualizes network statistics through an interactive dashboard.

> **Note:** This project is built for educational purposes to demonstrate networking, cybersecurity, REST APIs, and full-stack development concepts.

---

## Features

### Live Packet Capture
- Capture live packets from a selected network interface
- Real-time packet processing
- Start/Stop packet capture
- Support for multiple network protocols

### Packet Analysis
- Extract source and destination IP addresses
- Display source and destination ports
- Detect transport and application layer protocols
- Packet length analysis
- TCP flags inspection
- TTL analysis
- Timestamp recording

### Supported Protocols
- Ethernet
- IPv4
- IPv6
- TCP
- UDP
- ICMP
- ARP
- DNS
- HTTP
- HTTPS (metadata only)
- DHCP

### Dashboard
- Live packet monitoring
- Interactive charts
- Protocol distribution
- Traffic timeline
- Top source IPs
- Top destination IPs
- Packet statistics
- Active alerts

### Packet Search & Filtering
- Filter by protocol
- Filter by IP address
- Filter by ports
- Search packets
- Sort packets
- View packet details

### Threat Detection
- Port Scan Detection
- SYN Flood Detection
- ICMP Flood Detection
- Suspicious Port Monitoring
- Traffic Spike Detection
- Custom Alert Rules

### REST API
- Packet APIs
- Statistics APIs
- Alert APIs
- Capture Control APIs
- Filtering APIs

---

# Tech Stack

## Frontend

- React
- HTML5
- CSS3
- JavaScript (ES6+)
- React Router
- Axios
- Chart.js / Recharts

## Backend

- Python
- Django
- Django REST Framework
- SQLite (Development)
- PostgreSQL (Production)

## Networking

- Scapy
- PyShark (Optional)
- Socket Programming

---

# Project Structure

```
dpi-platform/

├── frontend/
│
│   ├── public/
│   ├── src/
│   │
│   ├── assets/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── hooks/
│   ├── styles/
│   │
│   ├── App.jsx
│   ├── main.jsx
│   │
│   └── package.json
│
├── backend/
│
│   ├── dpi/
│   ├── packets/
│   ├── alerts/
│   ├── statistics/
│   ├── requirements.txt
│   └── manage.py
│
├── screenshots/
│
└── README.md
```

---

# Architecture

```
                Network Interface
                        │
                        ▼
                Packet Capture (Scapy)
                        │
                        ▼
                Packet Parser
                        │
                        ▼
               Packet Analyzer
                        │
                        ▼
             Threat Detection Engine
                        │
                        ▼
                 Django REST API
                        │
                        ▼
                 React Dashboard
```

---

# Dashboard Overview

The dashboard provides:

- Live packet monitoring
- Protocol statistics
- Network traffic visualization
- Active alerts
- Recent packets
- Packet inspection window

---

# API Endpoints

## Packet APIs

```
GET     /api/packets/
GET     /api/packets/<id>/
```

## Statistics APIs

```
GET     /api/statistics/
GET     /api/protocols/
```

## Alerts APIs

```
GET     /api/alerts/
```

## Capture APIs

```
POST    /api/capture/start/
POST    /api/capture/stop/
```

---

# Database Schema

## Packet

| Field | Description |
|--------|-------------|
| id | Primary Key |
| timestamp | Capture Time |
| source_ip | Source IP |
| destination_ip | Destination IP |
| protocol | Protocol |
| source_port | Source Port |
| destination_port | Destination Port |
| packet_length | Packet Size |
| ttl | Time To Live |
| flags | TCP Flags |
| payload | Packet Payload |
| suspicious | Boolean |

---

## Alert

| Field | Description |
|--------|-------------|
| id | Primary Key |
| packet | Related Packet |
| severity | Low/Medium/High |
| type | Alert Type |
| description | Alert Details |
| created_at | Timestamp |

---

# Future Improvements

- WebSocket live updates
- Authentication & Authorization
- User Management
- Packet Export (CSV/PCAP)
- GeoIP Visualization
- Machine Learning Based Anomaly Detection
- Role-Based Access Control (RBAC)
- Dark/Light Theme
- Docker Deployment
- Kubernetes Deployment
- CI/CD Pipeline

---

# Learning Objectives

This project demonstrates practical implementation of:

- Computer Networks
- Packet Sniffing
- Deep Packet Inspection
- Python Programming
- Django REST Framework
- React Development
- REST APIs
- Database Design
- Full-Stack Development
- Cybersecurity Fundamentals

---

# Disclaimer

This project is intended **only for educational and research purposes**. Packet capture should only be performed on networks you own or have explicit authorization to monitor. Users are responsible for complying with applicable laws, organizational policies, and ethical guidelines.

---

# Author

**Devesh Krishnani**

Full Stack Python Developer | Web Developer | Cybersecurity Enthusiast

---

## License

This project is licensed under the MIT License.
