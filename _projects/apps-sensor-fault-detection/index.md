---
layout: post
title: "APPS - Pedal Sensor Fault Detection"
description: "A dual-channel fault detection system for an accelerator pedal position sensor, verified with MIL, SIL and back-to-back testing (100% equivalence) and implemented as production-ready C code."
skills:
  - MATLAB/Simulink
  - MIL Testing
  - SIL Testing
  - Embedded Coder
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780357418957.webp
---

## Fault Logic
Two opposing analog signals (0.5-4.5 V) with V1 = 4*P + 0.5 and V2 = 5.0 - V1. Three boolean flags: `APP_SensorFailure1` and `APP_SensorFailure2` for out-of-range values, and `APP_SensorFailureCoherency` when V1 + V2 does not equal 5.0.

## Code Generation
Standalone C code with Simulink Coder (ERT), optimized for execution and RAM with no dynamic memory. A single periodic step function, `APP_SensorFailureDetection_step()`, can be integrated into a VCU or BCM.

## Verification Workflow
- **MIL:** pedal sweep (0-100%) with injected faults (open circuit, short to ground, sum mismatch).
- **SIL:** generated C code compiled on the host and run with the same test vectors.
- **Back-to-back:** MIL and SIL outputs matched with 100% equivalence.

## Gallery
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780349078998.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780349086253.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780349063848.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780349083060.webp" height="300" %}
