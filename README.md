# Active Drag System

## Table of Contents
- [Introduction](#introduction)
- [Flight Software](#flight-software)
- [PCB Design](#pcb-design)
- [OpenRocket](#openrocket)
- [CAD](#cad)
- [Installation](#installation)

## Introduction
This project is focused on the development of an active drag system, or air brake, for a model rocket competing in the NASA Student Launch competition (https://www.nasa.gov/learning-resources/nasa-student-launch/). This work was done on a non-competition vehicle as its advancements are intended to be used in future years' competitions.
This project demonstrates the designs of the various components, including the flight software, printed circuit board (PCB), OpenRocket analysis for the vehicle, and CAD drawings for the system. 
Due to time constraints and a focus on the main competition vehicle, the non-competition vehicle was never flown with an active drag system installed.

## Flight Software
### Overview
The `Arduino Codes` directory contains the code necessary for controlling the vehicle's Active Drag System. This system adjusts the vehicle's drag tabs based on readings from an altimeter and accelerometer to control the vehicle's apogee. The system is controlled before launch using a Bluetooth module that can connect to a user's phone, allowing for the constant monitoring of flight readiness once the system is installed in the vehicle. Data is redundantly saved to an onboard flash memory chip and SD for storage and post-flight analysis.

### Block Diagram
![Flight Software](Arduino%20Codes/blockDiagram.png)

### Description
The flight software implements a state machine to manage the deployment of drag tabs in the Active Drag System. This system actively modulates the drag during flight to achieve a desired apogee by processing real-time data from the altimeter and accelerometer. The state machine ensures that the drag tabs are deployed or retracted based on the vehicle's altitude and acceleration, thus controlling the peak altitude accurately.

## PCB Design
### Overview
The `PCB Design` directory contains all the files related to the design and manufacturing of the vehicle's printed circuit boards (PCBs). These PCBs are used to integrate the electronic components necessary for the vehicle's operation.

### Images
![Top Layer](PCB%20Design/Images/topLayer.png)
![Bottom Layer](PCB%20Design/Images/bottomLayer.png)
![Schematic](PCB%20Design/Images/schematic.png)

### Description
PCB design is crucial for ensuring that the electronic components are connected properly. The files in this directory include design files, Gerber files for manufacturing, libraries for making the schematics, and images showing different layers and the schematic of the PCB. 

## OpenRocket
### Overview
The `OpenRocket` directory contains simulation files for the vehicle. These files can be used to simulate the vehicle's flight characteristics and performance.

### Images
![Vehicle Design](OpenRocket/Design.png)
![Flight Simulation](OpenRocket/FlightSim.png)

### Description
OpenRocket is a model rocket simulator that allows you to design and simulate the performance of rockets. The model in this directory represents the vehicle design as well as detailed simulations that help in predicting the flight path, stability, and performance of the vehicle.

## CAD
### Overview
The `CAD` directory contains the design files for the system's structural components. This model was created in SolidWorks, and the files can be used to fabricate the parts using 3D printing.

### Images
![CAD Design](CAD/pic1.PNG)
![CAD Design](CAD/pic2.PNG)
![CAD Design](CAD/pic3.PNG)
![CAD Design](CAD/pic4.PNG)
![CAD Design](CAD/built.jpg)

### Description
FEA (finite element analysis) and CFD (computational fluid dynamics) were performed on the system to evaluate both its structural integrity and effectiveness as a braking system.

## Installation
To install the software and code for this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/will-becht/Active-Drag-System