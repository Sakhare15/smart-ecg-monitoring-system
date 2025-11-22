Smart ECG Monitoring System

A real-time web-based ECG monitoring system that visualizes ECG signals, detects R-peaks, calculates heart rate (BPM), and provides intelligent alerts with clinical recommendations. Includes email/SMS notifications, clinical suggestion panel, and real-time abnormality detection.

🚀 Features
📈 Real-Time ECG Visualization

Smooth scrolling ECG waveform

360 Hz sampling resolution

Red dot R-peak markers

1500-sample rolling window display

❤️ Intelligent Heart Rate Monitoring

Accurate BPM calculated from RR intervals

Real-time HR updates

Sudden HR change detection (>20 BPM in 10 sec)

🔔 Smart Alert System

Automatically detects and alerts:

Bradycardia (HR < 60 BPM)

Tachycardia (HR > 100 BPM)

Sudden heart rate jumps

Alerts show on UI + delivered via Email/SMS

Cooldown:

5-minute cooldown for repeated alerts

Prevents notification overload

📧 Email & SMS Notifications
Email (Fully Functional)

Sends automatic email alerts using Gmail

Contains abnormality details + clinical recommendations

Non-blocking (does not interrupt ECG stream)

SMS (Optional)

Ready for Twilio integration

Can be enabled via settings panel

🏥 Clinical Suggestions Panel

Each alert shows detailed, evidence-based guidance:

Severity (HIGH / MEDIUM)

Condition explanation

Immediate actions

Patient monitoring recommendations

Long-term suggestions

⚙️ Notification Settings (Persistent)

Enable/disable email

Enter your recipient address

Configure SMS (optional)

Settings saved automatically

📂 Project Structure
/
├── app.py                   # Flask backend + WebSocket streaming
├── static/
│   ├── script.js            # Frontend ECG rendering + alerts
│   └── styles.css           # UI styling
├── templates/
│   └── index.html           # Main UI panel
├── ecg_data/
│   └── mitbih_100.csv       # Medical-grade ECG sample
└── README.md

🏗️ Tech Stack
Frontend

HTML, CSS, JavaScript

Chart.js

Socket.IO

Responsive medical-grade UI

Backend

Python

Flask

Eventlet (async streaming)

WFDB for ECG processing

▶️ How to Run Locally
1️⃣ Install dependencies
pip install flask eventlet numpy wfdb

2️⃣ Start server
python app.py

3️⃣ Open browser
http://127.0.0.1:5000

🧪 How It Works

Load MIT-BIH ECG data

Stream ECG in chunks to frontend (real-time effect)

Detect R-peaks → Mark on graph

Calculate BPM using RR interval

Trigger alerts if abnormalities occur

Show clinical suggestions + send email/SMS

📊 Real-Time Alerts Include

Condition name

Severity level

What it means medically

Recommended immediate actions
<img width="1528" height="750" alt="Screenshot 2025-11-23 001410" src="https://github.com/user-attachments/assets/97408a58-c64f-4a30-9b6c-d8537f2a62fa" />
<img width="1534" height="812" alt="Screenshot 2025-11-23 001207" src="https://github.com/user-attachments/assets/535065f8-6417-4537-a849-93b9ac2153eb" />
<img width="1600" height="900" alt="Screenshot 2025-11-23 001126" src="https://github.com/user-attachments/assets/4a51be8f-4f62-466f-95c4-8ab982b1f9e2" />

Long-term recommendations

Auto email delivery with full report

🔮 Future Enhancements

AI-based arrhythmia prediction

Patient history dashboard

Cloud storage for ECG sessions

Android/iOS app extension

Medical practitioner login portal
