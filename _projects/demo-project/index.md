---
layout: post
title: Advanced Dexterous Prosthetic Hand Development
description: This project focuses on the design and development of an advanced dexterous robotic hand, aiming to replicate the complex motion and functionality of a human hand. The project required expertise in mechanical design, embedded systems, control algorithms, and human-centered design to achieve high precision and functionality.
skills:
  - Mechanical Design
  - Embedded Systems
  - Control Algorithms
  - Inverse Kinematics
  - Human-Centered Design
  - Prototyping & Fabrication
  - Biomechanical Simulation

main-image: /Bitilda1.png
---

## Purpose
The development of an advanced dexterous prosthetic hand was undertaken to explore the limits of biomimetic robotics. This project involved replicating the intricate structure, range of motion, and dynamic control of the human hand using custom-designed mechanical linkages, embedded systems, and sophisticated control algorithms.

## Key Objectives
- Replicate human-like dexterity and motion.
- Achieve real-time control for complex finger movements.
- Optimize for compact form factor and lightweight design.
- Integrate robust control algorithms for precise actuation.

## Design and Development
### Mechanical Design
The hand features a complex linkage mechanism replicating the natural biomechanics of human fingers. Utilizing SolidWorks for CAD modeling, stress analysis was conducted to ensure structural integrity under dynamic loads.

### Embedded Systems
Microcontrollers (Arduino and STM32) were employed to manage the control of 15 motors, encoders, and drivers, ensuring real-time response and precision.

### Control Algorithms
The control system integrates inverse kinematics models to map finger joint positions accurately. The algorithms handle real-time feedback for smooth and coordinated finger movements.

### Prototyping & Fabrication
The hand was prototyped using 3D printing technologies (FDM and PolyJet) and assembled with precision components to maintain the delicate balance between durability and lightweight design.

## Image Gallery

### Linkage Mechanism Architecture

{% include image-gallery.html images="architecture.png" height="400" %}

(a) Exploded view. (b) Un-exploded view. (c) Full design with representation of virtual human joints. (d) Annotated main components list


### Kinematic structure of the finger

{% include image-gallery.html images="Kinematics.png" height="400" %}


### Relationship between Prismatic displacement and finger pose 

{% include image-gallery.html images="displacements.png" height="400" %}

(a) Home position. (b) MCP abduction/adduction. (c) MCP flexion/extension. (d) PIP + DIP
flexion/extension. (e) MCP + PIP + DIP flexion/extension. (f) MCP + PIP + DIP flexion/extension and
simultaneous abduction/adduction


### Custom electromechanical components

{% include image-gallery.html images="blowup.png" height="400" %}

(a) Exploded view of functional components. (b) annotated list relative to hand size


### Grasp types achievable by the Bi-TILDA

{% include image-gallery.html images="Bitilda1.png" height="400" %}

(a) Power grasp (b) Delicate fingertip
grasp of large object. (c) Power grasp using only two thumbs and middle finger. (d) Pinch grasp of
medium sized object. (e) Precision grasp of small, thin object. (f) Delicate precision grasp.


### Camera based tele-operation control

{% include image-gallery.html images="Teleoperation.png" height="400" %}

Tracks fingertip coordinates in cartesian space and maps it to motor positions through a complex inverse kinematics solver


### Workspace comparison

{% include image-gallery.html images="workspace.png" height="400" %}

Comparative analysis of reachable workspace and Inter-digit overlap, showing that the two thumb achitecture provides a larger field of precise dexterity through redundancy


## Challenges and Solutions
- **Complex Kinematic Modeling:** Solved through iterative design and simulation.
- **Power and Space Constraints:** Optimized PCB layout and efficient wiring solutions.
- **Precision Control:** Advanced PID control loops for stable performance.

## Key Achievements
- Successfully developed a functional, dexterous robotic hand with high fidelity to human hand movements.
- Demonstrated real-time control of individual fingers with coordinated gestures.

## Technologies Used
- **CAD Tools:** SolidWorks
- **Microcontrollers:** Arduino, STM32
- **Programming Languages:** Python, C++
- **Prototyping:** 3D Printing (PolyJet, FDM), CNC Machining

## Conclusion
This project showcases the integration of mechanical, electronic, and software engineering to create a sophisticated robotic system. It stands as a testament to the potential of interdisciplinary approaches in advancing assistive technologies.
