---
layout: post
title: "Passive Cell Balancing - Model-Based Design"
description: "A passive balancing algorithm for a 4-cell Li-ion pack built with Simulink and Stateflow as a Software Component, tested Model-in-the-Loop and turned into production-ready C code with Simulink Coder (ERT)."
skills:
  - MATLAB/Simulink
  - Stateflow
  - Embedded Coder
  - Cell Balancing
  - MIL Testing
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348183229.webp
---

## Stateflow Logic
A chart with two states (BalancingON, BalancingOFF) reads four SoC inputs, finds the minimum SoC and activates balancing resistors SW1-SW4 for cells that exceed it by more than 0.01, with a 0.001 hysteresis threshold to prevent chattering.

## Software Component Architecture
Packaged as `PassiveBalancing_SWC` with inputs SoC1-SoC4 and outputs BalCmd and SW1-SW4, so it can be reused inside a larger BMS software architecture.

## MIL Testing
A Simulink test harness covered equal SoC, small differences, large differences (0.1) and extreme cases (full vs empty), confirming state transitions and that balancing stops once all cells are within 0.01.

## Code Generation & Validation
Generated C code with Simulink Coder (ERT), optimized for execution and RAM, with fixed-width types and no dynamic memory allocation. Back-to-back tests confirmed numerical equivalence: starting from [0.60, 0.70, 0.80, 0.90], the switches for cells 1-3 activate and turn off after convergence.

## Gallery
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348187101.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348190588.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348193282.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2147/highlight_1780348420463.webp" height="300" %}
