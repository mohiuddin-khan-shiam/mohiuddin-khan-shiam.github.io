---
title: "Autonomous Line Following Hardware Robot"
excerpt: "Autonomous vehicle engineered from fundamental discrete logic gates, IR optical sensors, comparator ICs, and H-bridge motor drivers without microcontrollers."
collection: portfolio
date: 2023-11-01
permalink: /portfolio/autonomous-line-follower/
---

<div class="project-header-box">
  <span class="badge badge--tools"><i class="fa-solid fa-microchip"></i> Digital Logic Design</span>
  <span class="badge badge--tools"><i class="fa-solid fa-robot"></i> Embedded Hardware</span>
  <span class="badge badge--tools"><i class="fa-solid fa-bolt"></i> Discrete Electronics</span>
</div>

### Project Overview

Developed as a capstone physical engineering project for the **Digital Logic Design** curriculum at BRAC University, this autonomous line-following vehicle demonstrates the power of low-level analog-to-digital signal processing without relying on microcontrollers or high-level firmware.

### Engineering & Hardware Design

- **Optical Sensor Array**: Configured infrared (IR) transmitter-receiver optical pairs calibrated for high-contrast ground reflectance differentiation.
- **Signal Condition & Comparators**: Utilized LM393 voltage comparators to transform analog reflectance levels into sharp TTL binary logic signals.
- **Combinational Logic Circuitry**: Engineered Boolean logic arrays using discrete NOT, AND, OR, and XOR IC gates to determine precise steering decisions (straight, gentle turn, hard pivot).
- **Actuation & Motor Driving**: Integrated L293D dual H-bridge motor drivers to control dual DC gear motors, handling dynamic voltage delivery and inductive back-EMF protection.
