# 🔍 Wireshark Network Traffic Analysis & Protocol Profiling

<div align="center">

![Wireshark](https://img.shields.io/badge/Wireshark-v4.x-1679A7?style=for-the-badge&logo=wireshark&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Guest_OS-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![VirtualBox](https://img.shields.io/badge/VirtualBox-Oracle-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

*A comprehensive packet-level investigation profiling transport and application layer behaviors — DNS resolution, TCP handshakes, TLSv1.3 streams, and anomaly detection.*

</div>

---

## 📖 Overview
This project demonstrates hands-on network forensics using Wireshark to capture, decode, and analyze live network telemetry. It covers the full inspection pipeline — from low-level TCP flag verification to encrypted TLS session fingerprinting.

---

## ✨ Features
- **DNS Protocol Dissection:** Detailed mapping of domain lookups and query/response structures.
- **TCP Handshake Verification:** Inspection of `SYN`, `SYN-ACK`, and `ACK` flag sequences.
- **Cryptographic Stream Analysis:** Fingerprinting of TLSv1.3 handshake parameters and cipher negotiation.
- **Anomaly Profiling:** Real-time extraction of TCP sequence warnings via Wireshark Expert Info.
- **Volumetric Visualization:** Monitoring packet-per-second loads using I/O Graphs.

---

## 💻 Technologies Used
- **Network Analyzer:** Wireshark v4.x
- **Virtualization:** Oracle VirtualBox
- **Guest OS:** Linux
- **Protocols Analyzed:** DNS · TCP · TLSv1.3 · IPv4 · UDP

---

## 🛠️ Installation & Setup

### Prerequisites
Install [Wireshark](https://www.wireshark.org/download.html) on your local system.

### Clone the Repository
```bash
git clone https://github.com/kunalkushwaha-tech/Wireshark-Network-Analysis.git
cd Wireshark-Network-Analysis
Open a Capture File
1.Launch Wireshark.
2.Go to File → Open.
3.Select a .pcapng file from your saved captures directory.
🕹️ Usage — Display Filters
Paste these filters directly into the Wireshark filter bar:
# Filter DNS traffic only
dns

# Isolate TCP 3-way handshake (SYN packets)
tcp.flags.syn == 1

# Filter all TLS/SSL streams
tls
## 📸 Analysis Captures

### 1. 🌐 DNS Resolution Mappings
![DNS Analysis](screenshorts/dns-resolution.jpg)

### 2. 🤝 TCP 3-Way Handshake
![TCP Handshake](codes/tcp-handshake.jpg)

### 3. 🔐 TLS Parameter Negotiation
![TLS Traffic](screenshorts/tls-negotiation.jpg)

### 4. ⚠️ Expert Information Diagnostics
![Expert Info](screenshorts/expert-info.jpg)

### 5. 📊 Volumetric I/O Graph
![I/O Graph](screenshorts/io-graph.jpg)

### 6. 🌊 Protocol Flow Sequences
![Flow Graph](screenshorts/protocol-flow.jpg)

### 7. 💬 Session Conversations
![Conversations Tracking](screenshorts/conversations.jpg)
📁 Repository Structure
Wireshark-Network-Analysis/
├── screenshorts/         # All 7 annotated analysis captures
├── .gitignore            # Git untracked file rules
├── LICENSE               # MIT open-source license
├── README.md             # Project documentation (this file)
└── requirements.txt      # Python automation dependencies

🎓 Learning Outcomes
Packet Dissection — Decoded OSI Layer 4 (TCP/UDP) and Layer 7 (DNS/TLS) structural headers.
Security Baseline — Differentiated between plaintext and cryptographically secured sessions.
Network Diagnostics — Identified connection dropouts, retransmissions, and anomalies via Expert Info.
🔮 Future Improvements
[ ] PyShark script to automate malformed packet detection from the CLI.
[ ] GeoIP database integration to map server locations geographically.
👤 Author
Kunal Kushwaha
Student · Cybersecurity Intern
(https://github.com/kunalkushwaha-tech)
📄 License
This project is licensed under the MIT License — see the LICENSE file for details.

