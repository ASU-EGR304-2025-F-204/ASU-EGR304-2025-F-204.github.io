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


### Update Brightness
* Reads the most recent ADC value from the distance sensor front-end.
* Applies simple digital filtering to smooth out noise and rapid fluctuations in the sensor signal.
* Maps the filtered value into a small number of discrete brightness levels (for example 6 steps from very dim to bright).
* Gradually steps between brightness levels so the LED does not “jump” or flash when the distance changes.
* Sends the final brightness command to the LED driver via the DAC output and then returns to the main loop.



### Team Members and Roles

**Caleb Yuen – Master Controller (Hub)**  
  Developed the theoretical control logic for how the system coordinates all subsystems. Planned the initialization sequence, communication structure, and signal flow between boards.

**Aaron Kiem – Audio Front-End**  
  Developed the sound detection and filtering logic. Configured the microphone and amplifier circuit using the MCP6022 op-amp and implemented ADC-based sampling to identify clap patterns while rejecting background noise.

**Quinn Maness – Filter Board**  
  Developed the filtering and filter adjustment system for the clap sound logic. Utilized a window comparator circuit with window comparator TLV6700DDCR and the active band-pass device BA3835F-E2 in order to create the filter threshold for decibel level and frequency, respectively. Implemented potentiometers onto both systems in order to allow for user adjustment of the threshold ranges for both frequency and decibel.

**Roshan Roy Geoffrey Joe – Distance Sensor Front-End**  
  Designed and implemented the brightness-control logic driven by the distance sensor and MCP6002 op-amp. Configured the ADC on RA0 to read the amplified distance signal, filtered the readings in software, and mapped them into discrete brightness levels. Used DAC1 on RA2 to send a smooth, analog brightness command to the LED board through the ribbon cable.


## References
* [Curiosity Nano hardware user guide](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/UserGuides/PIC18F57Q43-Curiosity-Nano-HW-UserGuide-DS40002186B.pdf)

If we were to create a version 2.0 of this project we would like to have extra debugging LEDs to indicate which subsystem is giving output to the overall system.
