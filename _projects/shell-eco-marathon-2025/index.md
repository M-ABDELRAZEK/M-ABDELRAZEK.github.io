---
layout: post
title: "Shell Eco-marathon 2025 - 3-Wheel Electric Prototype"
description: "As Powertrain Head for Shell Eco-marathon 2025 in Qatar, I designed and simulated the battery system and powertrain of a 3-wheel electric prototype under strict rules (1 kWh, 60 V). The team finished 7th in the Asia-Pacific and Middle East region."
skills:
  - MATLAB/Simulink
  - OptimumLab
  - AutoCAD
  - BMS Integration
  - Battery Pack Design
  - Wiring
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335954910.webp
---

## Competition Rules
16 km track (4 laps), battery energy of 1 kWh or less, on-board voltage of 60 V or less, and a maximum time of 39 minutes. The goal was maximum energy efficiency.

## Motor Sizing & Decision Matrix
Sized the motor from drag, acceleration, rolling and gradient forces (0.46 kW peak, 0.20 kW rated) for 0.278 m/s2 acceleration at 30 km/h. A decision matrix compared brushed, brushless and hub motors, and the **350 W hub motor** won on efficiency (no drivetrain losses), availability and cost.

## Battery Pack (14S5P, 756 Wh)
A 70-cell pack with **Samsung INR18650-30Q** cells: 14 series, 5 parallel, 50.4 V nominal, 58.8 V max, 15 Ah, 756 Wh and 3.36 kg.

## Smart BMS
Integrated a smart BMS (4S-17S, 60 A) with 1 A active balancing, 4.2 V / 2.5 V per-cell over/under-voltage protection, current limits and a 60 C temperature cut-off. The Bluetooth interface gave real-time cell voltage, balancing and current monitoring.

## Simulation
MATLAB and Optimum-Lap models (with a custom drive cycle, since Optimum-Lap does not support 3-wheel vehicles) gave a 26 km/h average speed, **0.6175 kWh/100 km** simulated energy consumption and a 36.8 minute finishing time.

## Tractive System Documentation
Designed the tractive system schematic (battery to controller, precharge circuit, emergency shutdown paths) and wrote the safety documentation. The car passed competition scrutineering.

## Gallery
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780336810950.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780336734888.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335631073.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780336959169.webp" height="300" %}
