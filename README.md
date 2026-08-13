# BE Capstone Project

## Project Title

**Automatic Bottle Filling Using PLC**

---

## Team Details

| Sr. No. | Name of Student  | Roll No. | Branch                  | Email ID |
| ------- | ---------------- | -------- | ----------------------- | -------- |
| 1       | Ruchika Pandey   | 18       | Automation and Robotics |          |
| 2       | Nimish Pimparkar | 22       | Automation and Robotics |          |
| 3       | Krishna Tikoo    | 29       | Automation and Robotics |          |
| 4       |                  |          | Automation and Robotics |          |

---

## Guide Details

**Project Guide:** Jayshree Ramakrishnan
**Department:** Automation and Robotics
**Institute:** VESIT, Mumbai

---

## Problem Statement

Manual bottle filling can result in inconsistent filling levels, water spillage, and human error. There is a need for an automated bottle-filling system that can accurately detect bottles, control the filling process, and inspect the filled bottles with minimal human intervention.

The aim of this project is to design and develop an **automatic bottle filling and inspection system using PLC-based control and OpenCV-based quality inspection**. The system will automate the conveyor movement, bottle detection, water filling, and quality inspection process.

---

## Abstract

Manual bottle filling is a time-consuming process that can lead to inconsistent filling levels, water spillage, and human error. To overcome these limitations, this project proposes an automated bottle filling system using a Programmable Logic Controller (PLC) along with an OpenCV-based quality inspection system.

The PLC controls the major operations of the system, including the conveyor, bottle detection, and water pump. A proximity sensor detects the presence of a bottle at the filling position and triggers the filling sequence for a predefined duration. After filling, a camera captures an image of the bottle at the inspection platform. OpenCV-based image processing is then used to determine the water level and detect possible spillage.

The detected water level is compared with the required filling range, and the bottle is classified as either **PASS or FAIL** based on the inspection result. The proposed system aims to provide consistent bottle filling, reduce manual intervention, minimize spillage, and improve quality control.

The project can be applied to automated bottle-filling and inspection processes where reliable and repeatable operation is required.

---

## Objectives

1. To study the existing manual bottle-filling process and its limitations.
2. To design a PLC-based automated bottle-filling system.
3. To develop a conveyor system for automatic bottle movement and positioning.
4. To implement bottle detection using a proximity sensor.
5. To control the water pump and filling process using PLC programming.
6. To develop an OpenCV-based vision system for water-level and spillage detection.
7. To classify bottles as PASS or FAIL based on the inspection results.
8. To integrate the PLC, sensor, conveyor, pump, relay, and vision system.
9. To test and validate the complete automated system.
10. To document the project and its results.

---

## Scope of the Project

The project covers the design and development of an automated prototype for bottle filling and quality inspection.

The scope includes:

* Design and development of a PLC-based control system.
* Automatic conveyor-based bottle movement.
* Bottle detection using a proximity sensor.
* Automatic control of the water pump.
* Filling bottles for a predefined time.
* Integration of PLC hardware and control components.
* Camera-based bottle inspection.
* OpenCV-based water-level detection.
* Detection of possible water spillage.
* PASS/FAIL classification of bottles.
* Testing and debugging of the complete system.
* Performance evaluation and project documentation.

---

## Existing System

In a conventional manual bottle-filling process, bottles are positioned and filled manually. The operator is responsible for controlling the filling operation and checking the filled bottles.

This method can result in:

* Inconsistent water levels.
* Water spillage during filling.
* Human error.
* Increased manual intervention.
* Difficulty in maintaining consistent quality.
* Reduced process automation.

The uploaded project material specifically identifies inconsistent filling, spillage, and human error as key problems associated with manual bottle filling.

---

## Proposed System

The proposed system is an **automated PLC-based bottle filling and OpenCV-based inspection system**.

The system uses a conveyor to move bottles automatically. A proximity sensor detects when a bottle reaches the filling position and sends a signal to the PLC. The PLC then controls the filling sequence and operates the water pump for a predefined period.

