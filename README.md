# 🛡️ Threat Scanner

![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg)
![Platform: Web Crypto API](https://img.shields.io/badge/Crypto-SHA--256%20Client--Side-cyan.svg)
![Engines: 36 Vendors](https://img.shields.io/badge/Engines-36%20Security%20Vendors-blue.svg)

A client-side URL, File, and Hash Security Inspector inspired by VirusTotal. **Threat Scanner** inspects suspicious URLs, computes real cryptographic file hashes locally in the browser via the Web Crypto API without uploading sensitive files, and aggregates multi-vendor security detections alongside static heuristic analysis.

🔗 **[Live Demo on GitHub Pages](https://Shiv2048.github.io/threat-scanner/)**

---

## ✨ Key Features

* **🔒 Privacy-First Local File Hashing (Web Crypto API):** Computes real **SHA-256** and **SHA-1** cryptographic digests and inspects binary **Magic Header Bytes** (`ArrayBuffer`) directly inside the browser—zero server file uploads required.
* **🔍 Static URL Heuristic Engine:** Evaluates URLs using **Shannon Entropy** (randomness scoring), high-risk TLD detection (`.xyz`, `.top`, `.zip`), unencrypted HTTP checks, raw IPv4 host usage, and brand typosquatting detection.
* **🛡️ 36-Engine Vendor Detection Matrix:** Visualizes multi-vendor threat consensus (`Clean`, `Phishing`, `Malware`, `Trojan.Dropper`, `Suspicious`, `Unrated`) with interactive filtering and search.
* **🌐 WHOIS, DNS & SOC Remediation Playbook:** Displays simulated DNS (`A`, `MX`, `NS`, `TXT`) and WHOIS telemetry alongside deterministic Firewall/EDR blocklist rules and one-click **JSON / CSV IOC export**.
* **🧰 Built-in URL Defanger:** Converts live malicious links into safe, non-clickable IOCs (`http://` ↔ `hxxp://`, `.` ↔ `[.]`) for safe sharing in incident tickets.

---

## 📁 Repository Structure

```text
threat-scanner/
├── index.html          # Self-contained Threat Scanner web application
├── README.md           # Project documentation & architecture overview
├── LICENSE             # MIT Open-Source License
└── .gitignore          # Standard OS & IDE ignore rules
```

---

## 🚀 Quick Start (Run Locally)

Because Threat Scanner uses a zero-build, standalone HTML5 architecture, no Node.js or external package installation is required:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Shiv2048/threat-scanner.git
   ```
2. **Launch the inspector:**
   Navigate into the project folder and double-click `index.html` to open it in any modern browser (Chrome, Edge, Firefox, Safari).

---

## 🛠️ Tech Stack

* **Frontend:** HTML5, Vanilla JavaScript (ES6+), Tailwind CSS
* **Cryptography & Binary Inspection:** Browser Native **Web Crypto API** (`crypto.subtle.digest`) & `FileReader` (`ArrayBuffer`)
* **UI & Visualization:** Lucide Icons, Dynamic SVG Circular Detection Gauges

---

## 📄 License

Distributed under the MIT License. Copyright (c) 2026 Shivam Vinayak Patil. See `LICENSE` for details.