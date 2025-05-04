# 🛡️ Ransomware Simulation Project – CSCE 5550

## 📌 Project Summary

This project simulates the complete workflow of a **file-encrypting ransomware attack** and implements a full defense pipeline, developed for the CSCE 5550 course (Spring 2025). All components were tested in a **controlled VM environment** using **Kali Linux**, **Windows 10**, and **Python 3.12**.

The project focuses on four main phases:

1. **Infection** – Delivered a ransomware payload using Metasploit (EternalBlue exploit).
2. **Monitoring** – Tracked file changes in real time using Python's `watchdog`.
3. **Detection** – Identified suspicious activity based on rapid `.pdf` file modifications.
4. **Mitigation** – Terminated malicious `.exe` processes and provided popup alerts.


---

## 🔧 Tools & Technologies Used

- Kali Linux (Attacker VM)
- Windows 10 (Victim VM)
- Metasploit Framework (MS17-010)
- Python 3.12 (on Windows)
- Python Libraries: `cryptography`, `watchdog`, `ctypes`, `subprocess`, `shutil`
- Fernet encryption (AES-128 under the hood)
- Log files: `monitor_log.json`, `detection_log.json`, `mitigation_log.json`

---

## 📁 Components

| File | Description |
|------|-------------|
| `project.py` | Encrypts/decrypts `.pdf` files using a Fernet key and displays a ransom popup. |
| `monitor.py` | Monitors file events in a target folder and logs them to `monitor_log.json`. |
| `detection.py` | Analyzes logs to detect ransomware-like behavior based on time-based thresholds. |
| `mitigation.py` | Terminates recently modified `.exe` files that are running and logs actions. |

---

## 🔐 What We Did *Not* Upload

This GitHub repository **does not contain**:

- Any actual payloads, exploits, `.exe` binaries, or shellcode.
- Any Metasploit scripts or output.
- Any tools or code intended for malicious purposes.

All payload generation, shell access, and exploitation steps were performed **locally within a closed VM lab environment** for educational purposes only.

---

## ⚠️ Ethical Use Disclaimer

This project is intended **strictly for academic and research purposes**.

- All testing was done in isolated virtual machines.
- No real-world systems were impacted.
- This repository should **not** be used for malicious purposes.

---

## 👨‍💻 Author

**Sai Kumar**  
M.S. Computer Science – University of North Texas  
Course: CSCE 5550 – Computer Security, Spring 2025  
Instructor: Dr. [Insert Instructor Name]

---

## 🧠 Outcome

This project demonstrates a realistic ransomware attack and response simulation, covering:

- Delivery and execution of a ransomware payload
- Encryption using strong symmetric cryptography
- Detection via rule-based behavioral analysis
- Real-time mitigation of suspicious processes
- Safe recovery using backups

---

## 📌 Final Note

If you're using this repository, ensure that all activities are conducted ethically, legally, and inside a secure testing environment.
