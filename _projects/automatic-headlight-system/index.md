---
layout: post
title: "Automatic Headlight System"
description: "An automatic headlight controller in Simulink with debounced lux thresholds, a fail-safe condition and engine-status gating, validated with MIL tests and generated as C code with Simulink Coder (ERT)."
skills:
  - MATLAB/Simulink
  - Embedded Coder
  - MIL Testing
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366182100.webp
---

## Behavior
Inputs are ambient light (lux), ignition status and a 3-position switch (Off / Auto / On). In Auto mode the headlights turn **on** when lux is below 400 for 3 seconds, or immediately when lux is above 1000 (fail-safe), and turn **off** when lux is 600 or higher for 5 seconds. The output is gated by engine status.

## Debouncing
Two independent counters (3 s turn-on, 5 s turn-off) prevent flicker from shadows or oncoming headlights.

## Code Generation
MISRA-style C code with the ERT target, fixed-width types, a multi-rate step function (1.0 s control logic, 0.01 s reserved for expansion) and no dynamic memory.

## MIL Validation
Lux sweeps from 0 to 1200 and back, a 600-to-400 step, lux above 1000, and ignition and mode switch toggling.

## Gallery
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366185342.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366188058.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366192133.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366194891.webp" height="300" %}
