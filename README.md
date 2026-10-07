# BE Capstone Project

## Project Title

**PLC based Automatic Bottle filling with AI-based Quality Inspection**

---

## Team Details

| Sr. No. | Name of Student | Roll No. | Branch | Email ID |
|---|---|---|---|---|
| 1 | Ruchika Pandey | 18 | Automation and Robotics | |
| 2 | Nimish Pimparkar | 22 | Automation and Robotics | |
| 3 | Krishna Tikoo | 29 | Automation and Robotics | |


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

1. To study the existing manual bottle-filling and inspection process and its limitations. 
2. To design and develop a PLC-based automated bottle-filling system. 
3. To develop a conveyor mechanism for automatic bottle movement and positioning. 
4. To implement bottle detection using a proximity sensor. 
5. To control the conveyor, water pump, and filling sequence using the PLC. 
6. To develop a camera-based bottle inspection system using YOLO and OpenCV. 
7. To detect damaged, cracked, or deformed bottles using the YOLO-based AI model. 
8. To detect the water level in the filled bottle using OpenCV. 
9. To detect visible water spillage around the bottle using OpenCV-based image 
processing. 
10. To classify bottles based on inspection results as PASS or FAIL / GOOD or 
DEFECTIVE. 
11. To provide a red-light indication when a defective bottle or filling-related problem is 
detected. 
12. To integrate the PLC automation, sensor, conveyor, pump, camera, AI, and inspection 
system and validate the complete prototype. 

## Scope of the Project

Small-scale prototype: Develop a low-cost automated bottle filling and inspection system for academic and demonstration purposes.
Bottle handling: Automate bottle movement and positioning using a conveyor and PLC.
Water filling: Control the water-filling process using a PLC and pump.
Bottle inspection: Use a camera to inspect the bottle before and after filling.
Defect detection: Use YOLO to identify common bottle defects such as damage or deformation.
Water-level detection: Use OpenCV to identify LOW, CORRECT, or HIGH water levels.
Spillage detection: Use OpenCV to detect visible water spillage around the bottle.
Quality decision: Generate a basic PASS/FAIL result based on inspection.
Controlled testing: Test the system under controlled lighting and operating conditions.
Integration: Demonstrate the integration of PLC-based industrial automation and computer vision in a low-cost prototype.

## Existing System

Manual Handling: Bottles are manually handled, positioned, filled, and inspected.
This increases human effort and can reduce process efficiency.

Manual Inspection: Bottle defects, water level, and spillage are mainly checked by people.
This can result in missed defects and inconsistent quality decisions.

# Major Component

Part 1 – PLC-Based Bottle Filling Automation
| Component                       |    Quantity | Purpose                      |
| ------------------------------- | ----------: | ---------------------------- |
| Siemens S7-1200 PLC (CPU 1212C) |           1 | Main control unit            |
| 24V DC SMPS                     |           1 | PLC/control power supply     |
| DC Geared Motor                 |           1 | Conveyor drive               |
| Conveyor Belt                   |           1 | Bottle transportation        |
| Reflective/Proximity IR Sensor  |           1 | Bottle detection             |
| 24V DC Mini Water Pump          |           1 | Water filling                |
| Relay Module, 24V DC SPDT       |           3 | Switching motor/pump loads   |
|     Water Tank/Reservoir        |           1 | Water storage                |
| Connecting wires                | As required | Electrical connections       |
| Push Buttons                    | As required | Start/Stop control           |
| Emergency Stop                  |           1 | Safety                       |
| Supporting mechanical structure | As required | Conveyor/filling arrangement |

Part 2 – AI-Based Bottle Inspection
| Component                               |    Quantity | Purpose                       |
| --------------------------------------- | ----------: | ----------------------------- |
| Zebronics Zeb-Crystal Clear 480p Webcam |           1 | Bottle image/video capture    |
| Acer Aspire Lite AL15-41 Laptop         |           1 | AI processing                 |
| XCLUMA 5V USB 2-Channel Relay           |           1 | Red LED switching             |
| 12V Red LED Indicator                   |           1 | Defective bottle indication   |
| 12V DC Adapter                          |           1 | Red LED power                 |
| White LED/Light Source                  |         1–2 | Controlled illumination       |
| Bottle Samples                          |    Multiple | YOLO training/testing         |
| Inspection Tray/Background              |           1 | Controlled vision environment |
| USB and connecting wires                | As required | Connections                   |

