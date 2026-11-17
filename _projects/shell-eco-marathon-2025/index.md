---
layout: post
title: "Shell Eco Marathon 2025"
description: "As a powertrain head for the Menofia Racing Team for Shell Eco-marathon 2025 in Qatar, I was responsible for the design, simulation, and integration of the battery system and powertrain sizing for a 3‑wheel electric prototype competing in the prototype category. The competition objective was to achieve maximum energy efficiency (km/kWh) over a 16 km track (4 laps) while complying with strict rules: battery energy ≤1 kWh, on‑board voltage ≤60 V, and a maximum time of 39 minutes. My work encompassed cell selection, battery pack configuration (14S5P), BMS integration, motor sizing via decision matrix, and vehicle performance simulation using MATLAB and Optimum‑Lap. The project resulted in a 7th place finish in the Asia‑Pacific & Middle East region and validated energy consumption of 0.6175 kWh/100 km."
skills:
  - MATLAB/Simulink
  - OptimumLab
  - AutoCAD
  - MATLAB Battery Builder Module
  - Wiring
main-image: https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335954910.webp
---

## Accomplishments

### 1. Motor Sizing & Decision Matrix Analysis
Sized the required motor power (0.46 kW peak, 0.20 kW rated) based on vehicle dynamics forces (drag force, acceleration force, rolling resistance, gradient force) and targeted **acceleration 0.278 m/s² and 30 km/h expected speed**. made a decision matrix comparing brushed, brushless, and hub motor, selecting the **350 W hub motor** for its higher efficiency (no drivetrain losses), availability, and lowest cost.

### 2. Custom Battery Pack Design (14S5P, 756 Wh)
Designed a **70‑cell Li‑ion battery pack using Samsung INR18650‑30Q** cells: **14 series** (50.4 V nominal, 58.8 V max), **5 parallel** (15 Ah, 15 A continuous). **Total energy 756 Wh**, **mass 3.36 kg**, complying with Shell Eco‑marathon rules (≤1 kWh, ≤60 V). Used Excel and MATLAB for calculations and cells decision matrix.

### 3. Smart BMS Selection & Real‑Time Data Monitoring
Selected and integrated the **Daily 100 Balance Smart BMS** (4S–17S, 60 A) featuring **active cell balancing** (1 A), over‑voltage (4.2 V/cell) and under‑voltage (2.5 V/cell) protection, over‑current limits (4 A charge / 18 A discharge), and temperature monitoring (cut‑off at 60 °C). Utilized the BMS **Bluetooth interface** for real‑time monitoring of individual cell voltages, balancing status, and current via a mobile app.

### 4. Vehicle Performance Simulation (MATLAB & Optimum‑Lap)
Modeled energy consumption and lap time using MATLAB and Optimum‑Lap. Despite Optimum‑Lap’s limitation of not supporting 3‑wheel vehicles, derived a usable drive cycle. Achieved **average cruising speed 26 km/h**, **energy consumption 0.6175 kWh/100 km**, and **estimated finishing time 36.8 minutes** for the 16 km track – meeting competition efficiency targets.

### 5. Tractive System Wiring, Circuit Schematic & Safety Documentation
Designed the complete **circuit schematic** for the tractive system, including high‑power connections from battery to motor controller, precharge circuit, and emergency shutdown paths. Documented wiring diagrams for power and signal lines, ensuring proper insulation and separation of high and low voltage. Authored the comprehensive **tractive system documentation** covering electrical design flow, system level diagram, and safety compliance. Ensured all systems passed competition scrutineering.

## Project Gallery

{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780336810950.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780336734888.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335631073.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780336959169.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335028961.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335323753.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335129617.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335149178.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335213181.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335260121.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335297356.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335397060.webp" height="300" %}
{% include image-gallery.html images="https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335722724.webp, https://akwaxnogqtinoivdfvrf.supabase.co/storage/v1/object/public/portfolio/b45cf5d8-5e0c-4699-a5f2-98786d182ac3/projects/2137/highlight_1780335512128.webp" height="300" %}
