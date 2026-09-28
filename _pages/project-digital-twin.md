---
title: "Digital Twin & Distributed Sensing"
layout: single
permalink: /projects/digital-twin/
author_profile: true
---

[← Back to Projects](/projects/) · Part of [Maritime Systems](/projects/maritime/)

A digital twin connects live vessel telemetry with a synchronized simulation environment through a distributed communication architecture using Fast DDS, MQTT, TCP/IP, and UDP. The platform combines real vessel state information with simulated sensors and scenarios, enabling safe and repeatable testing of perception, navigation, autonomy, and decision-support algorithms before deployment on the water. It also supports sim-to-real validation by comparing real telemetry with simulated behavior and AI outputs under both normal and challenging operating conditions.
<div style="text-align: center;"><img src="/images/maritime/digital-twin-telemetry.jpg" alt="Digital twin and live telemetry integration" style="width:100%; max-width:760px; height:auto;"></div>

The architecture is built around distributed communication using Fast DDS, MQTT, TCP/IP, and UDP, enabling data exchange between the physical vessel, simulation environment, sensor models, and AI components. This creates a flexible platform where real telemetry can be combined with synthetic sensor data such as RGB, thermal, AIS, GNSS, radar, or other simulated observations.

The digital twin provides a safe environment for testing perception, navigation, autonomy, and decision-support algorithms before deploying them on the vessel. Real operational data can be replayed or synchronized with simulated scenarios, while difficult or safety-critical situations can be reproduced repeatedly without exposing the vessel or surrounding traffic to unnecessary risk.

The platform also supports sim-to-real validation by comparing simulated behavior, sensor outputs, and AI predictions against real telemetry. This helps identify differences between the virtual and physical environments and improves confidence in algorithms before real-world trials.

Together, the live vessel and digital twin form a closed development and validation loop supporting:

- real-time vessel visualization and state synchronization
- distributed sensor and telemetry integration
- synthetic multi-sensor data generation
- AI and autonomy testing
- navigation and COLREG scenario validation
- repeatable edge-case and adverse-condition testing
- sim-to-real comparison and validation
- real-world maritime situational awareness
