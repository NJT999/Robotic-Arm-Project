# 5-DOF Robotic Arm
This is a 5-degree-of-freedom robotic arm that is built utilizing three MG90s microservos, two MG996R microservos, five 10k Ohm Potentiometers, and an ESP32 microcontroller. This project has been built and designed entirely by me with some external inspiration from others robotic arm projects online. To differentiate myself from preexisting projects, I plan to add a second part of this project which will utilize a webcam and OpenCV to sort colored blocks. 

## Overview
This project is my first personal project and has served as a way to learn CAD via Fusion360 and to interact with the Arduino IED before college. This arm will start off by being manually controlled through five potentiometers, but the project will evolve to use the OpenCV software to have the arm "color-sense." Currently, each potentiometer is linked servos controlling the waist, shoulder, elbow, wrist, and gripper respectively. 

## Hardware
Component | Quantity | Purpose
--- | --- | --- 
MG90s Micro Servo | 3 | Joint Rotation
MG996R Servo | 2 | Joint Rotation (Base / Shoulder) 
10k Potentiometer | 5 | Manual Joint Control
ESP32 Microcontroller | 1 | "Brain" (Controls Elements in Circuit)
Electrolytic Capacitor (1000µF) | 1 | Smooths Power Fluctuation

## Software
* Arduino IED - Used to control servos with potentiometers and PWM
* Fusion360 - Used to model and print robotic arm with CAD
* KiCad 10.0 - Used to design the PCB that is used in the arm  

## Breadboard Wiring (Prototype) 
- Used an external power supply of 5V and 4 amps to supply circuit
- External power supply would connect to the servos and to the VIN pin on the ESP32
- The ESP32 would emit 3.3V from the 3v3 pin for the potentiometers
- The 1000µF Capacitor was placed after the external power supply to reduce fluctuation from servos

Servo | Pin 
--- | --- 
Base | GPIO 13 
Shoulder | GPIO 14 
Elbow | GPIO 27 
Wrist | GPIO 26
Gripper | GPIO 25

Potentiometer | Pin 
--- | --- 
Base | GPIO 36 
Shoulder | GPIO 39 
Elbow | GPIO 34 
Wrist | GPIO 35
Gripper | GPIO 32

## CAD Design

## PCB Design


## Project Phases
### Phase 1 
- [x] Hardware selected and modeled on breadboard
- [x] Potentiometer mapping and servo testing
- [x] Arm modeled in Fusion360
- [ ] Arm 3D printed and assembled
- [x] PCB designed and ordered via JLCPCB
- [ ] Redesign base and integrate PCB into base

### Phase 2 
- [ ] Webcam mounted in sorting location
- [ ] OpenCV script written in Python
- [ ] ESP32 receives commands via WiFi
- [ ] Arm autonomously sorts by color

## Challenges / Lessons Learned
### Servo Torque ###
- The MG90 microservos 2.2 kg/cm stall torque was exceeded when arm was fully extended 
- Upgraded MG90 servos in the base and shoulder joints to MG996R servos (9.4 kg/cm)
- Removed unnecessary plastic in joints to decrease stress on joints
- Learned to calculate how much torque is necessary before designing arm.

### Wire Consideration ###
- Wires from the MG90 servos would be pinched at certain positions or would dangle from the arm
- Added holes in certain parts and additional space to fit wires
- Learned to account for all aspects of components during the design

### Manufacture Discrepancies ###
- Manufacturing dimension specs would differ from the physical motors
- Measured each servo using a digital dial caliper to obtain actual dimensions
- Learned to measure twice, cut once

## Author
Noah Thompson 
Incoming Engineering Student — Iowa State University, Class of 2030
