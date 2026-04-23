# Secure RFID Smart Door System

:::info

Author: ARIFOGLU Gul Neva  
GitHub Project Link: https://github.com/UPB-PMRust-Students/fils-project-2026-nevoss-s

:::


This project presents a smart home door system based on the STM32 microcontroller using the Rust programming language. The system provides secure and automated access control for a house entrance.

When a person approaches the door, a PIR motion sensor detects movement and activates the system. The user must scan an RFID card to gain access. If the card is valid, the door opens using a servo motor. If invalid, access is denied.

The system also uses LEDs and an LCD display to provide feedback, and a photoresistor to automatically control lighting after entry.

---

## Motivation

This project was chosen to simulate a real-life smart home system that combines security, automation, and embedded systems design. It provides practical experience with Rust in embedded environments and interaction with hardware components.

---

## Architecture
System workflow:

1. Person approaches the door  
2. PIR sensor detects motion  
3. RFID system activates  
4. Card is scanned  
5. STM32 verifies the card  
6. If valid:
   - Door opens (servo motor)
   - Green LED turns on
   - LCD displays welcome message  
7. If invalid:
   - Door remains closed
   - Red LED turns on  
8. After entry:
   - Light is controlled automatically using photoresistor  

---


## Log


- Week 1: Project idea selection  
- Week 2: Component research  
- Week 3: Hardware planning  
- Week 4: Initial setup  
- Week 5+: Implementation and testing  

---


## Hardware

Main components:

- STM32 microcontroller  
- RFID module (RC522)  
- PIR motion sensor  
- Servo motor (SG90)  
- LCD display (16x2 I2C)  
- LEDs  
- Photoresistor  
- Breadboard and jumper wires  

The STM32 microcontroller controls all peripherals. The RFID module is used for authentication, the PIR sensor detects motion, and the servo motor controls the door mechanism. The LCD provides feedback to the user, while LEDs indicate system status. The photoresistor enables automatic lighting control.

---



## Bill of Materials

| Component | Usage | Price |
|----------|------|------|
| STM32 | Main controller | 100 RON |
| RFID RC522 | Card reader | ~40 RON |
| Servo Motor SG90 | Door control | ~40 RON |
| PIR Sensor | Motion detection | ~20 RON |
| LCD 16x2 I2C | Display | ~20 RON |
| LEDs | Status indication | ~5 RON |
| Photoresistor | Light detection | ~2 RON |
| Breadboard & wires | Connections | ~20 RON |

## Software

|
The system is implemented in Rust and handles:

- Motion detection (PIR sensor)
- RFID authentication
- Servo motor control
- LED status signaling
- LCD communication
- Automatic lighting control

## Links

1. [link](https://embassy.dev/)
...
