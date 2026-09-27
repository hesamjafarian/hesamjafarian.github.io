---
title: "Industrial Robotics & Interpretable AI"
layout: single
permalink: /projects/industrial-robotics/
author_profile: true
---

[← Back to Projects](/projects/)

*2018 – 2026 · Tampere University · STEM SAS*

Across industrial R&D I build digital twins of robotic work cells and develop interpretable, data-driven AI for robot safety and collision detection.

### Robotic work-cell simulation
I model complete industrial work cells — for example, multi-robot automotive lines with ABB welding manipulators operating around a car body on a conveyor — including kinematic robot models, tooling (grippers, welding torches), cameras, and safe-zone layouts. These digital twins drive path-planning, route-optimization, and 3D geometric collision-detection (Separating Axis Theorem, Bounding Volume Hierarchies) before anything runs on a real line.
<div style="text-align: center;"><img src="/images/industrial-robotics/industrial-robot-cell.jpg" alt="Simulated multi-robot automotive work cell with ABB manipulators" style="width:100%; max-width:760px; height:auto;"></div>
<div style="text-align: center;"><img src="/images/industrial-robotics/collision-scenario.jpg" alt="Collision-detection scenario: robot arm near a car body on the conveyor" style="width:100%; max-width:680px; height:auto;"></div>

### Learning-based, interpretable collision detection
Classical collision detection recomputes scene geometry at every step — the main bottleneck for real-time, collision-free path planning. I replace those expensive checks with data-driven models that approximate the collision space:
- A Natural Gradient Boosting (NGBoost) model trained on ~300,000 UR5 joint-space samples raised collision-checking throughput from ~625 to ~938,000 checks per minute — about a 1000× speed-up — with calibrated, probabilistic outputs suited to sampling-based planners.
- Shallow artificial neural-network topologies that collapse the collision pipeline into a compact, fast predictor.
- Rule-based, interpretable models that make each collision decision explainable rather than a black box.
<div style="text-align: center;"><img src="/images/industrial-robotics/interpretable-collision-demo.png" alt="Interpretable collision-detection demo: collision (red) vs clear (blue) states" style="width:100%; max-width:720px; height:auto;"></div>

The robot models and collision datasets are built and shared through the Simulbotics robotics simulation platform. Earlier, I also developed ML models for quality prediction in metal additive manufacturing. This work is published at the RSS and AHFE workshops and in ASME and IEEE venues — see [Publications](/publications/).