| Software           | Purpose                             |
| ------------------ | ----------------------------------- |
| Python 3.14.3      | Programming                         |
| Visual Studio Code | Development environment             |
| OpenCV             | Water-level and spillage inspection |
| Ultralytics YOLO   | Bottle defect detection             |
| NumPy              | Image/data processing               |

### PLC I/0 List
Prepare a table containing:
| Tag No. | Description             | Type | Signal | Address |
| ------- | ----------------------- | ---- | ------ | ------- |
| DI-01   | Start Push Button       | DI   | NO     | I0.0    |
| DI-02   | Stop Push Button        | DI   | NC     | I0.1    |
| DI-03   | Bottle Detection Sensor | DI   | NO/NC  | I0.2    |
| DO-01   | Conveyor Motor          | DO   | —      | Q0.0    |
| DO-02   | Water Pump              | DO   | —      | Q0.1    |

### Working

Step-by-Step Procedure
Step 1 – System Start
The PLC starts the conveyor and initiates the bottle-handling sequence.

Step 2 – Bottle Arrival
An empty bottle moves on the conveyor toward the first inspection position.

Step 3 – Bottle Positioning
The bottle moves slightly and is positioned in front of the fixed camera for proper inspection.

Step 4 – Bottle Inspection Using YOLO
The camera captures the bottle image and sends it to the YOLO AI model.
YOLO checks whether the bottle is:
Good
Damaged
Deformed

Step 5 – Bottle Quality Decision
Good Bottle: No indicator light is activated, and the bottle continues toward the filling station.
Damaged/Defective Bottle: The red LED turns ON to indicate the defect, and the bottle is prevented from proceeding to the filling operation.

Step 6 – Transfer to Filling Station
The good bottle continues on the conveyor and reaches the water filling station.

Step 7 – Bottle Positioning at Filling Station
The PLC positions the bottle correctly below the filling nozzle and controls the conveyor movement.

Step 8 – Water Filling
The PLC activates the water pump and fills the bottle for a predefined duration.

Step 9 – Filling Completion
After the preset filling time, the PLC switches the pump OFF.

Step 10 – Post-Filling Inspection
The filled bottle moves to the camera inspection position. The same camera is used for the second inspection.

Step 11 – Water-Level Detection Using OpenCV
OpenCV analyzes the bottle image and determines the water level as:
LOW
CORRECT
HIGH

Step 12 – Spillage Detection Using OpenCV
OpenCV also examines the area around the bottle to detect visible water spillage.

Step 13 – Final Quality Decision
The inspection results are evaluated:
Correct water level + No spillage → PASS / GOOD
Low/High water level or Spillage → FAIL / DEFECTIVE

Step 14 – End Point
After the inspection, the bottle continues to the end point of the conveyor, where the PLC stops the conveyor.

### SYSTEM ARCHITECTURE
                    SYSTEM ARCHITECTURE
                           │
                           ▼
                  ┌─────────────────┐
                  │   START / STOP  │
                  │   Push Buttons  │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │      PLC        │
                  │  Control Unit   │
                  └────────┬────────┘
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
       ┌──────────┐  ┌──────────┐  ┌────────────┐
       │ Conveyor │  │  Bottle  │  │   Water    │
       │  Motor   │  │  Sensor  │  │    Pump    │
       └────┬─────┘  └──────────┘  └──────┬─────┘
            │                             │
            ▼                             ▼
       Bottle Movement              Water Filling
            │                             │
            └─────────────┬───────────────┘
                          ▼
                ┌───────────────────┐
                │  Camera Inspection│
                │     (USB Camera) │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │      Laptop       │
                │ Python + OpenCV   │
                │     + YOLO        │
                └─────────┬─────────┘
                          │
             ┌────────────┴────────────┐
             ▼                         ▼
       ┌─────────────┐          ┌──────────────┐
       │ YOLO Defect │          │ OpenCV Level │
       │ Detection   │          │ & Spillage   │
       └──────┬──────┘          └───────┬──────┘
              │                         │
              └──────────┬──────────────┘
                         ▼
                ┌───────────────────┐
                │   PASS / FAIL     │
                │ Quality Decision  │
                └─────────┬─────────┘
                          │
                    ┌─────┴─────┐
                    ▼           ▼
                GOOD BOTTLE   DEFECTIVE
                    │           │
                    ▼           ▼
                Continue     Red LED ON
                Process




                                   
