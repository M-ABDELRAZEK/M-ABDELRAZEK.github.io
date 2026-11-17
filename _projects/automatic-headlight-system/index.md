---
layout: post
title: "Automatic Headlight System"
description: "Developed an automatic headlight control system using MATLAB/Simulink. The system reads ambient light (lux sensor), ignition status, and a 3‑position switch (Off/Auto/On). In Auto mode, it turns headlights ON when lux <400 (after 3 seconds debounce) or lux >1000 (fail‑safe), and OFF when lux ≥600 (after 5 seconds debounce). The final output is gated by engine status. C code was generated with Simulink Coder (ERT). MIL tests validated all modes, debounce times, and fail‑safe behavior."
skills:
  - MATLAB/Simulink
  - Embedded Coder
  - MIL Testing
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366182100.webp
---

## Accomplishments

### 1. Simulink Model with Debounced Lux Thresholds
Designed a Simulink model with two independent debouncing counters. The **Turn‑on debouncer** triggers when `Ambient_Light < 400` and confirms after 3 seconds (counter = 3). The **Turn‑off debouncer** triggers when `Ambient_Light ≥ 600` and confirms after 5 seconds (counter = 5). Debouncing eliminates headlight flickering due to transient light changes (e.g., shadows, oncoming headlights).

### 2. Fail‑Safe & Priority Logic
Implemented a fail‑safe condition: if `Ambient_Light > 1000` (sensor fault or extreme bright condition), the system forces headlights ON regardless of debouncer state. The Auto mode logic is:

- ON if (lux <400 after 3s debounce) OR (lux >1000).
- OFF if (lux ≥600 after 5s debounce).

A 3‑position `Light_Switch` (0=Off, 1=Auto, 2=On) selects the mode. The final output is ANDed with `Engine_Status` – headlights only operate when engine is running.

### 3. Automatic C Code Generation (ERT)
Generated standalone, MISRA‑style C code using **Simulink Coder** with ERT target, optimized for execution and RAM efficiency. The code includes fixed‑width types (`real_T`, `boolean_T`, `uint8_T`) from `rtwtypes.h`, a multi‑rate step function (`AHS_step1()` for control logic at 1.0s, `AHS_step0()` for future expansion at 0.01s), and an `ert_main.c` with overrun protection. No dynamic memory allocation – suitable for automotive BCM or Arduino.

### 4. Model‑in‑the‑Loop (MIL) Validation
Created a MIL test harness in Simulink to verify the model under all conditions:

- Lux sweep from 0 to 1200 and back, confirming debounce delays (ON after 3s, OFF after 5s).
- Lux step from 600 to 400 (hysteresis).
- Lux >1000 → immediate ON.
- Toggling ignition and mode switches.

MIL tests confirmed correct behavior before any code generation.

## Project Gallery

{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366185342.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366188058.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366192133.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366194891.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2151/highlight_1780366197588.webp" height="300" %}
