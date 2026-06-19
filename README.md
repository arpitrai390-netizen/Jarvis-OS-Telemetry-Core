# JARVIS: Workstation Telemetry Core & Voice Operator

An asynchronous, voice-activated desktop assistant built with Python. This project was developed to explore real-time system tracking, OS-level hardware manipulation, and local AI execution.

## 🛠️ System Architecture & Tech Stack
- **Language:** Python
- **GUI Engine:** Tkinter (Custom dark-themed telemetry visual dashboard)
- **Concurrency:** Asynchronous execution using the `threading` library to prevent UI freeze during speech loops
- **Local AI Brain:** Integrated via `ollama` running an offline `llama3.2:1b` model
- **Hardware Telemetry:** `psutil` for live CPU/RAM tracking, `keyboard` for native OS manipulation, and `pvrecorder` for acoustic amplitude filtering

## ⚡ Key Engineering Features
- **Acoustic Energy Filtering:** To save processing overhead, the system reads audio in 512-sample frames and only triggers Google Speech Recognition when the structural amplitude metrics cross a defined volume threshold.
- **Native OS Manipulation:** Bypasses driver issues by simulating low-level Windows keyboard media button signals directly via software.
- **Robust Exception Handling:** Isolated all local AI network operations and hardware calls in `try-except` blocks to maintain runtime stability.

*Note: Developed with algorithmic assistance from Gemini for structural optimization and UI threading design.*
