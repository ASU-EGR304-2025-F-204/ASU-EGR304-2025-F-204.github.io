---
title: Product Requirements
tags:
- tag1
- tag2
---

## Project Objective

Our team is designing a next generation clap-activated smart light that makes everyday living a little easier. Traditional clap lights are cheap and fun, but anyone who's used one knows the fustrations. They often turn on when you are just talking or laughing and sometimes do not respond at all when you actually want them to. We want to fix that.

Our system will reliably tell the difference between a real clap and background noise so it only responds when you want it to. It will also let user custimize settings, schedule lights to turn on or off automatically, and fit seamlessly into a mondern smart home setup. The goal is to create a product that feels intuitive, dependable, and genuinely useful in daily life.

## Stakeholders

What is important to our team is reliability, accessibility, and simplicity. We want our clap-activated light to respond accurately every time without confusing random sounds for claps. Ease of use is another priority because users should not need electrical experience to install or customize the system. We also care about safety and affordability, making sure our design can be powered by a low-voltage USB connection and built under thirty dollars for accessible prototyping and real-world use.

We are designing primarily for two groups. The first group is young adults such as college students, nurses, or shift workers who need a simple, automated way to wake up or control lights hands-free. The second group is seniors and people with limited mobility who benefit from being able to turn on lights safely without getting up or reaching for switches.

As a team, our focus is on developing a reliable sound detection system that minimizes false triggers, a safe low-voltage circuit that can be used in dorms or senior living environments, and a modular design that can expand into future smart-home integration. These priorities show what matters most to us—creating a product that is dependable, safe, and inclusive while demonstrating real engineering and design skills.


## Use Cases

**User Story #1: Jesus**

Jesus is a senior who values simplicity and independence in his daily routine. He recently purchased a clap-activated device, and it turned out to be exactly what he needed. Now, with just a clap of his hands, he can easily turn the device on or off without having to fumble for switches.

For Jesus, this small feature makes a big difference, especially in his senior years. It gives him a sense of control and convenience, reducing the hassle of bending over or reaching for hard-to-access buttons. He feels grateful for how straightforward and effective the device is, and he finds joy in the fact that it works seamlessly for his needs.

**User Story #2: Arleta**

Arleta is someone who values convenience and ease in her daily life. She often found herself frustrated by having to constantly get up just to turn things off. That small but repeated hassle wore her down over time.

With her new clap-activated device, everything changed. Now, a simple clap of her hands allows her to control it without leaving her spot. She loves the newfound freedom and simplicity—it feels empowering to handle things effortlessly. For Arleta, this small feature means less interruption in her day and more comfort in her home.

## Aspects

**1. Hardware / Product Design**  
The product should operate at a safe low-voltage level below five volts and be compact enough for a small desk or bedside setup. All components should fit within a housing that can handle regular use without breaking or overheating. The design should allow easy connection between boards using a consistent interface.  

**2. Software / Functionality**  
The system should detect claps within a range of one to three meters with at least ninety percent accuracy. It should process and respond to valid input in under two hundred milliseconds and operate continuously for long periods without errors or resets.  

**3. User Experience**  
The device should be simple for a new user to set up in under ten minutes. It should clearly indicate when it is on, off, or waiting for a signal. The experience should feel reliable and intuitive so users can interact with it without confusion or technical knowledge.  

**4. Customization**  
The system should allow users to adjust sensitivity levels and the number of claps required for activation. It should also support different light brightness levels or colors for comfort and preference.  

**5. Manufacturing**  
The total production cost should remain under thirty dollars, and the design should use a minimal number of parts to simplify assembly and reduce failure points. The device should be consistent and reliable after multiple uses.  

**6. Safety**  
The system should prevent short circuits, maintain safe operating temperatures, and protect against overcurrent conditions. All wiring and enclosures should minimize electrical hazards and comply with basic safety standards for low-voltage devices.  

## Requirement Criteria Specifications

* 1. Regulate system power from 9 volts to 5 volts
* 2. Clap Detection Accuracy: ≥90% recognition at 1–3 m, ≤70 dB SPL background.
* 3. False Trigger Rate: ≤5% during 1 hour of continuous conversation/TV.
* 4. Response Time: Light toggles within ≤200 ms of valid clap detection.
* 5. Customization: User can set detection threshold (3 decibel levels) and number of claps (1–3).
* 6. Power Safety: On-board regulator maintains 5 V ±10% for MCU; overcurrent protection ≤1.5 A.
* 7. Durability: Device operates for ≥10,000 toggle cycles without component failure.
* 8. Manufacturing Cost: <$30 total BOM.
* 9. Setup Time: First-time setup ≤10 minutes by a new user.

## Open Questions

* Do we stick with a simple mechanical relay that’s cheap but makes a noticeable click, or invest in a solid-state option that’s quieter and feels higher-end?
* Should our first version stay focused on core clap and scheduling features, or do we start building in Alexa/Google compatibility right away?
* Is the PIC’s built-in timer “good enough” for daily schedules, or would it be worth adding a real-time clock chip to keep things precise over time?
* Should the design remain USB-powered for safety and easy prototyping, or do we eventually move toward a plug-in AC module that can directly control household lamps?