---
title: Software Design
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


### Set ON/OFF
* Compares input data (voltage from photoresistor and op-amp) against defined thresholds.  
* Controls output pins for lighting, using the results of threshold checks.  
* Enables proper state transitions (ON/OFF toggle).  


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

**Quinn Maness – Light Sensor**  
  Developed the system for sensing outside light to save power. Used a photoresistor and MCP6004 Op-Amp with a LM7805 voltage regulator. Configured the microcontroller to output a digital voltage based on the input from the photoresistor-MCP6004 system.

**Roshan Roy Geoffrey Joe – Distance Sensor Front-End**  
  Designed and implemented the brightness-control logic driven by the distance sensor and MCP6002 op-amp. Configured the ADC on RA0 to read the amplified distance signal, filtered the readings in software, and mapped them into discrete brightness levels. Used DAC1 on RA2 to send a smooth, analog brightness command to the LED board through the ribbon cable.

## Software Version 2.0 Discussion
If our team were to develop a Version 2.0 of the entire ClapSense software system, we would focus on improving how the four subsystems work together and how data moves from the sensing boards into the Hub. In our current design each subsystem functions independently and sends a simple signal to the Hub. The Audio Front-End outputs a digital clap detection signal, the Light Sensor sends a digital high or low value based on ambient brightness, and the Distance Sensor Front-End outputs an analog voltage for LED brightness. The Hub software then reads these three inputs and makes the final decision about turning the motor on or off and adjusting the LED brightness. This approach works, but the software in Version 2.0 could take much better advantage of the hardware and create a more synchronized and reliable overall system.

One improvement would be standardizing the signal processing across the sensing boards so the Hub receives cleaner and more consistent information. Right now each board interprets its own sensor in its own way, and the Hub has to assume the signals are correct. In a Version 2.0 design we could refine the Audio Front-End software to provide not just a raw clap flag but also confidence levels or filtered metrics that make clap detection more robust. The Light Sensor Front-End could provide a scaled brightness value instead of a simple high or low output, giving the Hub more context for deciding when to activate the system. The Distance Front-End could support built in smoothing or classification so the Hub does not need to process noisy ADC readings. These changes would make the system more accurate and better aligned with our team requirement of reducing false triggers and ensuring predictable behavior in different environments.

Another major improvement would involve timing and synchronization. In Version 1 each subsystem updates its output continuously and independently, and the Hub polls them in a loop. This can lead to small inconsistencies in when each signal changes. Version 2.0 could establish a shared update rate or a trigger mechanism so that all subsystems refresh their outputs at predictable intervals. The Hub could then run its state machine with the confidence that all three inputs represent a consistent snapshot of the environment. This improvement would help us meet the performance requirement of responding to a clap within two hundred milliseconds while avoiding situations where one subsystem lags behind the others.

We would also redesign the Hub software to use a clearer and more expressive state machine. In Version 1 the Hub simply checks whether a clap occurred and whether the light sensor is covered. In Version 2.0 we could introduce states such as Listening, Verifying, Active, and Cooldown. These states would let the Hub combine information from the Audio, Light, and Distance boards in smarter ways. For example, the Hub could ignore claps when the distance sensor shows that no one is near the device or require multiple confirmation checks from the Audio Front-End before activating the motor. This would directly support our requirements for accuracy, safety, and usability.

Finally, Version 2.0 would benefit from better system wide debugging and calibration. Only the Hub currently outputs information over UART, and it is mostly used to display the distance ADC value. A future version could unify debugging so that the Hub reports audio thresholds, light sensor values, and distance readings together. Users or teammates could then adjust sensitivity or brightness mapping without editing the firmware on each board. This would make the entire system easier to tune and would help us meet our requirement for simple setup and consistent performance.

Overall, Version 2.0 would not completely change the purpose of any subsystem, but it would improve how they cooperate. The Audio Front-End would provide richer clap information, the Light Sensor would offer more environmental context, the Distance Front-End would deliver cleaner and more stable data, and the Hub would coordinate everything through a smarter state machine. These changes would make the software more reliable, more accurate, and better aligned with the team’s product requirements.




## References
* [Curiosity Nano hardware user guide](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/UserGuides/PIC18F57Q43-Curiosity-Nano-HW-UserGuide-DS40002186B.pdf)
