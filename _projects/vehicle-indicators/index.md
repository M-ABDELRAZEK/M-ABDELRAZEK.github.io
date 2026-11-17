---
layout: post
title: "Vehicle Indicators"
description: "Designed a complete vehicle indicator control system using MATLAB/Simulink logic. The model handles three push‑button inputs (Left, Right, Hazard) with debouncing and priority (Hazard overrides individual signals). Outputs are LeftIndicator and RightIndicator boolean signals, with 1Hz blinking. The model was verified through Model‑in‑the‑Loop (MIL) and Software‑in‑the‑Loop (SIL) tests, then integrated with an Arduino Uno via Hardware‑in‑the‑Loop (HIL) using Simulink’s Arduino support package. The complete system was simulated in Proteus (Arduino + LEDs + switches) to validate real‑time behavior. Production‑ready C code was generated with Simulink Coder (ERT) and deployed on the physical Arduino, demonstrating a full MBD‑to‑hardware workflow."
skills:
  - MATLAB/Simulink
  - Proteus
  - Arduino
  - Hardware Interface
  - HIL Testing
  - Arduino Support Package
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361074070.webp
---

## Accomplishments

### 1. Robust Debouncing & Priority Logic
- Implemented a debouncing subsystem using counters: each switch must remain active for 10 consecutive time steps before being recognized, preventing false triggers from mechanical bounce.
- Built a state machine that gives **Hazard** highest priority (overwrites Left/Right), then Left or Right individually.
- Used MATLAB Function blocks and If‑Action subsystems to manage the three‑way decision.

### 2. Blinking Generation
- Generated 1 Hz blinking.
- When a direction is active, the corresponding output toggles every second. Hazard activates both outputs synchronously.

### 3. MIL, SIL & HIL Testing
- Performed **MIL** simulations in Simulink to verify logic correctness (debouncing, priority, blinking).
- Executed **SIL** on the host to compare generated C code outputs against the model – achieved 100% equivalence.
- Conducted **Hardware‑in‑the‑Loop (HIL)** by connecting the Simulink model to an actual Arduino Uno (via Arduino support package), injecting real switch signals and reading LED outputs in real‑time, validating the software on target hardware without full vehicle integration.

### 4. Full System Simulation in Proteus & Code Generation
- Interfaced the Simulink model with an Arduino virtual board in **Proteus** by generating standalone C code and loading the hex file into the Proteus Arduino model.
- Simulated the complete circuit: push‑buttons (left, right, hazard) and LEDs (left/right indicators). Verified debouncing, hazard override, and correct blinking frequency in a realistic virtual environment.
- Generated production‑ready C code using **Simulink Coder (ERT)** with execution and RAM efficiency, then deployed it to a physical Arduino for on‑bench validation.

## Project Gallery

{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361078026.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361081374.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361084916.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361087866.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361091505.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361094902.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361098777.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2150/highlight_1780361101717.webp" height="300" %}
