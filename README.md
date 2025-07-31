# Assignment 6 – What is Shodan?

## 🎯 Objective
To understand how Shodan (a search engine for Internet-connected devices) reveals publicly accessible data about hosts without active scanning.

## 🔍 Target: scanme.nmap.org
We explored the host `scanme.nmap.org` using [https://shodan.io](https://shodan.io) to view publicly visible information.

## 🖥️ Information Found

- **IP Address**: 45.33.32.156
- **Hostnames**: scanme.nmap.org
- **Location**: Fremont, California, USA
- **Organization**: Linode (Cloud provider)
- **ISP**: Akamai Connected Cloud
- **Operating System**: Ubuntu
- **Web Server**: Apache 2.4.7
- **Open Ports**:
  - **22 (SSH)** — Running OpenSSH 6.6.1p1
  - **80 (HTTP)** — Web interface (Apache)
  - **123, 31337** — Other exposed ports

## 🛡️ Security Analysis

### 👨‍💻 For Attackers:
- SSH version information (OpenSSH 6.6.1p1) can help attackers identify known vulnerabilities.
- Apache version may also have historical CVEs.
- Open ports allow mapping of attack surface without touching the host directly.

### 🧑‍💼 For Defenders:
- Shows how much data is public by default.
- Encourages banner obfuscation and port filtering.
- Highlights the need for external surface monitoring tools.

## 📸 Screenshot


<img width="2874" height="1728" alt="Screenshot 2025-07-31 224354" src="https://github.com/user-attachments/assets/fd0c60f5-f468-47c6-9bff-aa8e3e654356" />

## ✅ Conclusion
Shodan is a powerful tool that reveals what attackers can see without even scanning the system. It’s crucial for defenders to regularly audit their internet-facing assets using Shodan or similar tools.

