---
layout: post
title: "ADAS Direction Detection"
description: "A simple ADAS direction detection system developed for the OS Academy Model‑Based Design Challenge (achieved 3rd place). The MATLAB/Simulink model processes steering yaw rate (-180° to 180°) and camera‑based road sign detection to automatically activate the vehicle’s direction indicator. The logic compares yaw rate against thresholds (right ≥30°, left ≤-120°, straight ≈0°) and validates against sign input before outputting a boolean confirmation signal. The model was structured into three subsystems: SteeringDetection, SignValidation, and OutputGeneration. Production‑ready C code was generated using Simulink Coder (ERT) with fixed‑width data types (int16_T for angles, boolean_T for flags) for execution and RAM efficiency."
skills:
  - MATLAB/Simulink
  - Embedded Coder
  - MIL Testing
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2144/highlight_1780345641088.webp
---

## Accomplishments

### 1. Simple ADAS Logic with Appropriate Data Types
Designed a Simulink model with inputs: `Steering_Input_YawRate` (int16_T, range -180° to 180°) and `RoadSign_Input_Camera` (boolean_T). Output: `Direction_Indicator_Output` (boolean_T). Used **int16_T** to optimize memory (instead of int32) and **boolean_T** for flags – suitable for low‑cost embedded targets.

### 2. Threshold‑Based Decision Logic
Implemented the following logic:

- If camera detects a turn sign **AND** steering angle ≥30° → right indicator ON.
- If camera detects a turn sign **AND** steering angle ≤-120° → left indicator ON.
- If no sign detected **AND** steering angle ≈0° → straight confirmation ON.
- Else → indicator OFF.

Used **Switch blocks** with relational operators and **If‑Action subsystems** for clean state‑based execution.

### 3. Structured Subsystems & Code Generation
Organized the model into three subsystems: `SteeringDetection` (yaw rate thresholding), `SignValidation` (camera matching), and `OutputGeneration` (final decision). Generated standalone C code using **Simulink Coder (ERT)** with `rtwtypes.h` (fixed‑width types), model step function, and `ert_main.c` as a real‑time harness. Code optimized for execution efficiency and minimal RAM.

## Project Gallery

{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2144/highlight_1780345645405.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2144/highlight_1780345648779.webp" height="300" %}
