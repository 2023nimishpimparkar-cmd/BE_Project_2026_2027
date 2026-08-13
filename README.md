# BE Capstone Project

## Project Title

**Automatic Bottle Filling Using PLC**

---

## Team Details

| Sr. No. | Name of Student | Roll No. | Branch | Email ID |
|---|---|---|---|---|
| 1 | Ruchika Pandey | 18 | Automation and Robotics | |
| 2 | Nimish Pimparkar | 22 | Automation and Robotics | |
| 3 | Krishna Tikoo | 29 | Automation and Robotics | |
| 4 | | | Automation and Robotics | |

---

## Guide Details

**Project Guide:** Jayshree Ramakrishnan  
**Department:** Automation and Robotics  
**Institute:** VESIT, Mumbai

---

## Problem Statement

The aim of this project is to design and develop an **automated bottle filling and quality inspection system using PLC-based control and OpenCV-based image processing technology**.

Manual bottle filling can result in inconsistent filling levels, water spillage, and human error. The proposed system aims to automate bottle detection, conveyor movement, water filling, and quality inspection with minimal human intervention.

---

## Abstract

Manual bottle filling can lead to inconsistent filling, water spillage, and human error. To overcome these limitations, this project proposes an automated bottle filling system using a Programmable Logic Controller (PLC) and an OpenCV-based quality inspection system.

The PLC controls the conveyor, bottle detection, and water-filling process. A proximity sensor detects the presence of a bottle at the filling position and provides an input to the PLC. The PLC then controls the filling sequence by operating the water pump for a predefined duration. After filling, the bottle is moved to an inspection platform.

A camera captures an image of the filled bottle, and OpenCV-based image processing is used to detect the water level and possible spillage. The detected water level is compared with the required filling range. Based on the inspection result, the bottle is classified as either PASS or FAIL.

The proposed system is expected to provide consistent bottle filling, reduce water spillage and human intervention, and improve the reliability of quality inspection. The system can be used as a prototype for automated bottle-filling and inspection applications.

---

## Objectives

1. To study the existing manual bottle-filling process and its limitations.
2. To design a PLC-based automated bottle-filling system.
3. To develop a conveyor mechanism for automatic bottle movement.
4. To implement bottle detection using a proximity sensor.
5. To control the water pump and filling sequence using PLC.
6. To develop an OpenCV-based vision system for bottle inspection.
7. To detect the water level and possible spillage.
8. To classify the inspected bottles as PASS or FAIL.
9. To integrate the PLC, sensor, conveyor, pump, relay, and camera system.
10. To test and validate the complete system.

---

## Scope of the Project

The project covers the design and development of an automated bottle-filling and inspection prototype.

The scope includes:

- Design and development of a PLC-based control system
- Conveyor-based automatic bottle movement
- Bottle detection using a proximity sensor
- Automatic water filling
- PLC control of the conveyor and water pump
- Relay-based control of the motor and pump
- Camera-based bottle inspection
- OpenCV-based image processing
- Water-level detection
- Spillage detection
- PASS/FAIL classification
- Hardware integration
- Testing and debugging
- Performance analysis and documentation

---

## Existing System

In the existing manual bottle-filling method, bottles are positioned and filled manually. The filling operation and inspection are dependent on human operators.

Manual bottle filling can result in:

- Inconsistent filling levels
- Water spillage
- Human error
- Increased manual intervention
- Difficulty in maintaining consistent quality
- Reduced automation

The project presentation identifies inconsistent filling, spillage, and human error as the major limitations of manual bottle filling.

---

## Proposed System

The proposed system is an **automated PLC-based bottle-filling system integrated with an OpenCV-based quality inspection system**.

### Main Idea

The system automatically detects, fills, and inspects bottles with minimal human intervention.

### Working

1. The conveyor moves the bottle toward the filling position.
2. A proximity sensor detects the bottle.
3. The sensor sends an input signal to the PLC.
4. The PLC controls the conveyor and positions the bottle.
5. The PLC activates the water pump.
6. The bottle is filled for a predefined duration.
7. The pump is switched OFF after the filling sequence.
8. The conveyor moves the filled bottle to the inspection platform.
9. A camera captures the bottle image.
10. OpenCV processes the captured image.
11. The water level and possible spillage are detected.
12. The detected water level is compared with the required filling range.
13. The bottle is classified as PASS or FAIL.

