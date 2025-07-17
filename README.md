# Log Alert Generator

![Python](https://img.shields.io/badge/language-python-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

A Python-based log parser and alert generator that detects suspicious login activity from system authentication logs (`auth.log`). Built for cybersecurity learners, SOC analysts, and anyone interested in detection engineering or log forensics.

---

## Project Overview

This tool scans system logs for signs of brute-force attacks, privilege escalation attempts, and unauthorized access. Alerts are automatically generated and saved to a CSV file for quick triage or integration with other tools.

---

## Threats Addressed

| Threat                          | Detection Logic                                   |
|--------------------------------|---------------------------------------------------|
| Brute-force login attempts     | Multiple failed SSH logins from same IP          |
| Credential stuffing / guessing | "Invalid user" entries with external IPs         |
| Unauthorized access            | Unexpected successful logins                     |

---

## Features

-  Parse Linux-style `auth.log` files
-  Detect failed SSH login attempts
-  Flag invalid usernames
-  Track successful logins (audit visibility)
-  Export alerts to structured `.csv`
- Easy to customize or expand

---

## 📂 Folder Structure
log-alert-tool/
├── parser.py # Main script
├── sample_logs/
│ └── auth.log # Sample log input
├── alerts/
│ └── alerts.csv # Output alerts
├── README.md
└── .gitignore

---

## How to Use

### Requirements:
- Python 3.x

### Run the Tool:

```bash
python3 parser.py
