# Log Alert Generator

![Python](https://img.shields.io/badge/language-python-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

A Python-based log parser that scans authentication logs (`auth.log`) for suspicious activity like brute-force SSH attempts, invalid user logins, and unauthorized access. Alerts are automatically generated and exported to a `.csv` file for quick triage or integration with other tools.

---

##  Threats Addressed

| Threat                          | Detection Logic                                   |
|--------------------------------|---------------------------------------------------|
| Brute-force login attempts     | Multiple failed SSH logins from the same IP       |
| Credential stuffing / guessing | "Invalid user" entries with external IPs          |
| Unauthorized access            | Unexpected successful logins                      |

---

##  Features

-  Parse Linux-style `auth.log` files
-  Detect failed SSH login attempts
-  Flag invalid usernames
-  Track successful logins (for auditing)
-  Export alerts to structured `.csv` format
- Easy to customize or expand with new patterns

---

## Project Structure

log-alert-tool/
├── parser.py # Main script
├── sample_logs/
│ └── auth.log # Sample log input
├── alerts/
│ └── alerts.csv # Output alerts
├── screenshot.png # Output preview
├── README.md
└── .gitignore


---

## How to Use

### Requirements
- Python 3.x

### Run the Tool

```bash
python3 parser.py

alerts/alerts.csv
```csv
timestamp,alert_type,ip,severity,raw
2025-07-15T21:10:00,Invalid user login attempt,192.168.1.202,high,"Invalid user admin from 192.168.1.202 port 22"
2025-07-15T21:12:01,Failed SSH login,192.168.1.101,medium,"Failed password for root from 192.168.1.101 port 22 ssh2"
2025-07-15T21:13:00,Successful SSH login,192.168.1.10,info,"Accepted password for user1 from 192.168.1.10 port 22 ssh2"

## Screenshot

[![Tool Output Screenshot](screenshot.png)](screenshot.png)
