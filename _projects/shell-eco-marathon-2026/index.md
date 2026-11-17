---
layout: post
title: "Shell Eco-marathon 2026 - Pulse & Glide Powertrain"
description: "As Electrical Head, I led the redesign of the electric prototype powertrain: a regular BLDC motor with a 10:1 drivetrain instead of a hub motor, a 36 V 10S5P battery, and drive-cycle simulation used to train an AI driver-advisory model. Awarded 2nd Place, Data & Telemetry System Award."
skills:
  - MATLAB/Simulink
  - Excel
  - AutoCAD
  - Telemetry
  - Pulse & Glide
  - AI Data Generation
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341202629.webp
---

## Award
**2nd Place - Data & Telemetry System Award**, Shell Eco-marathon Qatar 2026.

## Drivetrain: Hub Motor to BLDC + Gearbox
The hub motor could not coast because of regenerative drag and suffered thermal stress. Replacing it with a **350 W BLDC motor and a 10:1 drivetrain** allows true Pulse & Glide driving, lowers average current and improves thermal behavior. Motor reselection and bench tests were part of the work.

## Battery Reassembly (10S5P, 36 V, 540 Wh)
Rebuilt the pack from the same Samsung INR18650-30Q cells: 10 series, 5 parallel, 36 V nominal, 42 V max, 15 Ah, 540 Wh and 2.4 kg, matching the new motor (17 A max).

## Drive Cycle & AI Training Data
Built a custom Pulse & Glide drive cycle in Excel (0.264 m/s2 acceleration, -0.0885 m/s2 coasting deceleration, 22-30 km/h) and simulated power in MATLAB: 25 km/h average speed, 33.2 minutes for 16 km and a simulated **383.8 km/kWh**, compared with the team's previous 109 km/kWh baseline. The simulation also generated position, speed and acceleration data to train an **AI model that advises the driver when to accelerate and when to coast**.

## Circuit Changes & Telemetry
Moved non-propulsion accessories off the joulemeter reading (powered through a DC/DC converter), revised the precharge circuit for the 36 V bus, updated the emergency shutdown paths and integrated telemetry sensors for speed, position and current.

## Gallery
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341036176.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341041914.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341330410.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2139/highlight_1780341348569.webp" height="300" %}
