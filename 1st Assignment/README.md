# Assignment 6 – What is Shodan?

## 🎯 Objective
To understand how Shodan (a search engine for Internet-connected devices) reveals publicly accessible data about hosts without active scanning.

---

## 🧪 Methodology

1. Navigated to [https://shodan.io](https://shodan.io)
2. Used the search query `scanme.nmap.org`
3. Examined the data shown: IP address, hostnames, organization, services, open ports, operating system, and banner information
4. Took a screenshot of the result for documentation
5. Analyzed the findings from both an attacker's and defender's point of view

---

## 🔍 Target: scanme.nmap.org

- **IP Address**: 45.33.32.156  
- **Hostnames**: scanme.nmap.org  
- **Location**: Fremont, California, USA  
- **Organization**: Linode (Cloud provider)  
- **ISP**: Akamai Connected Cloud  
- **Operating System**: Ubuntu  
- **Web Server**: Apache 2.4.7  
- **Open Ports**:
  - **22 (SSH)** — OpenSSH 6.6.1p1
  - **80 (HTTP)** — Apache Web Server
  - **123, 31337** — Miscellaneous exposed ports

---

## 📸 Screenshot



<img width="2874" height="1728" alt="Screenshot 2025-07-31 224354" src="https://github.com/user-attachments/assets/a9333107-2b5f-4b06-b76e-79e76b089e94" />


## 🔎 Findings

### 👨‍💻 For Attackers:
- Banner info (e.g., **OpenSSH 6.6.1p1**, **Apache 2.4.7**) may help attackers identify known CVEs
- Public ports give insight into services running on the target
- All this was found **without even scanning** — purely via Shodan

### 🧑‍💼 For Defenders:
- Shows how easily information leaks if not hardened
- Banner obfuscation and version hiding can reduce exposure
- Shodan is useful for **self-auditing** to check what your system exposes

---

## ✅ Conclusion – What I Learned

- **Shodan** is an extremely powerful tool for passive reconnaissance
- It demonstrates that information about exposed services is **already public** — even without an attacker actively scanning a host
- **Security isn’t just about firewalls** — it's also about knowing your digital footprint
- Regular monitoring with tools like Shodan can help defenders identify misconfigurations and fix them before attackers exploit them

---

## 💻 Code / Scripts Used

_No scripts were used for this assignment, as it involved only passive analysis through the Shodan web interface._

