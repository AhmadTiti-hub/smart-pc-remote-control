# Smart PC Remote Control System (IR + Air Mouse)

A full system that enables controlling a computer using an infrared remote and a motion-based air mouse.

## 🚀 Features
- Control PC using IR remote (volume, navigation, apps)
- Air mouse using gyroscope (MPU6050)
- Real-time cursor movement via ESP32 (Bluetooth)
- GUI-based Python application for command execution

## 🧠 System Overview

### IR Remote Module (Arduino Nano)
- Receives IR signals
- Decodes button inputs
- Sends commands via Serial

### Air Mouse Module (ESP32 + MPU6050)
- Reads motion data
- Converts motion into mouse movement
- Sends data via BLE

### PC Application (Python)
- Reads serial data
- Maps IR codes to actions
- Controls system using pyautogui

## 🧰 Technologies
- Arduino (C++)
- Python (Tkinter, PyAutoGUI)
- ESP32 (BLE Mouse)
- MPU6050 Sensor
- IR Receiver

## ⚙️ How to Run

### Python App
```bash
pip install -r requirements.txt
python pc_remote.py