### Major Components

- PLC
- Proximity sensor
- Conveyor
- Conveyor motor
- Water pump
- Relay module
- Power supply
- Camera
- OpenCV image-processing system

### Expected Benefits

- Consistent bottle filling
- Reduced water spillage
- Reduced human intervention
- Automated bottle movement
- Automated quality inspection
- PASS/FAIL classification
- Improved process reliability

---

## System Architecture

The overall system consists of a PLC-based control section and an OpenCV-based inspection section.

```text
                         ┌──────────────────┐
                         │   POWER SUPPLY   │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │       PLC        │
                         │ Control System   │
                         └───────┬───┬──────┘
                                 │   │
                    ┌────────────┘   └─────────────┐
                    │                              │
                    ▼                              ▼
          ┌──────────────────┐           ┌──────────────────┐
          │ Proximity Sensor │           │  Relay Module    │
          │ Bottle Detection │           └────────┬─────────┘
          └────────┬─────────┘                    │
                   │                    ┌─────────┴─────────┐
                   │                    │                   │
                   ▼                    ▼                   ▼
              Bottle              Conveyor Motor       Water Pump
              Detected                 │                   │
                                       ▼                   ▼
                                ┌────────────────────────────┐
                                │     BOTTLE FILLING         │
                                └─────────────┬──────────────┘
                                              │
                                              ▼
                                      ┌───────────────┐
                                      │ Filled Bottle │
                                      └───────┬───────┘
                                              │
                                              ▼
                                      ┌───────────────┐
                                      │   Inspection  │
                                      │    Platform   │
                                      └───────┬───────┘
                                              │
                                              ▼
                                      ┌───────────────┐
                                      │    Camera     │
                                      └───────┬───────┘
                                              │
                                              ▼
                                      ┌───────────────┐
                                      │     OpenCV    │
                                      │Image Processing│
                                      └───────┬───────┘
                                              │
                                  ┌───────────┴───────────┐
                                  │                       │
                                  ▼                       ▼
                         Water Level Detection     Spillage Detection
                                  │                       │
                                  └───────────┬───────────┘
                                              │
                                              
                                      ┌───────────────┐---

## Real-World Applications

### 1. Water Bottling Plants

The proposed system can be used in water bottling plants to automatically detect bottles, fill them to a predefined level, and inspect the filled bottles for incorrect water levels or possible spillage.

### 2. Beverage Industries

The system can be adapted for automated filling of beverages such as juices, soft drinks, and other liquid products by using suitable pumps, filling mechanisms, and sensors.

### 3. Food and Liquid Packaging Industries

The system can be used in food and liquid packaging industries where accurate and repeatable filling of bottles is required along with automated quality inspection.

---

## Advantages

### 1. Reduced Human Intervention

The system automatically performs bottle detection, conveyor movement, filling, and inspection, thereby reducing manual effort.

### 2. Consistent Filling and Inspection

The PLC provides controlled operation of the filling process, while the OpenCV system checks the water level and possible spillage.

### 3. Improved Automation and Efficiency

The integration of PLC, proximity sensor, conveyor, water pump, camera, and OpenCV provides an automated and systematic bottle-filling process.

---

## Disadvantages / Limitations

### 1. Dependence on Sensor and Camera Conditions

The performance of the system depends on proper sensor operation, camera positioning, and suitable lighting conditions during image processing.

### 2. Limited Bottle Compatibility

The prototype is designed for specific bottle dimensions and filling conditions. Different bottle sizes may require changes in the conveyor arrangement, filling mechanism, and OpenCV parameters.

### 3. Initial Cost and Maintenance

The system requires components such as a PLC, conveyor, motor, pump, sensors, relay, and camera. These components increase the initial cost and require periodic maintenance.

---
                                      │   PASS / FAIL │
                                      └───────────────┘
ffg
