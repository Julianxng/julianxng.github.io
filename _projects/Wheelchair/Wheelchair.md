---
layout: post
title: Dual Motor Augmentation for Wheelchair Users
description: A modular motorized conversion kit designed to enhance mobility, affordability, and independence for wheelchair users by repurposing hoverboard components into a universal attachment system.
skills:
  - Assistive Technology
  - Mechanical Design
  - Embedded Systems
  - Motor Control & Robotics
  - Human-Centered Design
  - Rapid Prototyping

main-image: /wheelchair.jpg
---

## Purpose
This project aimed to design and develop a low-cost, modular motorized conversion kit for manual wheelchairs, significantly improving accessibility for users who cannot afford traditional powered wheelchairs. By repurposing hoverboard motors and batteries, the system provides an adaptable, detachable motorized drive unit, reducing the physical strain of manual wheelchair operation.

The design focused on universal compatibility, allowing easy attachment to a wide range of wheelchairs, without requiring professional installation. Customizable control inputs, such as joystick and sip-and-puff interfaces, were considered to cater to users with different mobility needs.

## Key Features
- **Affordability:** Designed to cost under £100, compared to the thousands required for traditional power wheelchairs.
- **Modular Design:** Universally adaptable, using spider joint mechanisms for flexible attachment.
- **Eco-Friendly:** Utilizes recycled hoverboard motors and batteries, reducing electronic waste.
- **Customizable Control:** Can integrate joystick, touchpad, or sip-and-puff controls.
- **Quick Detach Mechanism:** Allows users to **install or remove the motor system in under 60 seconds.

## System Design and Development

### Mechanical Design
The structural system consists of a 3D-printed housing that encases the hoverboard drive unit, preventing pivoting while allowing secure attachment to the wheelchair frame. The system employs spider joints for structural flexibility, making it compatible with different wheelchair models.

### Electronics and Motor Control
Instead of modifying the hoverboard’s original motherboard, custom BLDC motor controllers were used, allowing direct PWM control from a Nucleo F401-RE microcontroller. A joystick provided intuitive user input, and the firmware implemented a differential drive algorithm to control movement.

### Prototyping and Testing
**First Prototype Issues:**
- Initial design had a single support shaft, which caused excessive torque on the axle, leading to failure during on-the-spot turning.

**Final Prototype Improvements:**
- Added dual lateral support shafts, reducing stress and improving stability.
- Increased 3D print infill density for structural components, preventing failure under high loads.
- Optimized motor control firmware to smoothen acceleration and reduce jerking.

## Image Gallery

### 3D CAD model
{% include image-gallery.html images="CAD.png" height="400" %}
Utilising 3 adjustable attachment arms for redundancy, allowing attachment to any wheelchair while also providing a force-resistant connection 

### Hoverboard teardown
{% include image-gallery.html images="breakdown.png" height="400" %}

### Prototyping lab
{% include image-gallery.html images="lab.png" height="400" %}

### Product in use
{% include image-gallery.html images="motion.png" height="400" %}

### Final product
{% include image-gallery.html images="wheelchair.png" height="400" %}

## Challenges and Solutions
- Attachment Stability: Early designs lacked rigidity, but adjustments in structural reinforcement and component positioning resolved these issues.
- Power Constraints: Using a single 36V battery instead of dual units optimized weight and efficiency.
- Terrain Limitations: Carpet testing revealed traction issues, which could be mitigated by using inflated tires and repositioning the drive unit closer to the wheelchair’s center axle.

## Future Improvements
- **Adaptive Controls:** Development of pressure pad sensors or gesture-based control for alternative input methods.
- **Advanced Safety Features:** Implementation of braking systems, stability enhancements, and waterproofing**.
- **Assistive Drive Mode:** Motorized assistance for manual operation, reducing user effort while maintaining control.

## Conclusion
This project demonstrated a working proof-of-concept for a low-cost, universally adaptable motorized wheelchair conversion kit. Within just six weeks of development, the system successfully functioned as intended, highlighting its potential for further development into a commercially viable assistive technology.

