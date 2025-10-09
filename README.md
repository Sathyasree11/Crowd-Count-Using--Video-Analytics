# Crowd-Count-Using--Video-Analytics

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


## 💻 Technology Stack

| Component | Technology |
|------------|-------------|
| **Frontend** | HTML5, CSS3, JavaScript, Chart.js |
| **AI Detection** | TensorFlow.js + COCO-SSD |
| **Backend** | Flask (Python) |
| **Database** | MySQL (PyMySQL) |
| **Data Logging** | CSV + MySQL |
| **Visualization** | Chart.js (Line, Bar) |

---

## ⚙️ How It Works

Login/Register – Secure authentication with Flask sessions.

Upload or Stream Video – Choose a live webcam feed or local file.

Draw Zones – Define specific areas for crowd detection.

Start Detection – AI model counts people in each zone.

View Dashboard – Live population trends & alerts update in real-time.

Export Data – Save data as CSV for reports or analysis.

---


## 🧠 System Architecture

Video Input (Webcam/Upload)

        ↓

Object Detection (TensorFlow.js)

        ↓

Zone Mapping → Count Calculation

        ↓

Flask Backend → MySQL + CSV Logging

        ↓

Visualization → Chart.js + Alerts

---



## ⚙️ Installation & Setup
### 🛠️ Prerequisites

Python 3.8 or higher

MySQL Server

Node.js (optional for frontend editing)

### 💾 Setup Guide

##### 1️⃣ Clone the repository
git clone https://github.com/Sathyasree11/Crowd-Count-Using--Video-Analytics

#### 2️⃣ Create and activate virtual environment
python -m venv venv
venv\Scripts\activate      
source venv/bin/activate   

 3️⃣ Install dependencies
pip install flask pymysql

 4️⃣ Configure database
 - Create a database in MySQL (e.g., crowd_portal)
 - Update DB_CONFIG in app.py with your credentials

 5️⃣ Run the application
python app.py

 6️⃣ Open your browser
http://127.0.0.1:5000/


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
---

## 🧾 Output / Results

### 1️⃣ Register Page
> Users can create a new account by entering full details like First Name, Last Name, Email, Contact Number, Date of Birth, Gender, State, and District.

🖼️ **Screenshot:** `register_page.png`  
💡 *Provides secure registration with MySQL integration.*

---

### 2️⃣ Login Page
> Registered users can log in securely using their username and password.

🖼️ **Screenshot:** `login_page.png`  
💡 *Implements Flask session management for authentication.*

---

### 3️⃣ Dashboard Page
> Displays workflow steps and system navigation.

🖼️ **Screenshot:** `dashboard_page.png`  
💡 *Acts as the control center for all features.*

---

### 4️⃣ Drawing Zones
> Allows users to draw custom zones directly on video frames for crowd tracking.

🖼️ **Screenshot:** `draw_zones.png`  
💡 *Each zone can be named and stored in the database.*

---

### 5️⃣ Preview Zones
> Displays previously created zones for review before running detection.

🖼️ **Screenshot:** `preview_zones.png`  
💡 *Ensures users verify zone setup before analytics.*

---

### 6️⃣ Edit Zones
> Modify existing zone coordinates or labels dynamically.

🖼️ **Screenshot:** `edit_zones.png`  
💡 *Provides flexibility for changing monitored areas.*

---

### 7️⃣ Delete Zones
> Remove unwanted zones from the database.

🖼️ **Screenshot:** `delete_zones.png`  
💡 *Keeps workspace clean and manageable.*

---

### 8️⃣ Real-Time Dashboard with Count Updates
> Displays live people counts in each zone using AI detection.

🖼️ **Screenshot:** `realtime_dashboard.png`  
💡 *Counts refresh dynamically as detection runs.*

---

### 📈 Graphs & Analytics

#### 🔹 Line Chart – Zone Counts Over Time
> Visualizes how crowd density changes in each zone dynamically.

🖼️ **Screenshot:** `line_chart.png`  
💡 *Perfect for monitoring time-based population fluctuations.*

---

#### 🔹 Bar Chart – Current Zone-Wise Counts
> Displays the current number of people detected in each zone.

🖼️ **Screenshot:** `bar_chart.png`  
💡 *Helps compare crowd intensity across multiple zones.*

---

### ⚠️ Alert System Triggered
> Automatically alerts users when the crowd in any zone exceeds the predefined threshold.

🖼️ **Screenshot:** `alert_triggered.png`  
💡 *Color-coded alert levels ensure quick visual identification.*

---

### 📤 Data Export (CSV)
> User can export detailed count logs for offline analysis or reporting.

🖼️ **Screenshot:** `export_csv.png`  
💡 *Stored logs include timestamps, zone IDs, and count values.*

---

📍**Summary:**  
The system provides a complete real-time people analytics experience — from secure user authentication and zone management to live detection, visualization, and alerts.

---




