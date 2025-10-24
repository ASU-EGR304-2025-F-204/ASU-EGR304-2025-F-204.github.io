---
title: Software Proposal
---

## Introduction

Our software design shows how the ClapSense system makes decisions and runs its internal processes. The program operates in a continuous loop that listens for sounds, checks audio levels, and adjusts the light brightness or power based on what it detects.

The diagram highlights how each part of the system including initialization, input reading, output control, and state updates works together under the PIC18F57Q43 Curiosity Nano microcontroller.


## System-Level Activity Diagram

![Software Proposal Diagram](image/SoftwareProposal.drawio.png)
[Download Source (.drawio)](https://drive.google.com/file/d/1XWd2HWFe6WUE2Gx3-sKtdRthA2hVnKsh/view?usp=sharing)

### Initialize System
* Configures hardware registers and resets internal variables.  
* Establishes communication between subsystems and sets the initial default state (`000`).  
* Ensures all hardware peripherals (ADC, GPIO, and UART) are configured before entering the main loop.


### Read Input
* Collects analog sound data from the microphone/sound sensor.  
* Uses the ADC to convert sound amplitude into a digital value for comparison.  
* Filters and interprets clap patterns to detect user input for toggling the light.


### Set Output
* Compares input data (frequency and decibel levels) against defined thresholds.  
* Controls output pins for lighting, using the results of threshold checks.  
* Enables proper state transitions (ON/OFF toggle or brightness adjustments).  
* Implements both frequency-based and decibel-based decision paths.


### Update State
* Handles user interface interactions such as button presses or brightness adjustments.  
* Monitors ADC readings to determine if brightness should increase or decrease.  
* Toggles the light output when valid clap or button signals are detected.  
* Returns to the main loop after updating the system state.


### Team Members and Roles

**Caleb Yuen – Master Controller (Hub)**  
  Designed the main control logic that coordinates all subsystems. Handles initialization, communication, and signal management between boards. Manages the decision-making process that interprets clap inputs and triggers the light output sequence.

**Aaron Kiem – Audio Front-End**  
  Developed the sound detection and filtering logic. Configured the microphone and amplifier circuit using the MCP6022 op-amp and implemented ADC-based sampling to identify clap patterns while rejecting background noise.

**Roshan Roy Geoffrey Joe – Sensor Front-End**  
  Designed and coded the light-sensing functionality using the TEMT6000 phototransistor and op-amp stage. Configured ADC and DAC modules to translate sensor data into adjustable brightness feedback signals.

**Quinn Maness – Filter Board**  
  Implemented the user interface and visual feedback system. Controlled LED indicators and potentiometers for brightness adjustment. Created status cues for system states (ON, OFF, and Brightness Levels) through PWM-driven LEDs.


## References
* [Curiosity Nano hardware user guide](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/UserGuides/PIC18F57Q43-Curiosity-Nano-HW-UserGuide-DS40002186B.pdf)

