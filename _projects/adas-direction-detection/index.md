---
layout: post
title: "ADAS Direction Detection"
description: "A simple ADAS direction detection model built for the OS Academy Model-Based Design Challenge (3rd place). It combines steering yaw rate and camera-based road sign detection to activate the direction indicator, with generated C code."
skills:
  - MATLAB/Simulink
  - Embedded Coder
  - MIL Testing
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2144/highlight_1780345641088.webp
---

## Result
**3rd place** at the OS Academy Model-Based Design Challenge.

## Logic
Inputs: `Steering_Input_YawRate` (int16, -180 to 180 degrees) and `RoadSign_Input_Camera` (boolean). Output: `Direction_Indicator_Output` (boolean).
- Turn sign and steering of 30 degrees or more: right indicator on.
- Turn sign and steering of -120 degrees or less: left indicator on.
- No sign and steering near 0: straight confirmation on.
- Otherwise the indicator is off.

## Structure & Code Generation
Three subsystems: SteeringDetection, SignValidation and OutputGeneration. C code generated with Simulink Coder (ERT), using int16_T and boolean_T for low memory use on low-cost embedded targets.

## Gallery
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2144/highlight_1780345645405.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2144/highlight_1780345648779.webp" height="300" %}
