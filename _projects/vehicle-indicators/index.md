---
layout: post
title: "Vehicle Indicators - MIL, SIL and HIL"
description: "A complete turn-signal and hazard controller in Simulink with debouncing and hazard priority, verified through MIL, SIL and Hardware-in-the-Loop on an Arduino Uno, simulated in Proteus and deployed as generated C code."
skills:
  - MATLAB/Simulink
  - Arduino
  - Proteus
  - HIL Testing
  - Embedded Coder
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361074070.webp
---

## Logic
Three push-button inputs (Left, Right, Hazard) with a 10-step debounce counter and a state machine where Hazard has priority. Outputs are LeftIndicator and RightIndicator, blinking at 1 Hz (both together for hazard).

## Verification
- **MIL** in Simulink for debouncing, priority and blinking.
- **SIL** on the host: 100% equivalence with the model.
- **HIL** with a real Arduino Uno through the Simulink Arduino support package.

## Proteus Simulation & Deployment
The generated C code (hex file) ran on an Arduino model in Proteus with push-buttons and LEDs, then on a physical Arduino for bench validation: a full model-based design to hardware workflow.

## Gallery
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361078026.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361081374.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361084916.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361087866.webp" height="300" %}
