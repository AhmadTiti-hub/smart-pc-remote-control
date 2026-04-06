# Smart PC Remote Control System (IR + Air Mouse)

A graduation project that enables full control of a Windows PC using an infrared remote and a motion-based air mouse.

## Features
- PC control using an IR remote
- Air mouse based on ESP32 + MPU6050
- Real-time cursor movement over BLE
- Python desktop application for serial command handling
- Keyboard shortcuts, media controls, app launching, and system actions

## Project Structure
```text
smart-pc-remote-control/
├── arduino/
│   ├── air_mouse/
│   │   └── air_mouse.ino
│   └── ir_receiver/
│       └── ir_receiver.ino
├── python_app/
│   └── pc_remote.py
├── docs/
│   └── PCRemote_Project_Report.pdf
├── images/
├── requirements.txt
└── README.md
```

## System Overview

### 1) IR Receiver Module
Uses an Arduino Nano with a VS1838B IR receiver to detect remote button presses and send decoded hexadecimal values to the PC over serial.

### 2) Air Mouse Module
Uses an ESP32 with an MPU6050 gyroscope/accelerometer to convert hand motion into mouse movement and send it to the PC over Bluetooth Low Energy.

### 3) Python Desktop App
Reads incoming serial commands and maps IR codes to Windows actions such as:
- Volume up/down/mute
- Page up/down
- Arrow keys
- Enter / Backspace / Space
- Ctrl+A / Ctrl+C / Ctrl+V / Ctrl+X / Ctrl+Z
- Open Chrome / YouTube / Shahid / Netflix
- Windows shortcuts
- Shutdown

## Hardware Used
- Arduino Nano
- ESP32
- MPU6050
- VS1838B IR receiver
- LG IR remote
- Bluetooth USB adapter
- Breadboard and jumper wires

## Software / Libraries
- Arduino C++
- Python
- IRremote
- BleMouse / ESP32 BLE Mouse
- pyserial
- pyautogui
- pywin32

## How to Run

### Python app
```bash
pip install -r requirements.txt
python python_app/pc_remote.py
```

### Arduino sketches
Open and upload:
- `arduino/ir_receiver/ir_receiver.ino`
- `arduino/air_mouse/air_mouse.ino`

You may also need the external libraries included separately in this package.

## Notes
- The original project targeted Windows.
- Some paths in the Python app point to local Chrome / HTML files and may need adjustment on another computer.
- The included PDF report documents the design, components, testing, and results.

## Author
Ahmad Titi
