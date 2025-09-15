# Smart Robot Car Project

## Overview
This project is an Arduino-based smart robot car that can operate in multiple modes: Bluetooth control, self-driving (obstacle avoidance), and line following. The car uses ultrasonic sensors for distance measurement, IR sensors for line detection, and an LCD for user feedback. It is designed to demonstrate a blend of embedded systems, robotics, and real-time control, reflecting my journey in hands-on robotics and automation.

## Features
- **Bluetooth Control:** Remotely control the car's movement and speed using a mobile device.
- **Self-Driving Mode:** The car autonomously avoids obstacles using three ultrasonic sensors.
- **Line Following:** Two line-following algorithms using multiple IR sensors for path tracking.
- **LCD Display:** Real-time feedback and instructions displayed to the user.
- **Modular Code:** Functions for each mode (Bluetooth, self-driving, line following) for easy extension and debugging.

## Hardware Used
- Arduino Uno (or compatible)
- L298N Motor Driver
- 3x Ultrasonic Sensors (HC-SR04)
- 7x IR Sensors
- LiquidCrystal I2C LCD
- Bluetooth Module (e.g., HC-05)
- Motors, Chassis, Power Supply

## Code Structure
- **setup() / loop():** Initializes hardware and manages mode switching based on serial input.
- **bluetooth_controle():** Handles remote commands for movement and speed.
- **self_driving():** Implements obstacle avoidance logic using sensor data.
- **line_following1() / line_following2():** Two different line following strategies.
- **sensor_distance(), speed_controle():** Utility functions for sensor calibration and speed management.

## How It Works
1. **Startup:** LCD greets the user and prompts for Bluetooth connection.
2. **Mode Selection:** Modes are switched via serial commands (e.g., from a mobile app).
3. **Operation:**
   - In Bluetooth mode, the car responds to directional and speed commands.
   - In self-driving mode, it navigates around obstacles.
   - In line-following mode, it tracks lines using IR sensors.
4. **Feedback:** LCD provides real-time status and instructions.

## My Learning Journey
This project was a major step in my robotics learning path. I learned:
- Integrating multiple sensors and actuators with Arduino.
- Writing modular, maintainable embedded code.
- Real-time debugging and troubleshooting hardware/software issues.
- Designing user-friendly feedback systems (LCD, Bluetooth interface).
- The importance of calibration and robust error handling in robotics.

## Getting Started
1. **Wiring:** Connect all sensors, motors, and modules as per the pin assignments in the code.
2. **Upload:** Flash the `PROJECT_CAR.ino` code to your Arduino.
3. **Power Up:** Supply power to the car and connect via Bluetooth (if desired).
4. **Control:** Use a mobile app or serial monitor to send commands and switch modes.

## Pin Assignments
- **Motors:** 3, 5, 6, 9
- **Ultrasonic Sensors:** Trig (4, 7, 8), Echo (10, 11, 12)
- **IR Sensors:** 2, 13, 14, 15, 16, 17, 18
- **LCD:** I2C (0x27)

## Acknowledgements
- Inspired by open-source robotics projects and the Arduino community.
- Special thanks to online tutorials and forums for troubleshooting help.

---
*Made by Saud Ahmad – Robotics & AI Enthusiast*
