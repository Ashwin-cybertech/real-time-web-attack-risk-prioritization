# 🛡️ Real-Time Web Attack Risk Prioritization System

## 📌 Project Overview
This project simulates a real-world **Security Operations Center (SOC)** platform that detects, analyzes, prioritizes, and alerts on web attacks in **real time**.

It is designed as a **team-based SOC system**, where each module represents a different security role.  
All components were implemented **end-to-end by me**.

---

## 🎯 Objectives
- Detect web attack attempts in real time  
- Classify and analyze attacks  
- Map attacks to OWASP Top 10  
- Assign risk levels and response decisions  
- Store incidents for audit and compliance  
- Send instant alerts to SOC teams  

---

## 🧩 SOC Team-Based Architecture

This project is structured as a **10-role SOC workflow**:

| Role | Responsibility |
|----|----|
| Detection Engineer | Ingests real-time events via logs & webhooks |
| Web Security Analyst | Identifies attack type (SQLi, XSS, etc.) |
| OWASP Specialist | Maps attacks to OWASP Top 10 |
| Risk Analyst | Assigns risk score and severity |
| SOC Analyst | Decides monitor vs escalate |
| Incident Responder | Handles high-risk alerts |
| Notification Engineer | Sends Telegram alerts |
| Compliance Analyst | Logs incidents to database |
| Security Architect | Designs full SOC workflow |
| Automation Engineer | Orchestrates workflows using n8n |

---

## 🏗️ Architecture Flow
![n8n Workflow](screenshots/n8n-workflow.png)


Web Attack
↓
Vulnerable Web App (OWASP Juice Shop)
↓
Application Logs
↓
Python Log Monitoring Script
↓
n8n Webhook (Real-Time)
↓
Attack Analysis & Risk Scoring
↓
Database Logging
↓
Telegram Alert


---

## ⚙️ Technologies Used
- OWASP Juice Shop  
- Python  
- n8n  
- JavaScript  
- PostgreSQL  
- Telegram Bot API  
- Docker  

---

## 🔍 Key Features
- Real-time attack ingestion (webhooks)
- Attack classification (SQL Injection, XSS)
- OWASP Top 10 mapping
- Risk scoring (LOW / MEDIUM / HIGH)
- Automated SOC decision logic
- Incident logging for compliance
- Instant Telegram alerts

---

## 🧠 Detection & Analysis Logic
- SQL Injection → High Risk → Escalate
- XSS → Medium Risk → Monitor
- Suspicious activity → Logged for review

Detection is **log-based and pattern-driven**, similar to SIEM/WAF pipelines.

---

## ⚠️ Known Limitation
The demo application (OWASP Juice Shop) has limited stdout logging.  
Not all user actions generate logs, which reflects real-world log source challenges.

---

## 🚀 Future Enhancements
- Advanced correlation rules
- AI-based risk explanation
- Rate-based attack detection
- Dashboard visualization
- Ticketing system integration

---

## 🎤 Interview Summary
> Designed and implemented a real-time SOC system that detects web attacks, classifies threats, maps them to OWASP, assigns risk levels, logs incidents, and sends automated alerts.
