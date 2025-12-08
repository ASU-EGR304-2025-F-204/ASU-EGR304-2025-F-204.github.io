---
title: Product Requirements
tags:
- tag1
- tag2
---

## Project Objective
The goal of this project is to create a next-generation clap-activated smart light that reliably distinguishes real claps from background noise, responds quickly, and provides useful customization features to improve everyday convenience.

## Stakeholders

Our primary stakeholders are users whose needs directly influence our engineering limits. Seniors or individuals with limited mobility may clap from a seated or lying position, so the system must detect claps from longer distances and without requiring physical interaction. Users with reduced hearing may clap louder or softer than typical levels, so the system must support adjustable sensitivity to accommodate different sound profiles. Young adults, such as college students or shift workers, may need a simple hands-free way to control lights while multitasking, so the product must be easy to install and intuitive to use. Safety-focused users require low-voltage operation, no exposed wiring, and predictable behavior. These characteristics define our measurable design constraints: long-distance detection, adjustable thresholds, fast setup, consistent accuracy, and safe operation under 5 volts.


## Use Cases

**User Story #1: Jesus**

Jesus is a senior who prefers not to bend or reach for switches. Because he often claps while seated, the system must detect claps reliably from up to three meters away at varying angles. His story drives requirements for long-range detection, simple installation, clear status indication, and minimal physical effort.

**User Story #2: Arleta**

Arleta values convenience but lives with constant background noise from her TV. Her experience requires the system to ignore normal conversation and television audio while still responding to a deliberate clap. This leads to requirements for false-trigger filtering, adjustable sensitivity, and reliable operation in noisy environments.

## Aspects

**1. Hardware / Product Design**  
The product must operate safely below five volts, fit into a compact enclosure, and maintain reliable operation without excessive heat. Internal modules must connect consistently, and the physical design must withstand repeated daily use.

**2. Software / Functionality**  
A new user should be able to set up the device in under ten minutes. Visual indicators must clearly communicate system state, and interactions should feel intuitive without requiring technical knowledge.  

**3. User Experience**  
The device should be simple for a new user to set up in under ten minutes. It should clearly indicate when it is on, off, or waiting for a signal. The experience should feel reliable and intuitive so users can interact with it without confusion or technical knowledge.  

**4. Customization**  
Users should be able to adjust detection sensitivity and choose between one, two, or three claps for activation. Support for brightness levels or color control should be available for comfort and preference. 

**5. Manufacturing**  
The system must maintain a bill of materials cost under thirty dollars and use as few parts as possible to simplify manufacturing, improve reliability, and reduce failure points. 

**6. Safety**  
All circuitry must prevent shorts, overcurrent, and overheating. External surfaces must remain safe to touch, and the design must comply with low-voltage safety guidelines.

## Requirement Criteria Specifications (SMART)

* 1. Regulate system power from 9 V to 5 V within ±10%.
* 2. Clap detection accuracy ≥90% at 1–3 meters in ≤70 dB environments.
* 3. False trigger rate ≤5% during one hour of conversation or TV audio.
* 4. System response time ≤200 ms from clap to light toggle.
* 5. User-adjustable sensitivity across three levels and activation using 1–3 claps.
* 6. Overcurrent protection limited to ≤1.5 A; external surface temperature ≤50°C.
* 7. Device must operate for at least 10,000 toggle cycles without failure.
* 8. Total BOM cost < $30.
* 9. First-time setup completed by a new user in ≤10 minutes.
* 10. System must detect claps ≥80 dB SPL for accessibility.
* 11. Device must remain operational without false triggers in noise up to 65 dB SPL.
* 12. All external surfaces must remain below 50°C during normal operation.

## Open Questions

* Should the product use a mechanical relay for simplicity or a silent solid-state switch for a more premium experience?
* Should the first product version focus solely on clap and scheduling features, or include Alexa/Google compatibility from the start?
* Is the PIC’s internal timer sufficient for scheduling, or is an external RTC required for long-term accuracy?
* Should the design remain USB-powered for safety, or eventually support AC mains control for lamp integration?
