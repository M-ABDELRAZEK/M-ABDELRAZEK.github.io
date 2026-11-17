---
layout: post
title: "Formula Student 2025"
description: "As the Powertrain Head for Menofia Racing Team, I led the powertrain sizing and vehicle performance analysis for our concept-class electric race car competing at FSUK 2025. The goal was to design a high-performance EV capable of completing dynamic events (Acceleration, Sprint, Skidpad, Endurance) with optimal energy efficiency, cost effectiveness, and compliance with FSUK safety regulations. My role focused on motor sizing, motor controller selection, simulating whole vehicle performance, selecting the battery cell configuration and sizing, precharge resistance sizing, and determining the optimal drive ratio and regenerative braking calculations for endurance track."
skills:
  - MATLAB/Simulink
  - IPG CarMaker
  - OptimumLab
  - Excel
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780338570554.webp
---

## Accomplishments

### 1. Motor Selection & Sizing
Selected **EMRAX 188 MV** motor **(60 kW peak / 37 kW continuous, 100 Nm peak / 56 Nm continuous)** after evaluating multiple options based on power-to-weight ratio, drag force, rolling force, gradient force and acceleration force which gives vehicle and motor analysis (62 kW peak / 10 kW continuous / 1435 wheel RPM / 416 wheel NM)

### 2. Motor Controller Selection
Selected **DTI HV 550** motor controller featuring **CAN Bus & SSI communication** for real‑time data exchange with other ECUs and BMS, **Sinusoidal Field‑Oriented Control (FOC)** for smooth torque delivery and high efficiency, integrated **regenerative braking support**, **6.8 kg mass** (lightweight), 390A peak current, 380A continuous current, 800V max voltage, and 320 kW peak power – providing significant headroom and future upgrade capability.

### 3. Custom Battery Pack Design
Designed **95S7P Li‑ion battery pack** using **Samsung Q30** cells: **342V nominal**, **399V max**, **7182 Wh capacity**, **21 Ah**, **140A max current**, **31.92 kg total weight**. The pack uses 5 series segments (19S7P each) to comply with FSUK 120V‑per‑segment safety rule, achieving high energy density and safe voltage distribution.

### 4. Precharge Circuit Engineering
Sized precharge circuit for 342V battery and 200 µF controller DC bus capacitance with **1 sec charging time** to **99.3% of bus voltage**. Calculated **precharge resistance = 1000 Ω**, time constant = 0.2 sec, inrush current = 0.342 A, energy dissipated = 11.7 J, average power = 11.7 W, **peak power = 117 W** – ensuring safe DC bus charging, protecting contactors and capacitors from inrush damage.

### 5. Regenerative Braking & Energy Recovery
Targeted **1g braking deceleration**; based on vehicle dynamics and load transfer (RWD), calculated **86.3 Nm regeneration torque** which is applicable for the motor characteristics. **Limited regeneration current from 31 A to 28 A** (max battery charging current), reducing effective **deceleration to 0.834g** and **stopping time from 100 km/h to 3.39 sec** (compared to 2.8 sec target without hydraulic brakes). Achieved **0.293 kWh recovered energy for endurance track** – approximately 5% of battery SoC

### 6. Vehicle Performance Simulation
Simulated acceleration event (75m from standstill) achieving **4.9 seconds**, predicted top speed of 110 km/h, and confirmed full endurance range of 22 km using MATLAB and IPG CarMaker.

### 7. Drive Ratio Optimization
Determined optimal single‑speed drive ratio of **1:6** using OptimumLab and acceleration load profile and motor curves, balancing acceleration time, top speed, and energy consumption over a representative FSUK tracks. Trade‑off analysis considered motor operating points, efficiency map, and lap time.

### 8. Multi‑Platform Simulation Validation
Validated vehicle performance across **three simulation platforms** (MATLAB, IPG CarMaker, Optimum Lab) to ensure model consistency and reduce platform‑dependent errors. This cross‑validation approach increased confidence in simulation results – critical for a concept‑class vehicle where physical testing was limited.

## Project Gallery

{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780277415982.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780277464957.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780266551952.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780277607443.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780277720356.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780277850703.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780278074451.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780278163656.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780278204194.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780278280929.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780315254620.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780278331166.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780278437561.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780278653136.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780278724859.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780278786683.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780279023565.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780279095758.webp" height="300" %}
