# 🛡️ Cyber Defense Agent (CDA)

An intelligent, real-time cyber defense system built using **FastAPI**, designed to detect, analyze, and respond to modern cyber threats such as ransomware, malware, SQL injection, and data exfiltration.

---

## 🚀 Features

* 🔍 Real-time threat detection engine
* 🧠 Rule-based + heuristic detection (SOC-style)
* ⚡ Automated response system (firewall, isolation, WAF rules)
* 📡 Simulated threat intelligence & event streaming
* 🚨 Severity-based alerting with escalation
* 🧪 DRY-RUN mode for safe testing
* 📊 Ready for dashboard integration (Streamlit / frontend)

---

## 🧩 Architecture

```
Client / Dashboard (Streamlit)
            ↓
      FastAPI Backend
            ↓
 ┌─────────────────────┐
 │  CyberDefenseAgent  │
 ├─────────────────────┤
 │ Detection Engine    │
 │ Responders          │
 │ Intel Collectors    │
 └─────────────────────┘
```

---

## 📁 Project Structure

```
files/
│── web_server.py
│── main.py
│── requirements.txt
│── README.md
│
├── core/
│   ├── __init__.py
│   └── agent.py
│
├── detectors/
│   ├── __init__.py
│   └── detection_engine.py
│
├── responders/
│   ├── __init__.py
│   └── responders.py
│
├── intel/
│   ├── __init__.py
│   └── collectors.py
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/cyber-defense-agent.git
cd cyber-defense-agent
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Application

Start the FastAPI server:

```bash
uvicorn web_server:app --reload
```

Open in browser:

* API Docs → http://127.0.0.1:8000/docs
* Dashboard → http://127.0.0.1:8000

---

## 🧪 Example Logs

```
[CRITICAL] ransomware | Ransomware file extension — rule S006
[HIGH] data_exfiltration | Exfiltration: 80 MB outbound
[CRITICAL] malware | Malware C2 beacon detected
```

---

## 🛡️ Detection Capabilities

| Category          | Description                     |
| ----------------- | ------------------------------- |
| SQL Injection     | Detects DB injection attempts   |
| XSS               | Cross-site scripting attacks    |
| Command Injection | OS command execution attempts   |
| Malware (C2)      | Command & Control communication |
| Ransomware        | File encryption patterns        |
| Data Exfiltration | Large outbound data transfer    |
| Lateral Movement  | Internal network propagation    |
| Phishing          | Suspicious URL patterns         |

---

## ⚡ Response Actions

* 🚫 Firewall rules (`iptables`)
* 🔒 Host isolation
* 🌐 WAF blocking rules
* 🚨 Alert escalation

> ⚠️ By default, system runs in **DRY-RUN mode** (no real blocking)

---

## 🌐 Deployment

### Option 1: Render

```bash
uvicorn web_server:app --host 0.0.0.0 --port 10000
```

### Option 2: Docker

```dockerfile
FROM python:3.11
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["uvicorn", "web_server:app", "--host", "0.0.0.0", "--port", "8000"]
```

---

## 📊 Streamlit Dashboard (Optional)

You can connect a Streamlit frontend to visualize alerts:

```bash
streamlit run streamlit_app.py
```

---

## ⚠️ Disclaimer

This project is intended for:

* Educational purposes
* Security research
* Simulation environments

Not recommended for production without further hardening.

---

## 👨‍💻 Author

Developed by Gurudarshan v

---

## ⭐ Contribute

Pull requests are welcome!
Feel free to open issues or suggest improvements.

---

## 📜 License

MIT License