After filling, the bottle is moved to an inspection platform where a camera captures its image. OpenCV processes the captured image to determine the water level and detect possible spillage. The detected water level is compared with the required filling range. Based on the inspection result, the bottle is classified as **PASS or FAIL**.

### Major Components

* PLC
* Proximity sensor
* Conveyor system
* Conveyor motor
* Water pump
* Relay module
* Power supply
* Camera
* OpenCV-based image-processing system

The PLC, sensor, conveyor, pump, relay, and power supply have already been identified as the main hardware components.

### Working Principle

1. The conveyor moves the bottle toward the filling position.
2. The proximity sensor detects the bottle.
3. The sensor sends an input signal to the PLC.
4. The PLC stops/positions the conveyor and activates the water pump.
5. The bottle is filled for a predefined duration.
6. The pump is switched off after the filling sequence.
7. The conveyor moves the filled bottle to the inspection platform.
8. A camera captures the filled bottle.
9. OpenCV processes the captured image.
10. The system determines the water level and checks for spillage.
11. The water level is compared with the required filling range.
12. The bottle is classified as **PASS** or **FAIL**.

The vision-inspection flow is:

**Camera → Image Processing → Level & Spillage Detection → PASS/FAIL**

---

## System Architecture

```text
                    ┌──────────────────────┐
                    │      Power Supply    │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │         PLC          │
                    │  Control & Sequence  │
                    └───────┬───────┬──────┘
                            │       │
              ┌─────────────┘       └──────────────┐
              ▼                                    ▼
    ┌──────────────────┐                 ┌──────────────────┐
    │ Proximity Sensor │                 │   Relay Module   │
    │ Bottle Detection │                 └───────┬──────────┘
    └────────┬─────────┘                         │
             │                         ┌─────────┴─────────┐
             ▼                         ▼                   ▼
       Bottle Detected          Conveyor Motor        Water Pump
             │                         │                   │
             └─────────────────────────┴───────────────────┘
                                       │
                                       ▼
                              ┌─────────────────┐
                              │ Filled Bottle   │
                              │ Inspection Area │
                              └────────┬────────┘
                                       │
                                       ▼
                              ┌─────────────────┐
                              │      Camera     │
                              └────────┬────────┘
                                       │
                                       ▼
                              ┌─────────────────┐
                              │     OpenCV      │
                              │ Image Processing│
                              └────────┬────────┘
                                       │
                         ┌─────────────┴─────────────┐
                         ▼                           ▼
                 Water Level Detection        Spillage Detection
                         │                           │
                         └─────────────┬─────────────┘
                                       ▼
                              ┌─────────────────┐
                              │   PASS / FAIL   │
                              └─────────────────┘
```

---

## Current Project Status

The PLC control architecture for the conveyor and water pump has been finalized, including the required inputs, outputs, and operating sequence. The required components have also been identified.

The bottle detection sensor has been selected, and a relay module has been selected for safe control of the conveyor motor and water pump. Basic PLC ladder logic for start/stop, bottle detection, conveyor operation, and pump control has been developed. PLC programming, hardware integration, and component testing are currently in progress.

---

## Expected Outcome

The expected outcome of the project is a working automated bottle-filling prototype capable of:

* Automatically detecting bottles.
* Automatically positioning bottles using a conveyor.
* Controlling the filling process using a PLC.
* Filling bottles for a predefined duration.
* Detecting water level using OpenCV.
* Detecting possible water spillage.
* Classifying bottles as PASS or FAIL.
* Reducing manual intervention.
* Improving filling consistency and quality inspection.

---

## Project Timeline

| Activity                             | Target         |
| ------------------------------------ | -------------- |
| Finalize Project Design & Components | April 2026     |
| Research Started                     | July 2026      |
| Procure Required Components          | August 2026    |
| Build Conveyor & Filling Mechanism   | September 2026 |
| Develop PLC Program                  | September 2026 |
| Integrate Sensor, Pump & Conveyor    | October 2026   |
| Develop OpenCV Bottle Detection      | October 2026   |
| Complete Testing & Debugging         | November 2026  |
| Final Demonstration & Documentation  | November 2026  |

