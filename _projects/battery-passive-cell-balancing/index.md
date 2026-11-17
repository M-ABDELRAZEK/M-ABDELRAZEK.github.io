---
layout: post
title: "Battery Passive Cell Balancing"
description: "Developed a passive cell balancing algorithm for a 4‑cell Li‑ion battery pack using Model‑Based Design with MATLAB/Simulink and Stateflow. The work was structured as a Software Component (SWC) to enable modular code generation and easy integration into a larger BMS. A Model‑in‑the‑Loop (MIL) test environment was created to validate the balancing logic (state machine, threshold comparisons, switch activation) before any code generation. After MIL verification, production‑ready C code was generated using Simulink Coder (ERT) with fixed‑width types, optimized for execution and RAM efficiency. The project demonstrates a complete MBD workflow: modeling → MIL testing → SWC structuring → automatic code generation."
skills:
  - MATLAB/Simulink
  - Stateflow
  - Embedded Coder
  - Cell Balancing
  - MIL Testing
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348183229.webp
---

## Accomplishments

### 1. Stateflow Logic for 4‑Cell Passive Balancing
Designed a Stateflow chart with two states (`BalancingON`, `BalancingOFF`). The chart reads four SoC inputs (real_T), calculates the minimum SoC via `Min_SoC()`, and activates balancing resistors (SW1–SW4) for cells whose SoC exceeds the lowest by more than 0.01. The balancing decision uses a hysteresis threshold of 0.001 to avoid state chattering. Implemented helper functions `BalOFF()` and `ControlSW()` for clean separation of logic.

### 2. Software Component (SWC) Architecture
Structured the balancing algorithm as a standalone **Software Component** (model name `PassiveBalancing_SWC`) with clearly defined input ports (`SoC1`–`SoC4`) and output ports (`BalCmd`, `SW1`–`SW4`). This SWC design enables easy reuse, integration into a larger BMS software architecture, and independent code generation.

### 3. Model‑in‑the‑Loop (MIL) Testing
Created a MIL test harness in Simulink to verify the balancing logic across multiple scenarios: cells with equal SoC, cells with small differences (within 0.001), cells with large differences (0.1), and extreme cases (full vs empty). MIL testing confirmed correct state transitions, threshold behavior, and that balancing stops when all cells are within ±0.01 of the lowest SoC. This step ensured model correctness before code generation.

### 4. Automatic Code Generation & Embedded Readiness
Generated standalone C code using **Simulink Coder (ERT)** with targets for execution and RAM efficiency. The generated files (`PassiveBalancing_SWC.h/.c`, `rtwtypes.h`, `ert_main.c`) include fixed‑width types (`real_T`, `boolean_T`), a single step function, and an example main harness with overrun protection. The code uses only arithmetic operations and conditionals – no dynamic memory allocation – suitable for safety‑critical embedded BMS implementations.

### 5. Validation via Simulation (Post‑Code Generation)
After code generation, validated the generated C code against the MIL test cases (back‑to‑back testing) to ensure numerical equivalence. Simulated four cells starting at [0.60, 0.70, 0.80, 0.90] and observed that `BalCmd` stays 1.0, switches for cells 1–3 activate, and after convergence all switches turn off. The algorithm successfully balanced the pack within the defined tolerance.

## Project Gallery

{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348187101.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348190588.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348193282.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348420463.webp" height="300" %}
