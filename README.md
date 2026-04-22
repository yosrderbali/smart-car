# Smart Car - Safety System
 Intelligent driver safety system developed as part of an IoT project — 2nd year ISIMM

## 🎥 Project Demo
https://youtube.com/shorts/Xk-KSTW5c6g?feature=share

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

## How It Works
1. Camera captures the driver's face in real time
2. Python + OpenCV analyzes the eyes using Haar Cascade
3. If eyes are closed too long → drowsiness alert triggered
4. MQ-3 sensor continuously measures alcohol level
5. In case of danger → LED + buzzer + message on LCD screen
   
## Future Improvements
**Automatic SMS Alert** Upon accident detection, automatically sends an SMS to the victim's emergency contact via GSM SIM800L module, compensating for slow ambulance response times
- **GPS Tracking** Sends the exact vehicle location to the emergency contact
- **Mobile App** Real-time monitoring of driver's condition

## Author
**Yosr Derbali** — 2nd year IoT Student, ISIMM Monastir
