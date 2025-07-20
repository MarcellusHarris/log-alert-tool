#  Log Alert Tool

A Python-based log parsing tool that analyzes authentication logs for suspicious login activity, such as brute-force attempts, failed logins, or invalid users. It generates alerts into a structured CSV file — perfect for cybersecurity students, blue teamers, or anyone learning the fundamentals of threat detection.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License: MIT](https://img.shields.io/badge/License-MIT-green)

---

##  Live Project Page  
 [https://marcellusharris.github.io/log-alert-tool/](https://marcellusharris.github.io/log-alert-tool/)

---

##  Key Features

- Detects suspicious login attempts (failed SSH, invalid users)
- Parses logs using Python regex
- Saves alerts to CSV for easy review or SOC integration
- Lightweight and beginner-friendly

---

##  Screenshot

![Sample Output](log-tool-output.png)

---

##  How to Use

### 1. Clone the Repo

```bash
git clone https://github.com/MarcellusHarris/log-alert-tool.git
cd log-alert-tool

2025-07-15T21:12:01,Failed SSH login,192.168.1.101,medium,"Failed password for root from 192.168.1.101 port 22 ssh2"
2025-07-15T21:13:00,Successful SSH login,192.168.1.10,info,"Accepted password for user1 from 192.168.1.10 port 22 ssh2"

## Screenshot

[![Tool Output Screenshot](screenshot.png)](screenshot.png)
