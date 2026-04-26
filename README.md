# Smart Car — Driver Safety System

![license](https://img.shields.io/badge/license-MIT-green)
![platform](https://img.shields.io/badge/platform-Arduino%20UNO-00979d)
![language](https://img.shields.io/badge/language-Python%20%7C%20C%20%7C%20Arduino-e4812f)
![status](https://img.shields.io/badge/status-Completed%202025-238636)

Intelligent driver safety system developed as part of an IoT project — 2nd year ISIMM


## Project Demo
▶️ [Watch on YouTube](https://youtube.com/shorts/Xk-KSTW5c6g?feature=share)

## Description
Smart Car is an embedded system that monitors the driver's condition in real time to prevent road accidents caused by drowsiness or alcohol consumption.

## Objectives
- Detect driver drowsiness using computer vision
- Detect alcohol presence using the MQ-3 sensor
- Alert the driver in case of danger (LED, buzzer, LCD screen)
- Integrate sensors, microcontroller and software into a functional system

## Technologies Used
| Component | Role |
|-----------|------|
| Arduino UNO | Main microcontroller |
| MQ-3 Sensor | Alcohol detection |
| Camera | Captures driver's face |
| LED + Buzzer | Visual and audio alerts |
| LCD Screen | Displays alert messages |
| Python + OpenCV | Drowsiness detection (Haar Cascade) |
| Arduino IDE | Microcontroller programming |
| VS Code | Python script development |

## System Architecture
───Camera Feed → OpenCV + Haar Cascade → Python Vision Layer → Serial (USB)
                                                                  ↓
MQ-3 Alcohol Sensor ───────────────────────────────→ Arduino UNO → LED / Buzzer / LCD Alert

## How It Works
1. Camera captures the driver's face in real time
2. Python + OpenCV analyzes the eyes using Haar Cascade
3. If eyes are closed too long → drowsiness alert triggered
4. MQ-3 sensor continuously measures alcohol level
5. In case of danger → LED + buzzer + message on LCD screen

## Getting Started
**1. Install Python dependencies**
bash
pip install opencv-python pyserial numpy
**2. Upload Arduino sketch**
Open arduino/smart_car.ino in Arduino IDE
Select board: Arduino UNO → Upload
**3. Run the vision module**
bash
python vision/drowsiness_detector.py --port COM3

## Project Structure
smart-car/
├── vision/
│   ├── drowsiness_detector.py
│   └── serial_bridge.py
├── arduino/
│   └── smart_car.ino
├── pcb/
│   └── layout.cad
├── README.md
└── requirements.txt

## Future Improvements
- **Automatic SMS Alert** — Upon accident detection, automatically sends an SMS to the emergency contact via GSM SIM800L module
- **GPS Tracking** — Sends the exact vehicle location to the emergency contact
- **Mobile App** — Real-time monitoring of driver's condition

## Author
**Yosr Derbeli** — 2nd year IoT Student, ISIMM Monastir  
[github.com/yosrderbali](https://github.com/yosrderbali)
