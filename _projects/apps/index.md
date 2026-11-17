---
layout: post
title: "APPS"
description: "Developed a dual‑channel fault detection system for an accelerator pedal position sensor (APPS) using MATLAB/Simulink. Two opposing analog signals (0.5–4.5 V) are monitored for out‑of‑range and coherence faults. The model was verified through Model‑in‑the‑Loop (MIL) and Software‑in‑the‑Loop (SIL) with Back‑to‑Back testing to ensure equivalence. Production‑ready C code was generated with Simulink Coder (ERT) optimized for execution and RAM efficiency, suitable for automotive safety‑related applications."
skills:
  - MATLAB/Simulink
  - MIL Testing
  - SIL Testing
  - Embedded Coder
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780357418957.webp
---

## Accomplishments

### 1. Accurate Sensor Modeling & Fault Logic
- Derived the pedal transfer function: **V₁ = 4·P + 0.5** (increasing) and **V₂ = 5.0 – V₁** (decreasing).
- Implemented three fault flags using simple relational and arithmetic operations:
  - `APP_SensorFailure1` = (V₁ > 4.5) or (V₁ < 0.5)
  - `APP_SensorFailure2` = (V₂ > 4.5) or (V₂ < 0.5)
  - `APP_SensorFailureCoherency` = (V₁ + V₂ ≠ 5.0)
- Outputs are boolean_T, inputs are real_T (double) – appropriate for embedded fixed‑point conversion later.

### 2. Efficient Code Generation (ERT Target)
- Generated standalone C code using Simulink Coder with ERT target.
- Code generation objectives: **Execution efficiency** and **RAM efficiency** (no dynamic memory).
- Produced `rtwtypes.h` (fixed‑width types), `APP_SensorFailureDetection.c/.h`, and `ert_main.c` (real‑time harness with overrun protection).
- The single step function `APP_SensorFailureDetection_step()` runs periodically and can be integrated into an automotive BCM or VCU.

### 3. Rigorous Verification Workflow (MIL → SIL → Back‑to‑Back)
- **MIL:** Simulated the model with a pedal sweep (0→100%) and injected faults (open circuit, short to ground, sum mismatch). Verified correct flag activation.
- **SIL:** Compiled the generated C code on the host (x86‑64) and ran the same test vectors.
- **Back‑to‑Back:** Compared MIL and SIL outputs numerically; achieved **100% equivalence** across all scenarios, confirming the generated code faithfully implements the model logic.

## Project Gallery

{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780349078998.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780349086253.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780349063848.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2148/highlight_1780349083060.webp" height="300" %}
