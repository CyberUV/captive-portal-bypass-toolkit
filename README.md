
# 🔧 Captive Portal Exploitation Toolkit  
### *(JNU WiFi Rate Limit Bypass – Proof of Concept)*

![Python](https://img.shields.io/badge/Made%20with-Python-green?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=flat-square)

> A Python-based red-team utility for identifying and exploiting session mismanagement in captive portals, targeting WiFi data rate-limiting flaws like those found on the JNU campus network.

---

## 📌 Table of Contents

- [🔍 Features](#-features)
- [🛠️ Tech Stack](#️-tech-stack)
- [🚀 Usage](#-usage)
- [📁 File Structure](#-file-structure)
- [🎯 Objective](#-objective)
- [⚠️ Disclaimer](#️-disclaimer)
- [✍️ Author](#-author)

---

## 🔍 Features

- ✅ Automates login/logout process using HTTP form manipulation and R-ID credentials  
- 🔁 Cycles valid R-IDs to bypass session quotas and rate limits  
- 🔍 Detects timeouts or quota exceedance and re-authenticates automatically  
- 📡 Uses `netsh wlan` to detect SSID and interface for accurate targeting  
- 🧠 Tracks session use and rotates credentials using `login.txt` and `log.txt`  
- ♻️ Supports recursive re-login/logout loops for sustained access  

---

## 🛠️ Tech Stack

- **Language:** Python 3.x
- **Libraries:** `requests`, `subprocess`, `re`, `time`  
- **Concepts:** Captive Portal Enumeration, HTTP Form Exploitation, Session Management  
- **Platform:** Windows (CLI-based via `netsh` utilities)

---

## 🚀 Usage

1. **Clone the repository:**

```bash
git clone https://github.com/CyberUV/captive-portal-exploitation-toolkit.git
cd captive-portal-exploitation-toolkit
pip install requests
```
2. **Configure login.txt with R-ID credentials:**
``` 
r-id1
r-id2
r-id3
.
.
.
```
3. **Run main script**

`python3 data_limit.py`
>Main Dashboard
```
Internet Access In JNU Server
--------------------------------
1> Check Connectivity
2> Login
3> Logout
4> Unlimited Data
5> SYNC Login File
6> Exit

option =>
```
> Choose option 5 to sync the login file
```
Checking R-ID status
------------------------------
[+] Total R-IDs in login.txt: 9
[+] R-IDs used: 3 out of 9
[+] Last used R-ID: 31006
[+] Current R-ID in use: 30890
[?] Have you entered new R-IDs in login.txt? (yes/no): yes
```
> Enjoy the toolkit


## 📁 File Structure 
```
captive-portal-exploitation-toolkit/
│
├── data_limit.py         # Core automation logic
├── banner.py 
├── all_network.py
├── login.txt             # List of R-ID credentials
├── log.txt               # Tracks session activity
├── README.md             # Documentation
```

## 🎯 Objective
Developed as part of a **cybersecurity research initiative**, this toolkit explores weaknesses in real-world captive portals, specifically focusing on **session and rate-limit misconfigurations**.

> 🔐 This tool serves as an educational PoC to understand and responsibly disclose flaws in WiFi access control systems.

## ⚠️ Disclaimer

**This project is for educational and authorized penetration testing purposes only.**  
Any misuse of this tool on unauthorized networks is unethical and illegal.  
This toolkit was tested only in a **controlled lab** environment and **not deployed against live production infrastructure**.

## ✍️ Author

**Rudraksh Yadav**  
GitHub: [CyberUV](https://github.com/CyberUV)
Email: youaregorges@gmail.com
