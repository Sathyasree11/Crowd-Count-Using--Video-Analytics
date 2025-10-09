# Crowd-Count-Using--Video-Analytics
# Crowd Counting Portal – Smart Real-Time People Analytics

> A fully interactive **Crowd Counting & Zone Management Web Portal** built for **real-time monitoring**, **heatmap visualization**, and **automated alerts** using live video or uploaded footage.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-Framework-black.svg)
![TensorFlow.js](https://img.shields.io/badge/TensorFlow.js-AI%20Detection-orange.svg)
![Chart.js](https://img.shields.io/badge/Chart.js-Visualization-red.svg)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue.svg)
![Infosys Internship](https://img.shields.io/badge/Infosys-Internship-0080FF.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 🌟 Overview

The **Crowd Counting Portal** is an AI-powered Flask web application designed to monitor people density in real-time using **video streams or uploads**.  
It provides zone-based analytics, heatmaps, and alerts to ensure better **safety, crowd management, and decision-making**.  

This project integrates **TensorFlow.js**, **Flask**, **MySQL**, and **Chart.js** into a single dynamic dashboard — making it an ideal AI + Web hybrid solution.

---

## 🚀 Key Features

### 🎥 Live Crowd Detection
- Real-time people detection using **TensorFlow.js (COCO-SSD)**.  
- Works with both **webcam** and **uploaded video** inputs.

### 🧩 Smart Zone Management
- Draw and label **custom zones** over video feed.  
- Zone data is stored and retrieved from **MySQL (JSON format)**.

### 📊 Real-Time Analytics Dashboard
- Displays **line and bar charts** using Chart.js.  
- Zone-wise count tracking, historical data logs, and trend analysis.

### ⚠️ Alert System
- Automatic alerts when density exceeds threshold.  
- Color-coded (🟢 Safe, 🟡 Moderate, 🔴 Danger) zones for instant awareness.

### 🔐 User Authentication
- Flask-based login & registration system.  
- Each user’s uploads, zones, and analytics are private and secure.

### 💎 Responsive UI Design
- Built using **HTML5, CSS3, and Vanilla JS**.  
- Lightweight, fast, and responsive across devices.

---

## 🗂️ Project Structure

```bash
CrowdCountingPortal/
│
├── app.py                # Flask backend (uploads, zones, alerts, DB)
│
├── templates/            # HTML templates
│   ├── index.html        # Main dashboard with video + zones
│   ├── graphs.html       # Real-time analytics dashboard
│   ├── alerts.html       # Threshold alert visualization
│   ├── login.html        # User login
│   ├── register.html     # User registration
│   └── my_uploads.html   # Manage uploaded videos
│
├── static/
│   ├── app.js            # Frontend logic (drawing, counting, heatmap)
│   └── style.css         # Responsive modern styles
│
├── uploads/              # User-uploaded video files
├── counts_log.csv        # Automatic crowd data log
├── zones.json            # Saved zone coordinates
└── README.md             # Project documentation

💻 Technology Stack

| Component         | Technology                        |
| ----------------- | --------------------------------- |
| **Frontend**      | HTML5, CSS3, JavaScript, Chart.js |
| **AI Detection**  | TensorFlow.js + COCO-SSD          |
| **Backend**       | Flask (Python)                    |
| **Database**      | MySQL (PyMySQL)                   |
| **Data Logging**  | CSV + MySQL                       |
| **Visualization** | Chart.js (Line, Bar)              |

⚙️ How It Works

Login/Register – Secure authentication with Flask sessions.

Upload or Stream Video – Choose a live webcam feed or local file.

Draw Zones – Define specific areas for crowd detection.

Start Detection – AI model counts people in each zone.

View Dashboard – Live population trends & alerts update in real-time.

Export Data – Save data as CSV for reports or analysis.

.

🧠 System Architecture
Video Input (Webcam/Upload)
        ↓
Object Detection (TensorFlow.js)
        ↓
Zone Mapping → Count Calculation
        ↓
Flask Backend → MySQL + CSV Logging
        ↓
Visualization → Chart.js + Alerts

🗄️ Database Schema Overview
1. users
id	username	password	email	created_at
2. videos

| id | user_id | filename | size_bytes | created_at |

3. video_zones

| id | video_id | zone_id | label | coordinates |

4. zone_counts

| id | video_id | zone_id | ts | label | current | peak |

⚙️ Installation & Setup
🛠️ Prerequisites

Python 3.8 or higher

MySQL Server

Node.js (optional for frontend editing)

💾 Setup Guide
# 1️⃣ Clone the repository
git clone https://github.com/yourusername/CrowdCountingPortal.git
cd CrowdCountingPortal

# 2️⃣ Create and activate virtual environment
python -m venv venv
venv\Scripts\activate      # (Windows)
source venv/bin/activate   # (Mac/Linux)

# 3️⃣ Install dependencies
pip install flask pymysql

# 4️⃣ Configure database
# - Create a database in MySQL (e.g., crowd_portal)
# - Update DB_CONFIG in app.py with your credentials

# 5️⃣ Run the application
python app.py

# 6️⃣ Open your browser
http://127.0.0.1:5000/

