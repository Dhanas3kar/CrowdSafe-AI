# 🧠 CrowdSafe AI – The Smart Event Safety Platform

> 🎯 _AI-powered real-time crowd monitoring and panic detection system for large-scale public events._

---

## 🚀 Overview

**CrowdSafe AI** transforms ordinary CCTV infrastructure into an **intelligent command center** capable of detecting:
- Overcrowding and threshold breaches  
- Panic runs, surges, aggression, and abnormal activity  
- Smoke or fire hazards  
- Crowd flow directions (real-time movement tracking)  

💡 Designed for **festivals, rallies, concerts, and stadiums**, CrowdSafe AI uses Deep Learning + Optical Flow + Explainable AI to **predict and prevent disasters before they occur.**

---

## 🧩 Features

| Feature | Description |
|----------|-------------|
| 🧍 **Headcount Detection** | Detects and counts people zone-wise using YOLOv8. |
| ⚠️ **Abnormal Activity Detection** | Identifies panic runs, surges, smoke/fire, and aggression. |
| 🧭 **Crowd Flow Tracking** | Calculates direction and intensity of movement using Optical Flow. |
| 🔔 **Instant Alerts** | Triggers alerts on dashboard & notifies organizers in real-time. |
| 🤖 **Explainable AI (XAI)** | Displays clear reasons behind each alert (e.g., “Zone 2: Panic run detected”). |
| 🧠 **Scalable & Modular** | Works with existing CCTV infrastructure — no extra hardware needed. |

---

## 🧠 System Architecture

📹 CCTV Feeds (4)
↓
🧮 AI Models (YOLOv8 + Optical Flow + Anomaly Detection)
↓
⚙️ Decision Engine (Thresholds + Explainable Alerts)
↓
🖥️ Dashboard (React + Firebase)
↓
📲 Organizers & Volunteers (Notifications)


![Architecture Diagram](assets/architecture.png)  
*(Insert your architecture flowchart image here)*

---

## ⚙️ Technical Implementation

### 🏗️ 1. Input Layer
- 4 CCTV / video streams (simulated for demo).  
- Each feed divided into **intelligent zones (Z1–Z4)**.  

### 🧠 2. AI Processing Layer
- **YOLOv8** → Person detection & headcount per zone.  
- **Optical Flow (RAFT or OpenCV)** → Panic & flow direction.  
- **Smoke/Fire Classifier** → Detect environmental hazards.  
- **Pose Estimation (Optional)** → Detect aggression/fights.  

### ⚡ 3. Alert Engine
- Compares real-time headcount vs zone threshold.  
- Detects abnormal motion → triggers alerts.  
- Generates **Explainable AI** messages with reasons.  

### 🖥️ 4. Dashboard & Notification Layer
- React.js + Firebase real-time dashboard.  
- FastAPI backend for AI inference.  
- Push notifications to volunteers’ phones.  

### ☁️ 5. Deployment Layer
- Dockerized for scalability.  
- Runs on GPU / Cloud (AWS or GCP).  

---

## 🧰 Tech Stack

| Layer | Technologies |
|--------|---------------|
| **Detection & Tracking** | YOLOv8, OpenCV, RAFT (Optical Flow), PyTorch |
| **Backend** | Python, FastAPI |
| **Frontend** | React.js, Firebase |
| **Explainability** | SHAP / LIME |
| **Deployment** | Docker, AWS / GCP |

---

## 🧪 Demo Simulation

For hackathon demo, we used **4 pre-recorded CCTV videos** simulating a crowded event:
- Zone-wise crowd monitoring  
- Panic motion (people running → alert trigger)  
- Fire/smoke event detection  
- Volunteer notification simulation  

### 🎥 Example Workflow:
1️⃣ CCTV → YOLO counts people  
2️⃣ Optical Flow → Detects fast, collective motion  
3️⃣ Alert → “⚠️ Zone 3: Panic Run Detected”  
4️⃣ Firebase → Notifies organizers instantly  

---

## 📊 Results (Hackathon Demo Goals)

| Metric | Description |
|---------|-------------|
| 👥 Headcount Accuracy | ~94% with YOLOv8 |
| ⚠ Panic Detection | Real-time optical flow threshold |
| 📡 Alert Latency | < 1.2 seconds |
| 💬 Explainability | Each alert justified with cause |

---

## 🧭 Future Scope

- 🚁 **Drone Integration** for aerial crowd view.  
- 🎙️ **Multilingual Voice Assistant** (Tamil, Hindi, English).  
- 🧮 **Predictive Analytics** for crowd surge forecasting.  
- 🛰️ **Smart City Integration** with emergency systems.  

---

## 🧑‍💻 Contributors

| Name | Role | Email |
|------|------|-------|
| **Dhanasekar M** | ---- | dhanasekarmurgesan@gmail.com |
| **Sowndarya M** | ---- | sowndaryamanick@gmail.com |
| ** --- ** | ---- | ---- |
| **Dharun Prasath M** | ---- | dharunprasath.murugan@gmail.com |


---

## 📚 References
- [RAFT: Recurrent All-Pairs Field Transforms (ECCV 2020)](https://arxiv.org/abs/2003.12039)
- [YOLOv8 Documentation (Ultralytics)](https://docs.ultralytics.com)
- [OpenCV Optical Flow Guide](https://docs.opencv.org/)

---

## 🪄 How to Run Locally

```bash
# Clone the repository
git clone https://github.com/<your-username>/CrowdSafe-AI.git
cd CrowdSafe-AI

# Install dependencies
pip install -r requirements.txt

# Run the backend
python app.py

# For dashboard (React)
cd dashboard
npm install
npm run dev


