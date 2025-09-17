# Automated-Incident-Response-Bot
It is a Python-based automated incident response system designed to detect suspicious processes in real time, classify threats, and alert users instantly. The system integrates with a Flask web dashboard for live monitoring and uses the Twilio API to deliver SMS/WhatsApp alerts with secure OTP verification.  

# Features
* 🔍 Log Monitoring Engine – Continuously scans system logs for suspicious entries.

* 🧠 Threat Classification Module – Matches process behavior against predefined rules (rules.json).

* 🆔 Incident ID Generator – Assigns unique identifiers to each incident.

* 📲 Real-time Alerts – Sends SMS/WhatsApp notifications via Twilio with direct dashboard links.

* 🌐 Flask Web Dashboard – Allows users to view incidents, manage subscriptions, and verify OTPs.

* ⏱ Timestamp Generator – Tracks when incidents occur for audit and reporting.

# 🔑 Use Cases

* Endpoint monitoring in small-scale networks.

* Security awareness demonstrations.

* Learning project for cybersecurity, automation, and Flask development.

* 🗄 Incident Data Store – Stores alerts in SQLite for persistence and analysis.

* 🚫 Duplicate Alert Filter – Prevents repeated alerts for the same incident.

# 🛠 Tech Stack

* Programming Language: Python

* Web Framework: Flask

* Database: SQLite

# How It Works

* The Log Monitoring Engine watches system logs and identifies suspicious activity.

* Detected events are processed by the Threat Classification Module and assigned an Incident ID.

* The Alert Trigger Controller checks for duplicates, generates a timestamp, and saves data in the Incident Data Store.

* A verified user is alerted via SMS/WhatsApp through the Messaging Gateway (Twilio API).

* The Flask Web Dashboard provides a central view of all incidents, severity levels, and user subscriptions.

* APIs: Twilio (SMS/WhatsApp Alerts)

* Other Tools: JSON rule sets, PowerShell/Bash scripting

 # 1. Set Up the Environment
     python -m venv venv
    .\venv\Scripts\Activate.ps1
     pip install -r requirements.txt

#  2. Initialize the Database
    flask shell
    
# Inside the shell
    from app import db
    db.create_all()
    exit()
# 3. Run the Flask Dashboard
    $env:FLASK_APP = "app.py"
    flask run

# 4. Simulate Cyber Attacks
    python simulate_attack.py
    
# 5. Trigger whatsapp notifications via twilio API
    account_sid = 'your_account_sid'
    auth_token = 'your_auth_token'
    from_whatsapp = 'whatsapp:+14155238886'
    to_whatsapp = 'whatsapp:+91xxxxxxxxxx'
# Then run the notification script
    python send_whatsapp.py

# 6. Auto refresh dashboard
    setInterval(loadAlerts, 10000); 

# requirements.txt
    Flask==2.3.3
    Flask-SQLAlchemy==3.1.1
    twilio==8.6.0

# Summary
# 🔧 How to Run

    1. Clone the repo  
    2. Create and activate a virtual environment  
    3. Install dependencies  
    4. Initialize the database  
    5. Run `flask run` to start the dashboard  
    6. Run `simulate_attack.py` to inject alerts  
    7. Run `send_whatsapp.py` to notify via Twilio  
    8. View and manage alerts at `http://127.0.0.1:5000`







