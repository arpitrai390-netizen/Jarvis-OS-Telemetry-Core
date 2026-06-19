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

## 🚀 How to Setup and Run

Follow these instructions to deploy and execute the Jarvis Telemetry Core on your local Windows environment.

### 1. Prerequisites & AI Setup
Make sure you have Python 3.10+ installed on your machine.
To utilize the local neural network matrix feature:
1. Download and install [Ollama](https://ollama.com).
2. Open your terminal and pull down the lightweight Llama model:
   ```bash
   ollama run llama3.2:1b
   ```

### 2. Installation
Clone this repository to your local directory and install all required hardware and software dependencies:
```bash
git clone https://github.com
cd Jarvis-OS-Telemetry-Core
pip install -r requirements.txt
```

### 3. Execution
Launch the primary operator dashboard core:
```bash
python main.py
```