The timeline is based on the milestone schedule provided in the project presentation.

**Department:** Automation and Robotics  
**Institute:** VESIT, Mumbai  

---

## Problem Statement

Write a clear problem statement here.

Example:

> The aim of this project is to design and develop a system that solves the problem of __________ by using __________ technology.

---

## Abstract

Write a short summary of the project in 150–250 words.

The abstract should include:

- Background of the problem
- Proposed solution
- Technology used
- Expected outcome
- Application area

---

## Objectives

1. To study the existing problem and available solutions.
2. To design a suitable hardware/software/system architecture.
3. To implement the proposed solution.
4. To test and validate the system.
5. To document and publish the project work.

---

## Scope of the Project

Mention what the project will cover.

Example:

- Design and development of prototype
- Hardware implementation
- Software/mobile/web interface
- Data collection and testing
- Performance analysis

---

## Existing System

Describe the currently available system or method.

Mention its limitations:

- High cost
- Low accuracy
- Manual process
- Lack of automation
- Poor scalability
- Limited accessibility

---

## Proposed System

Describe your proposed solution.

Include:

- Main idea
- How it works
- Major components
- Expected benefits

---

## System Architecture

Add block diagram or system architecture image here.

```markdown
![System Architecture](images/system_architecture.png)
````

Briefly explain the architecture.

---

## Hardware Requirements

| Sr. No. | Component | Specification | Quantity | Purpose |
| ------- | --------- | ------------- | -------- | ------- |
| 1       |           |               |          |         |
| 2       |           |               |          |         |
| 3       |           |               |          |         |
| 4       |           |               |          |         |

---

## Software Requirements

| Sr. No. | Software / Tool | Version | Purpose |
| ------- | --------------- | ------- | ------- |
| 1       |                 |         |         |
| 2       |                 |         |         |
| 3       |                 |         |         |

---

## Technologies Used

Mention technologies used in the project.

Example:

* Embedded C / Python / JavaScript
* Arduino / STM32 / ESP32 / Raspberry Pi
* ROS / MATLAB / Simulink
* Machine Learning / Computer Vision
* IoT / Cloud / Mobile App
* PCB Design / CAD Design

---

## Methodology

Explain the step-by-step approach.

1. Literature survey
2. Problem identification
3. Requirement analysis
4. System design
5. Hardware/software development
6. Integration
7. Testing and validation
8. Documentation and publication

---

## Project Timeline

| Week / Month | Task Planned          | Status                            |
| ------------ | --------------------- | --------------------------------- |
| Week 1       | Problem finalization  | Pending / In Progress / Completed |
| Week 2       | Literature survey     |                                   |
| Week 3       | Requirement analysis  |                                   |
| Week 4       | System design         |                                   |
| Week 5       | Prototype development |                                   |
| Week 6       | Testing               |                                   |
| Week 7       | Documentation         |                                   |
| Week 8       | Paper writing         |                                   |

---

## Weekly Progress Updates

Students must update this section every week.

| Week   | Date | Work Completed | Work Planned for Next Week | Issues / Challenges | GitHub Commit Link |
| ------ | ---- | -------------- | -------------------------- | ------------------- | ------------------ |
| Week 1 |      |                |                            |                     |                    |
| Week 2 |      |                |                            |                     |                    |
| Week 3 |      |                |                            |                     |                    |
| Week 4 |      |                |                            |                     |                    |
| Week 5 |      |                |                            |                     |                    |
| Week 6 |      |                |                            |                     |                    |
| Week 7 |      |                |                            |                     |                    |
| Week 8 |      |                |                            |                     |                    |

---

## Design Files

Upload and link all design files here.

| File Type       | File Name / Link | Description |
| --------------- | ---------------- | ----------- |
| CAD Model       |                  |             |
| Circuit Diagram |                  |             |
| PCB Design      |                  |             |
| Flowchart       |                  |             |
| Simulation File |                  |             |

---

## Circuit Diagram

Add circuit diagram image here.

```markdown
![Circuit Diagram](images/circuit_diagram.png)
```

---

## Flowchart / Algorithm

Add flowchart image here.

```markdown
![Flowchart](images/flowchart.png)
```

### Algorithm

1. Start
2. Initialize the system
3. Read input from sensors/user
4. Process the data
5. Generate output/control action
6. Display/store/transmit result
7. Stop

---

## Implementation Details

Explain the actual implementation of the project.

### Hardware Implementation

Write details about connections, components, power supply, sensors, actuators, PCB, enclosure, etc.

### Software Implementation

Write details about code structure, libraries used, algorithms, communication protocols, database, app, cloud, etc.

---

## Code Structure

```text
BE-Capstone-Project/
│
├── README.md
├── docs/
│   ├── literature_survey.md
│   ├── project_report.pdf
│   └── presentation.pptx
│
├── hardware/
│   ├── circuit_diagram.png
│   ├── pcb_design/
│   └── cad_model/
│
├── software/
│   ├── src/
│   ├── include/
│   └── tests/
│
├── images/
│   ├── system_architecture.png
│   ├── prototype_photo.jpg
│   └── results.png
│
└── references/
    └── papers/
