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

- **Target group** Our product is designed for early risers college students, nurses, farmers, and other young adults (typically 19–30) who struggle with getting up in the morning and believe a light turning on could help them wake more easily. Seniors are also an important group. For many older adults, having to physically reach light switches can be a daily challenge that increases the risk of falls and reminds them of mobility limitations. A clap-activated light offers independence and peace of mind.
- **Target purchaser** The people most likely to buy this product are those looking for a quick, affordable way to add a clap-light to their home. Busy young adults with unpredictable sleep schedules can benefit from a simple, adjustable light system. Seniors with mobility issues are another key purchaser group, as the device reduces everyday inconveniences and promotes safety.
- **Customer service** Our users expect a product that is easy to set up without requiring electrical experience. For seniors in particular, installation needs to be straightforward and safe. Customer service should emphasize compatibility with a wide range of light fixtures, along with providing clear guidance on both on device adjustments and software customization. Striking a balance between simplicity and flexibility will be essential.
- **Marketing & Sales division** This product can be marketed on social media platforms like Instagram and TikTok through relatable college and lifestyle content, highlighting its convenience as a bedroom or dorm accessory. At the same time, outreach to senior communities including cable television ads and direct partnerships with senior homes will help connect with older users.
- **Retailers** The clap-light will be sold primarily through online retail channels for easy access and shipping. It should also be available at affordable, large retailers such as Walmart & Amazon. Packaging will be sustainable and designed to withstand normal storage conditions in a dry, moderate climate.


## Use Cases

**User Story #1: Jesus**

Jesus is a senior who values simplicity and independence in his daily routine. He recently purchased a clap-activated device, and it turned out to be exactly what he needed. Now, with just a clap of his hands, he can easily turn the device on or off without having to fumble for switches.

For Jesus, this small feature makes a big difference, especially in his senior years. It gives him a sense of control and convenience, reducing the hassle of bending over or reaching for hard-to-access buttons. He feels grateful for how straightforward and effective the device is, and he finds joy in the fact that it works seamlessly for his needs.

**User Story #2: Arleta**

Arleta is someone who values convenience and ease in her daily life. She often found herself frustrated by having to constantly get up just to turn things off. That small but repeated hassle wore her down over time.

With her new clap-activated device, everything changed. Now, a simple clap of her hands allows her to control it without leaving her spot. She loves the newfound freedom and simplicity—it feels empowering to handle things effortlessly. For Arleta, this small feature means less interruption in her day and more comfort in her home.

## Aspects

1. **Hardware / Product Design**
      * LED
      * PIC18F57Q43 Curiosity Nano Board
      * Various resistors
      * Wires
      * Sound sensors
      * Breadboard
      * Curisity Nano Cable
 
2. **Software / Functionality**
      * The product will have the implementation of Nano Board Coding
      * The product shall have one sensor to detect the user.

3. **User Experience**
      * The product shall be easy to setup and implement
      * The product will require the user to clap to toggle light

4. **Customization**
      * The product shall offer customizable decibel levels for detection
      * The product shall offer customizable amounts of claps for toggling
      * The product shall offer multiple different LED light colors.

5. **Manufacturing**
      * The product will be designed with circuitry on a breadboard.
      * Functioning of the device shall be easy to assess by a manufacturing.
      * The total cost price of the produce shall be <$30.
      * The product shall be designed to consist of the minimum possible amount of parts.


6. **Safety**
      * Powered by USB 5 V from Curiosity Nano board (no exposed mains in prototype).
      * All wiring on breadboard must avoid shorts; use resistors to limit LED current to ≤20 mA.
      * Relay or MOSFET switching stage must include flyback protection.

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