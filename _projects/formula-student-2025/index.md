---
layout: post
title: "Formula Student 2025 (FSUK) - EV Powertrain Sizing"
description: "As Powertrain Head for Menofia Racing Team, I led the powertrain sizing and vehicle performance analysis of a concept-class electric race car for FSUK 2025: motor and controller selection, a custom 95S7P battery pack, precharge sizing, drive ratio and regenerative braking."
skills:
  - MATLAB/Simulink
  - IPG CarMaker
  - OptimumLab
  - Excel
  - Battery Pack Design
  - Motor Sizing
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780338570554.webp
---

## Motor Selection & Sizing
Selected the **EMRAX 188 MV** (60 kW peak / 37 kW continuous, 100 Nm peak / 56 Nm continuous) after evaluating power-to-weight ratio and the drag, rolling, gradient and acceleration forces. Vehicle analysis showed 62 kW peak, 10 kW continuous, 1435 wheel RPM and 416 Nm wheel torque.

## Motor Controller
Selected the **DTI HV 550**: CAN bus and SSI communication, sinusoidal field-oriented control (FOC), integrated regenerative braking support, 6.8 kg, 390 A peak / 380 A continuous, 800 V max and 320 kW peak power, leaving headroom for future upgrades.

## Custom Battery Pack (95S7P)
Designed a 95S7P Li-ion pack with **Samsung Q30** cells: 342 V nominal, 399 V max, 7182 Wh, 21 Ah, 140 A max current and 31.92 kg. The pack is split into five 19S7P segments to comply with the FSUK 120 V-per-segment rule.

## Precharge Circuit
Sized the precharge circuit for the 342 V pack and a 200 uF controller DC-bus capacitance: 1 kOhm resistor, 0.2 s time constant, 1 s to reach 99.3% of bus voltage, 0.342 A inrush, 11.7 J dissipated and 117 W peak power.

## Regenerative Braking
Targeted 1 g braking and calculated 86.3 Nm of regenerative torque for the rear-wheel-drive load transfer. Limiting regeneration current from 31 A to 28 A (maximum battery charging current) reduces deceleration to 0.834 g, with a 100 km/h stop in 3.39 s. About 0.293 kWh is recovered over the endurance track, roughly 5% of battery SoC.

## Performance Simulation & Drive Ratio
Simulated a 75 m acceleration in **4.9 s**, a top speed of 110 km/h and a 22 km endurance range. OptimumLab and the acceleration load profile gave an optimal single-speed **1:6** drive ratio. Results were cross-validated across MATLAB, IPG CarMaker and OptimumLab.

## Gallery
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780277415982.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780277464957.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780266551952.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2135/highlight_1780277607443.webp" height="300" %}
