---
layout: post
title: "Shell Eco Marathon 2026"
description: "As the Electrical Head of the Menofia Racing Team for Shell Eco-marathon 2026, I led the redesign of the electric prototype’s powertrain and battery system to overcome limitations observed in the previous season (continuous motor operation, thermal stress). The key innovation was replacing the hub motor with a regular brushless DC motor + drivetrain, enabling mechanical decoupling during coasting and efficient Pulse & Glide driving strategy. The battery voltage was reduced from 48V to 36V (10S5P, 540Wh) while maintaining energy capacity within competition limits. I participated in motor reselection and tests, battery reassembly, and drive cycle simulation using MATLAB and Excel‑based acceleration/deceleration profiles. A core objective of the simulations was to generate dynamic data (position, speed, acceleration events) to train an AI model that advises the driver in real‑time when to accelerate and when to coast, with post‑processing for strategy optimization. This work contributed to winning the 2nd Place Data & Telemetry System Award at Shell Eco-marathon Qatar 2026. The new design improved thermal performance and reduced average current draw, accomplishing 383.8 km/kWh – building on the team’s previous 109 km/kWh efficiency baseline."
skills:
  - MATLAB/Simulink
  - Excel
  - AutoCAD
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341202629.webp
---

## Accomplishments

### 1. Drivetrain Innovation – From Hub Motor to Regular Motor + Drivetrain
Led the transition from a hub motor (which prevented coasting due to regenerative braking drag) to a **350W regular brushless DC motor** coupled with a drivetrain **(gear ratio 10:1)**. This mechanical decoupling enables true **Pulse & Glide** operation, reducing continuous motor running time, lowering average current, and improving thermal management – directly addressing the previous season’s overheating issues. Participated in motor re‑selection and on‑bench testing to validate performance.

### 2. Battery Reassembly – 36V, 10S5P, 540Wh
Redesigned and reassembled the battery pack using existing **Samsung INR18650‑30Q** cells in a new configuration: **10 series** (36V nominal, 42V max), **5 parallel** (15Ah, 15A continuous). **Total energy 540Wh, mass 2.4 kg** – compliant with Shell Eco‑marathon rules (≤1kWh, ≤60V). The 36V architecture matches the new motor’s requirement (max current 17A) and improves system safety.

### 3. Drive Cycle Simulation & AI Training Data Generation
Developed a custom drive cycle using Excel with calculated **acceleration (0.264 m/s²) and deceleration due to coasting (-0.0885 m/s²)** phases to implement Pulse & Glide between **22–30 km/h**. Simulated power consumption in MATLAB, achieving **average cruising speed 25 km/h**, **finishing time 33.2 minutes** for the 16 km track, and **energy efficiency of 383.8 km/kWh**. Generated dynamic dataset (position, speed, acceleration timing) specifically designed to train an **AI model** that advises the driver in real‑time when to accelerate and when to coast – enabling a dynamic driving assistant.

### 4. Circuit Modifications for Pulse & Glide & Telemetry Integration
Implemented key modifications to the tractive circuit to support Pulse & Glide operation, including: **excluding the non-propulsion accessories from the joulemeter reading** and powered directly from battery by DC/DC converter, revising the **precharge circuit** for the 36V bus, and updating **emergency shutdown paths**. **Integrated telemetry sensors** to collect real‑time vehicle data (speed, position, current) used for both driver feedback and post‑processing strategy optimization.

### 5. 2nd Place – Data & Telemetry System Award
The AI‑ready data generation and real‑time telemetry system contributed directly to winning the **2nd Place Data & Telemetry System Award** at Shell Eco‑marathon Qatar 2026, recognizing the team’s ability to collect, process, and utilize vehicle data for performance improvement.

## Project Gallery

{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341036176.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341041914.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341330410.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341348569.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341455563.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341459002.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341462217.webp" height="300" %}
