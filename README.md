<div align="center">

#  Team-Sentinels

### Jeevan Rakshak

*Every Beat Counts. A Safer Tomorrow. *

[![LIVE DEMO](https://img.shields.io/badge/🌐_-DOCS-blue?style=for-the-badge)](https://lanezy-frontend.vercel.app/)
[![DOCUMENTATIONS   ](https://img.shields.io/badge/🌐_LIVE-DEMO-blue?style=for-the-badge)](https://qr-codes.io/Xmmmmf)
---

</div>

## Project Overview

The **Jeevan Rakshak** wearable health and safety device built for people who face real risk from India's climate and disaster conditions eg outdoor workers, elderly residents, disaster-response teams, and anyone in areas where heat waves, floods, or unreliable connectivity are a fact of life. Rather than just showing a heart-rate number, it watches how physiological and environmental signals move together and flags the moment they start looking dangerous.

<br>

## Key Features

**Multi-parameter health monitoring** - Heart rate and body temperature tracked continuously not just isolated readings, but trends over time.

**Environmental context sensing** - Ambient temperature and humidity combined with body signals.

**Fall & inactivity detection** - accelerometer/gyroscope detects sudden impact, then checks for follow-up stillness.

**GPS-based emergency location** - Location is attached to any critical event so responders know where to go.

**Power efficient operation** - Low-power modes and optimized sampling on a rechargeable Li-Po battery, since the device is meant to run continuously.

<br>

---

## System Architecture






```






````

<br>

---
### 1.

## Hardware Components

| Component | Purpose |
|---|---|
| ESP32-S3 | Main controller + on-device (edge) AI |
| MAX30102 | Heart rate + SpO₂ |
| MAX30205 | Body temperature |
| BME280 | Ambient temperature + humidity |
| MPU6050 | Motion, fall & inactivity detection |
| GPS module | Location + emergency location support |
| OLED display | Status & alert readout |
| Buzzer | Audible alerts |
| Vibration motor | Silent/tactile alerts |
| SOS button | Manual emergency trigger |
| Li-Po battery | Portable power |
| Enclosure | Wearable protection |

**Safety Features:**
- No manual intervention required
- Heading-based intelligent lane detection
- Distance verification prevents premature activation
- Complete event logging for oversight

<br>

## How It Works

1. **Sense** — sensors continuously collect heart rate, SpO₂, temperature, humidity, and motion data
2. **Process** — the ESP32-S3 receives and filters sensor readings
3. **Analyze** — the on-device AI examines current values, trends over time, and combinations of parameters
4. **Decide** — the system classifies the state as `NORMAL`, `WARNING`, or `CRITICAL`
5. **Alert** — the OLED, buzzer, and vibration motor notify the wearer immediately
6. **Respond** — for critical conditions, the SOS mechanism and GPS location support emergency response

## Why On-Device AI

| Principle | Benefit |
|---|---|
| **Privacy** | Raw health data doesn't need to continuously leave the device |
| **Offline operation** | The core warning system works without internet connectivity |
| **Low latency** | No waiting on a remote server before generating a warning |
| **Disaster resilience** | Designed for conditions where connectivity is unreliable |


## Tech Stack

- **Firmware:** ESP32-S3 (Arduino / ESP-IDF)
- **Sensors:** MAX30102, MAX30205, BME280, MPU6050, GPS module
- **Companion App:** cloud-based fleet dashboard for real-time monitoring
- **Communication:** BLE / Wi-Fi for classified-status sync only

## Repository Structure

```
jeevan-rakshak/
├── firmware/        # ESP32-S3 source code
├── hardware/        # schematics & wiring diagrams
├── docs/            # documentation, diagrams, datasheets
├── dashboard/       # cloud companion app
└── README.md
```


<br>

---

## Technology Stack

### Frontend
```
React.js / Next.js • Tailwind CSS • Leaflet.js / Mapbox GL • Socket.io
```

### Backend
```
Node.js / Python FastAPI • RESTful + WebSocket • JWT + OAuth 2.0 • Redis + Bull
```

<br>


### Installation

#### 1️⃣ Clone Repository

```bash
# Clone the repository
git clone https://github.com/<your-username>/jeevan-rakshak.git
cd jeevan-rakshak

#### 2️⃣ Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
python manage.py migrate
python main.py
```

#### 3️⃣ Frontend Setup

```bash
cd frontend
npm install
cp .env.example .env.local
npm run dev
```
---

## System Strengths

### Technical Excellence
- **Hybrid Architecture** - Seamless AI, IoT, and geospatial integration
- **Real-time Processing** - Sub-second latency for critical operations
- **Scalable Design** - Microservices-ready for city-wide deployment
- **Hardware Light** - Minimal infrastructure requirements

### Operational Benefits
- **Deterministic Control** - Predictable and fair traffic management
- **Automated Enforcement** - Reduces manual workload
- **Emergency Response** - Life-saving automatic override
- **High Accuracy** - >95% AI detection accuracy

### Citizen-Centric
- **Public Transparency** - Open access to data and heatmaps
- **Direct Participation** - Citizen reporting channels
- **Instant Assistance** - Sub-minute tow response
- **Accountability** - Full audit trails

### Safety & Compliance
- **Proactive Prevention** - Physical barriers stop violations
- **Evidence-Based** - Automated violation capture
- **Officer Oversight** - Human verification loop
- **Audit Trails** - Complete legal compliance

<br>
## Demo

A working prototype of the cloud-side dashboard is live, simulating a fleet of wearables reporting classified status, vitals, and location in real time.
---
## Team

*(Add team name and member names here.)*


## 🙏 Acknowledgments

Built for **Smart India Hackathon** under Problem Statement **SIH26181** — Smart Health, Disaster Management & Resilience.


<br>
