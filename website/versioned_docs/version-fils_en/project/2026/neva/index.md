# Secure RFID Smart Door System

## Description
This project presents a smart home door system based on the STM32 microcontroller using the Rust programming language. The system provides secure and automated access control for a house entrance.

When a person approaches the door, a PIR motion sensor detects movement and activates the system. The user must scan an RFID card to gain access. If the card is valid, the door opens using a servo motor. If invalid, access is denied.

The system also uses LEDs and an LCD display to provide feedback, and a photoresistor to automatically control lighting after entry.

## Motivation
This project was chosen to simulate a real-life smart home system that combines security, automation, and embedded systems design. It provides practical experience with Rust in embedded environments and interaction with hardware components.

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

## Weekly Progress
- Week 1: Project idea selection  
- Week 2: Component research  
- Week 3: Hardware planning  
- Week 4: Initial setup  
- Week 5+: Implementation and testing  

## Hardware Design
Main components:
- STM32 microcontroller  
- RFID module (RC522)  
- PIR motion sensor  
- Servo motor (SG90)  
- LCD display (16x2 I2C)  
- LEDs  
- Photoresistor  
- Breadboard and jumper wires  

The STM32 controls all peripherals, processes RFID data, and manages system behavior.

## Software Design
The system is implemented in Rust. It handles:
- Motion detection
- RFID authentication
- Servo motor control
- LED indicators
- LCD communication
- Light control via photoresistor  

## Detailed Design
System flow:
- Initialize all peripherals  
- Wait for motion detection  
- Activate RFID reader  
- Read card data  
- Verify card  
- Control door (servo)  
- Update LEDs and LCD  
- Control lighting system  

## Bill of Materials
- STM32 – 0 RON  
- RFID RC522 – ~40 RON  
- Servo motor – ~10 RON  
- PIR sensor – ~10 RON  
- LCD display – ~20 RON  
- LEDs – ~5 RON  
- Photoresistor – ~2 RON  
- Breadboard and wires – ~20 RON  

## Software Libraries
- embassy-stm32  
- embassy-executor  
- embassy-time  
- mfrc522  
- lcd-lcm1602-i2c  
- embedded-hal-bus  
- defmt-rtt  
- panic-probe  