```

---

## How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/username/project-name.git
```

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

or mention specific software/library installation steps.

### Step 3: Upload / Run the Code

```bash
python main.py
```

or

```bash
arduino-cli upload -p COMx --fqbn board_name
```

### Step 4: Observe the Output

Mention the expected output of the project.

---

## Testing and Results

| Test No. | Test Description | Expected Result | Actual Result | Status      |
| -------- | ---------------- | --------------- | ------------- | ----------- |
| 1        |                  |                 |               | Pass / Fail |
| 2        |                  |                 |               | Pass / Fail |
| 3        |                  |                 |               | Pass / Fail |

---

## Result Images / Videos

Add images or videos of the working prototype.

```markdown
![Prototype](images/prototype_photo.jpg)
```

Video Link:

```markdown
[Project Demo Video](https://drive.google.com/your-video-link)
```

---

## Applications

Mention real-world applications of the project.

1.
2.
3.
4.

---

## Advantages

1.
2.
3.
4.

---

## Limitations

1.
2.
3.
4.

---

## Future Scope

Mention possible improvements.

1.
2.
3.
4.

---

## Research Paper / Publication

| Item                      | Details                                                   |
| ------------------------- | --------------------------------------------------------- |
| Paper Title               |                                                           |
| Conference / Journal Name |                                                           |
| Paper Status              | Not Started / Drafting / Submitted / Accepted / Published |
| Submission Date           |                                                           |
| Paper Link                |                                                           |

---

## References

Add references in IEEE format.

Example:

```text
[1] A. Author, B. Author, "Title of the Paper," Journal/Conference Name, vol. X, no. Y, pp. xx-yy, Year.
[2] Datasheet / Website / Book reference.
```

---

## Repository Update Guidelines

Each student team must update the GitHub repository regularly.

Minimum expected updates:

* Update README every week.
* Push code changes regularly.
* Upload circuit diagrams, CAD files, PCB files, reports and presentations.
* Add weekly progress in the progress table.
* Maintain proper folder structure.
* Do not upload unnecessary temporary files.
* Each major update should have a meaningful commit message.

Example commit messages:

```text
Added problem statement and objectives
Updated system architecture diagram
Added sensor interfacing code
Updated weekly progress for Week 3
Added testing results and prototype images
```

---

## Declaration

We declare that this project work is carried out by our team as part of the BE Capstone Project. The work will be regularly updated on GitHub and all references used will be properly cited.

---

## License

This project is for academic use only.

Optional:

```text
MIT License / Creative Commons / Institute Use Only
```

```
```
