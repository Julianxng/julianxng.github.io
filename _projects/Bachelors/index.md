---
layout: post
title: Electroencephalography Neuro-robotics
description: This project focuses on the design and development of a brain-computer interface (BCI) system that enables the control of a robotic arm through neural activity. The project required expertise in neuroengineering, signal processing, machine learning, and robotics to achieve accurate and reliable control.
skills:
  - Brain-Computer Interface (BCI)
  - Biological Signal Processing
  - Machine Learning
  - Neuroengineering
  - Robotics Control
  - Data Analysis

main-image: /main2.png
---

## Purpose
The aim of this research was to develop a brain-computer interface that enables individuals to control a robotic manipulator using their thoughts. This project explores the potential of neurotechnology to create assistive systems for individuals with motor impairments.

The system leverages electroencephalography (EEG) signals to classify motor imagery tasks and convert them into control commands for a robotic arm. This research aims to advance the accessibility of BCI technologies through cost-effective solutions with minimal hardware.

This page contains a breif oversight of an incredibly complex project, full details can be found in the original paper [here](https://drive.google.com/file/d/1VCVjxGq2CqPOhzUSwDlBgPKRQxJnPFXn/view?usp=drive_link)


## Key Objectives
- Capture and process EEG signals accurately.
- Classify motor imagery tasks with high accuracy.
- Develop a real-time control system for a robotic manipulator.
- Enhance accessibility of BCI systems with low-cost hardware.

## System Design and Development

### EEG Signal Acquisition
EEG data was collected using a medical-grade EEG device with bipolar electrodes. Signals were filtered using band-pass and notch filters to remove noise and artifacts.

### Signal Processing and Feature Extraction
The project implemented techniques such as:
- **Band-pass Filtering:** To isolate relevant frequency bands.
- **Common Spatial Patterns (CSP):** For feature enhancement.
- **Logarithm of Variance:** To extract significant features for classification.

### Machine Learning
Linear Discriminant Analysis (LDA) was employed for classifying motor imagery tasks. The model achieved an accuracy of 81.25% in differentiating between left and right-hand motor imagery tasks.
A Convolutional neural network was also developed, yet deemed unsuitable for real-time control.

### Robotic Control System
The classified EEG signals were mapped to control commands for a UR10 robotic arm. The system demonstrated real-time responsiveness and reliable control performance.

## Image Gallery

### Neurophysiological input
{% include image-gallery.html images="motor_imagery.png" height="400" %}
I leveraged the neurological phenomena known as 'motor imagery'. When a subject imagines moving their left or right hand, a spike of activity can be observed in the opposite side of the motor cortex, this is termed 'contralateral desynchronisation' and is exclusively observed within the 
alpha (8-12 Hz) and the beta rhythm (13-30 Hz) bands. 

### EEG Signal Acquisition Setup
{% include image-gallery.html images="architecture.png" height="400" %}
EEG signals were captured with two bipolar electrodes using an ADinstruments 26T powerlab device, fed into their proprietary software 'labchart' for which I wrote a custom sdk to import their encrypted files into python, where I processed them using the Scipy library and generated robotic commands to send to the UR10 

### Biological data capture
{% include image-gallery.html images="Data_capture.png" height="400" %}
I could not just press record and imagine left and right-hand movements for set periods of time, as the act of pre-empting when the next
signal is, and what it will be, affects the 'accuracy' or reliability of the right/left-hand signal I am creating.
To do it properly, I must create a structured yet randomised cue-based trial that would tell me what hand
to imagine moving and would tell me so at random intervals. I used software called PychoPy, typically
used in psychological examinations and studies.

### Alpha and beta spikes
{% include image-gallery.html images="PSD.png" height="400" %}
This diagram displays a signal's mean-square amplitude, or “power,” across a frequency spectrum. We can observe clear spikes indicating motor imagery behaviour.

### Contralateral descyncronisation
{% include image-gallery.html images="ERD_proof.png" height="400" %}
the top 'c3' channel has been filtered, it represents the left motor cotrex. We can observe event-related desynchronisation (ERD) through an increase in signal amplitude during the right hand movements (orange bars) and a decrease during left hand movements (blue bars)

### Signal extraction
{% include image-gallery.html images="Alpha+beta.png" height="400" %}
As the raw EEG signals encompasses the full spectrum of 0-100Hz alongside alot of noise and signal artifacts (non-neurological signals) they must be heavily processed to extract the alpha and beta waves that represent the control input. this was achieved using a band pass filter and a common spatial patterns algorithm.

### Common spatial patterns 
{% include image-gallery.html images="CSP.png" height="400" %}
To classify the data, The frequency information had to be represented in a suitable way to create the
feature vector. The first action was to calculate the logarithm of the variance in the band passed signals
activity for each channel. Below we see a bar chart plot of this logarithm, where each pair of bars
correspond to a channel. The blue and red of each channel represent the left- and right-hand trials.
We can see a small difference in the log-var of the left- and right-hand trials for both channels, The CSP
algorithm calculates mixtures of the channel components that are designed to maximise the difference in
variation between two classes. These mixtures are the spatial filters.

### Classification
{% include image-gallery.html images="scatter2.png" height="400" %}
After the CSP algorithm is applied, it is clear that it has maximised and minimised the variance of the two
classes. I now have two mixtures of classes, which are called components, and are created by two spatial
filters. The classification algorithm shall be a linear discriminant analysis (LDA). Therefore, the trials
will be represented as a scatter plot with the x-axis being the trials logarithm of the variance values with
the first CSP component, and the y-axis being their values with the last CSP component.

## Challenges and Solutions
- **Signal Noise and Artifacts:** Implemented robust filtering techniques to improve signal quality.
- **Classification Accuracy:** Enhanced model performance through feature optimization.
- **Real-Time Control Latency:** Optimized system architecture for reduced processing delays.

## Key Achievements
- Successfully developed a functional BCI system with real-time robotic control.
- Achieved classification accuracy of over 81% using minimal hardware.
- Demonstrated potential applications in assistive technologies for individuals with disabilities.

## Technologies Used
- **EEG Hardware:** Medical-grade EEG device
- **Programming Languages:** Python, MATLAB
- **Machine Learning:** Linear Discriminant Analysis (LDA)
- **Robotics:** UR10 robotic arm

## Conclusion
This project demonstrates the feasibility of using EEG signals for real-time control of robotic systems. It highlights the potential of BCI technologies in developing assistive devices and opens avenues for future research in neuroprosthetics and neurorehabilitation.
