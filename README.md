# 5-DOF Robotic Arm
This is a 5-degree-of-freedom robotic arm that is built utilizing three MG90s microservos, two MG996R microservos, five 10k Ohm Potentiometers, and an ESP32 microcontroller. This project has been built and designed entirely by me with some external inspiration from others robotic arm projects online. To differentiate myself from preexisting projects, I plan to add a second part of this project which will utilize a webcam and OpenCV to sort colored blocks. 

## Overview
This project is my first personal project and has served as a way to learn CAD via Fusion360 and to interact with the Arduino IED before college. This arm will start off by being manually controlled through five potentiometers, but the project will evolve to use the OpenCV software to have the arm "color-sense." Currently, each potentiometer is linked servos controlling the waist, shoulder, elbow, wrist, and gripper respectively. 

## Hardware
Component | Quantity | Purpose
--- | --- | --- 
MG90s Micro Servo | 3 | Joint Rotation
MG996R Micro Servo | 2 | Joint Rotation (Base / Shoulder) 
10k Potentiometer | 5 | Manual Joint Control
ESP32 Microcontroller | 1 | "Brain" (Controls Elements in Circuit)
Electrolytic Capcitor (1000µF) | 1 | Smooths Power Fluctuation

## Software
* Arduino IED - Used to control servos with potentiometers and PWM
* Fusion360 - Used to model and print robotic arm with CAD  

## Wiring


## CAD Design

## Project Phases
### Phase 1 
- [x] Hardware selected and modeled on breadboard
- [x] Potentiometer mapping and servo testing
- [x] Arm modeled in Fusion360
- [ ] Arm 3D printed and assembled
- [x] PCB designed
- [ ] Redesign base and integrate PCB into base

### Phase 2 
- [ ] Webcam mounted in sorting location
- [ ] OpenCV script written in Python
- [ ] ESP32 recieves commands via WiFi
- [ ] Arm autonomously sorts by color

## Challenges / Lessons Learned

### Author
Noah Thompson 
Incoming Engineering Student — Iowa State University, Class of 2030
