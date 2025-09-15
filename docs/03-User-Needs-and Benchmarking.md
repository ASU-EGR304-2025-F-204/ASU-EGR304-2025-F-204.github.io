---
title: User Needs and Benchmarking
tags:
- smart-home
- user-needs
---

## Introduction

This page documents how our team identified and prioritized user needs for a **smart home system** by benchmarking existing products and analyzing voice-of-the-customer (VOC) reviews. We summarize our method, product set, extracted needs, meta-needs, and the final prioritized list that will guide our requirements.


## Product Mission Statement
Our mission is to design and deliver a reliable smart home system that enhances daily living by improving **comfort, security, and energy efficiency**. We will analyze existing smart home products, incorporate user feedback, and leverage our team’s strengths to build an **accessible, maintainable, and user-friendly** solution that meets real-world needs.


## Benchmarking Method (VOC)
-


## Benchmarked Products (overview)
- [Clap Light](https://www.amazon.com/Control-Bedroom-Activated-Solution-Detection/dp/B0CVVBYG4R/)
- [Smart Blinds](https://www.amazon.com/MANSNIX-Motorized-Blackout-Automatic-Compatible/dp/B0B5X1DHWZ/)
- [Robot Vacuum & Mop](https://www.amazon.com/Mapping-Robotic-Navigation-Obstacle-Avoidance/dp/B0FGXQPQ8G)
- [Wifi Doorbell](https://www.bestbuy.com/product/ring-battery-doorbell-plus-smart-wifi-video-doorbell-battery-operated-with-head-to-toe-view-satin-nickel/J39HW6P9S2/sku/6531758?extStoreId=1189)
- [Smart Thermostat](https://www.walmart.com/ip/Google-Nest-Thermostat-Programmable-Smart-Thermostat-for-Home-Snow/415911305?wmlspartner=wlpa&selectedSellerId=102477550)


## Product Analyses

### 1) Clap Light — Amazon
**Search keywords:** `clap light smart lamp sound activated`  
**Search link:** [Amazon - Clap Light](https://www.amazon.com/Control-Bedroom-Activated-Solution-Detection/dp/B0CVVBYG4R/ref=sr_1_6?crid=3U1FMD7JVC7DW&dib=eyJ2IjoiMSJ9._tiqYg3j_PzFXnsdOnInFSkSRUS4rIO4ReeaU83PIvaCrzgJVULjJPAvigGHsL-XTR9qmRnjhaBsgdAl1ooTs8RQjZk_rSXzgWxmFJTAe9U3SmzcgOGVhxS0H7UfxAYzOM-j4xaYqC7cjOhI6xYYVZnXAf3kt31BZWAIl7r7s5Jmuio2JrmClKYbuv7WOXebE0Um1cxHQ2xX7z87t03HqwHpt6J0pFR0S1Sp99vNW7RkxunCeSY4Kmgwm2LzGB2gn2AOu7rqp7WSu_jbnMtImyWN_tBk_vu3joxxH7TjInU.CPaKihUm8y6R5_3XGf91pkNGACZSkA0U7NQJxZj5PYg&dib_tag=se&keywords=clap+light&qid=1757792515&sprefix=clap+light%2Caps%2C241&sr=8-6)

**Voice of the Customer → User Needs**

| Statements (summarized quotes) | User Need Statement | Explicit/Latent |
|---|---|---|
| “I love how it turns off when I clap—I don’t have to get up.” | The product reliably responds to hand claps to control the light. | Explicit |
| “Works well but also reacts to speaking or other sounds.” | The product distinguishes hand claps from other noises. | Explicit |
| “It turned on during phone calls / when people spoke.” | The product avoids false triggers from voices/background noise. | Explicit |
| “Goes on and off when I’m just talking or laughing.” | The product maintains accuracy by not confusing claps with speech/laughter. | Explicit |
| “Does not respond consistently to claps.” | The product responds consistently to clapping gestures. | Explicit |
| “Almost every noise sets it off—really annoying.” | The product filters irrelevant noise to minimize unwanted activations. | Explicit |

**Category / Meta-Need:**  
- **User Interaction** — *Recognize intended clap actions while ignoring background sounds.*

### 2) Smart Blinds — Amazon
**Search keywords:** `smart blinds motorized window shade`  
**Search link:** [Amazon - Smart Blinds](amazon.com/MANSNIX-Motorized-Blackout-Automatic-Compatible/dp/B0B5X1DHWZ/ref=cm_cr_arp_d_product_top?ie=UTF8)

**Voice of the Customer → User Needs**

| Statements (summarized quotes) | User Need Statement | Explicit/Latent |
|---|---|---|
| “Very easy to install and works flawlessly. Easy to program down motion if needed.” | The product should allow simple, user-friendly installation and programming. | Latent |
| “Love the blind. Works well. It is too long for most windows… I control it for the evening while I set up a timer for the morning.” | The product should adapt to different window sizes and allow scheduled automation. | Latent |
| “Easy install. No drill required unless you want to secure it more. Quiet motorized shade… Comes with extra spacers for adjusting.” | The product should be quiet, adjustable, and powered conveniently. | Latent |
| “Like the product but 2 of my 3 shades have pin holes… noticeable on blackout shades.” | The product should maintain consistent build quality with no light leakage. | Latent |
| “Bought these because Alexa said they could open/close on a schedule… not the case. No option in the app.” | The product should support scheduling directly through the app without extra hardware. | Latent |
| “Comes with regular battery drain issue. Motor sound bit loud then other times.” | The product should have long-lasting battery life and **consistent, quiet operation. | Latent |

**Category / Meta-Needs:**  
- **Power** — *Remain reliably powered through simple conventions (long battery life, easy replacement).*  
- **User Interaction** — *Require little to no setup while providing flexible automation (scheduling, app integration).*  
- **Quality** — *Deliver consistent performance and durable build with no defects.*


### 3) Robot Vacuum & Mop — Amazon
**Search keywords:** `robot vacuum smart home`  
**Search link:** [Amazon - Robot Vacuum and Mop](https://www.amazon.com/Mapping-Robotic-Navigation-Obstacle-Avoidance/dp/B0FGXQPQ8G)

**Voice of the Customer → User Needs**

| Statements (summarized quotes) | User Need Statement | Explicit/Latent | Meta Need |
|---|---|---|---|
| “It’s especially great for picking up pet hair from both carpets and hard floors.” | The product removes dirt, dust, and pet hair effectively across multiple floor types. | Explicit | Cleaning Performance |
| “The navigation system ensures it doesn’t bump into furniture or get stuck.” | The product avoids obstacles and provides reliable navigation. | Explicit | Reliability |
| “I love that it can clean my home quietly at night.” | The product operates at a quiet noise level suitable for daily routines. | Explicit | Comfort |
| “Battery drains too quickly if run on high suction.” | The product should have long-lasting battery life even under heavy use. | Explicit | Power |
| “Gets tangled in cords or rugs sometimes.” | The product avoids getting stuck and recovers smoothly from obstacles. | Latent | Reliability |
| “Sometimes misses corners or under furniture.” | The product cleans hard-to-reach areas like corners and under furniture. | Explicit | Coverage |

**Category / Meta-Need:**  
- **Automation & Cleaning** — *Automates floor cleaning with strong suction, reliable navigation, and smart integration for minimal user effort.*



### 4) Battery Doorbell Plus Smart Wifi Doorbell - Best Buy
**Search keywords:** `camera door doorbell smart household wifi`  
**Search link:** [Best Buy - Ring Wifi Doorbell](https://www.bestbuy.com/product/ring-battery-doorbell-plus-smart-wifi-video-doorbell-battery-operated-with-head-to-toe-view-satin-nickel/J39HW6P9S2/sku/6531758?extStoreId=1189)

**Voice of the Customer → User Needs**

| Statements (summarized quotes) | User Need Statement | Explicit/Latent | Meta Need |
|---|---|---|---|
| “Crystal-clear video, and the ‘head-to-toe’ view shows faces and packages; night vision works great.” | The product delivers high-quality HD+ (1536p) video with a tall field of view and clear night vision. | Explicit | Video Quality & Coverage |
| “Motion alerts are customizable and super responsive; ‘person detected’ notifications helped me intervene.” | The product provides reliable, customizable motion detection that promptly alerts the user. | Explicit | Reliability |
| “Two-way audio is crisp—people can hear me even from a distance.” | The product enables clear two-way communication with visitors. | Explicit | Communication |
| “Battery lasts weeks; for us it goes about a month between charges depending on foot traffic.”  | The product should offer long battery life under real-world usage. | Explicit | Power |
| “Installation was easy; the app is intuitive; I even hooked it to my existing doorbell wires/chime.” | The product must be simple to install and easy to control via an app. | Explicit | Ease of Use |
| “Works with Alexa—view on Echo Show and get announcements.” | The product should integrate smoothly with the Alexa ecosystem for viewing and voice prompts. | Explicit | Smart Home Integration |
| “After the 30-day trial you need a paid plan to keep using cloud recordings; package alerts are part of the subscription.” | The product should be transparent about ongoing costs; essential features (recording/package alerts) often require a subscription. | Explicit | Ownership Cost Transparency |
| “First charge took a while; having a spare quick-release battery is very handy.” | Faster charging or an easy spare-battery workflow reduces downtime. | Latent | Power Convenience |
| “Not compatible with my older doorbell bracket.” | The product should maintain or clearly communicate mount compatibility or include adapters. | Explicit | Compatibility |

**Category / Meta-Needs:**  
- **Home Monitoring and Security** — *See/communicate with visitors, receive dependable alerts, capture package deliveries.*
- **Ease of Use and Power** — *Simple setup with strong battery performance in real world conditions.*



### 5) Programmable HVAC Monitoring Thermostat - Walmart
**Search keywords:** `hvac thermostat smart household programmable`  
**Search link:** [Google Nest Thermostat](https://www.walmart.com/ip/Google-Nest-Thermostat-Programmable-Smart-Thermostat-for-Home-Snow/415911305?wmlspartner=wlpa&selectedSellerId=102477550)

**Voice of the Customer → User Needs**

| Statements (summarized quotes) | User Need Statement | Explicit/Latent | Meta Need |
|---|---|---|---|
| “It actually helped lower my bill—Eco Temps kick in when I leave.” | The product reduces energy costs with presence-based Eco temperatures and energy-saving features. | Explicit | Energy Savings |
| “I can set and tweak schedules right in the Google Home app from anywhere.”  | The product allows remote control and easy scheduling via the Google Home app (Quick Schedule). | Explicit | Ease of Use |
| “I just say the word to change the temp—works with Google Assistant/Alexa.” | The product supports reliable voice control across major smart-home assistants. | Explicit | Smart Home Integration |
| “It alerts me if something seems off with my HVAC and reminds me to change filters.” | The product provides HVAC monitoring and maintenance reminders to prevent issues. | Explicit | Reliability & Maintenance |
| “Install was straightforward, and the app checked my system for compatibility.” | The product offers simple, guided setup and a compatibility check to avoid surprises. | Explicit | Onboarding |
| “Looks clean and modern; the display is easy to read.” | The product has a minimal, readable display and aesthetic design that blends into the home. | Explicit | Aesthetics |
| “Runs fine on my system, but some setups really need a C-wire to avoid battery problems.” | The product should work across systems and clearly guide when a C-wire is required to ensure stable power. | Latent | Compatibility & Power |
| “ENERGY STAR certified—nice to know it’s efficient.” | The product meets ENERGY STAR efficiency standards. | Explicit | Energy Efficiency |
| “After hearing support news on older models, I want clear long-term software support.” | The product should provide transparent, durable software support and feature longevity. | Latent | Longevity & Support |

**Category / Meta-Needs:**  
- **Home Climate Control and Energy Management** — *Maintain satisfactory temperatures while cutting waste with easy app usage, system monitoring, and compatibility.*



## Consolidated Need Categories & Meta-Needs


> **Screenshots:** Insert three images showing (1) all needs collected, (2) grouped by category, (3) ranked.



## Prioritized Top Needs
1.   
2.   
3.   
4.  
5. 

>**Ranking method:** frequency in reviews (quantified counts), impact on safety/utility, and team vote (weighted 50/30/20).


