---
title: "Concurrent Swarm Simulation — Multi-Boat Waypoint Navigation"
layout: single
permalink: /projects/swarm/
author_profile: true
---

[← Back to Projects](/projects/)

*Autonomous systems R&D · real-time maritime simulation*

A concurrent, multi-agent simulation in which two autonomous boats operate at the same time, each independently navigating to a sequence of target points (waypoints and buoys) on the water. Every boat is remote-controlled over its own dedicated socket, senses the target points through an onboard object-filter sensor, and is steered in real time by Python control logic — a compact model of a cooperative swarm reaching distributed goals.
<div style="text-align: center;"><img src="/images/ailivesim-swarm/swarm-waypoints-overview.jpg" alt="Aerial view of the simulated harbour with target waypoints and buoys" style="width:100%; max-width:760px; height:auto;"></div>

Within this simulation environment I generate photorealistic, physically-based multi-sensor data — RGB/EO and thermal/IR cameras, LiDAR, radar, GNSS, and AIS — and build large, automatically-labelled synthetic datasets with domain randomization across weather, lighting, and sea state. This supports scenario and rare-edge-case testing, anti-collision and situational-awareness development, and sim-to-real validation before deployment on real vessels.

### Scenario setup in the situation editor
In the situation editor I place the mission elements: the target points — waypoints and coloured buoys — that the boats must reach, and the two boats themselves (small motorboats added as "Ego" vehicles). Each boat entry references its own control-socket profile and sensor-configuration profile, so the two craft are driven and sensed independently.
<div style="text-align: center;"><img src="/images/ailivesim-swarm/situation-editor-placers.jpg" alt="Situation editor with waypoint and buoy placers for each boat" style="width:100%; max-width:760px; height:auto;"></div>
<div style="text-align: center;"><img src="/images/ailivesim-swarm/ego-boats-labeled.jpg" alt="Two ego boats underway in the scenario" style="width:100%; max-width:720px; height:auto;"></div>
<div style="text-align: center;"><img src="/images/ailivesim-swarm/boat-definition-layer-edit.jpg" alt="Boat definition referencing its control-socket and sensor profiles" style="width:100%; max-width:560px; height:auto;"></div>

### Dedicated sockets and object-filter sensors
Control and sensing for each boat run over dedicated sockets. A per-boat sensor profile attaches a filtered object getter that returns only the objects of interest — here, everything matching the waypoint filter — with their distance and position inside a fixed collection radius. Each profile declares its own socket endpoint and a name, so the running scenario is matched to the correct control process. (Socket addresses and ports are blurred in the screenshots.)
<div style="text-align: center;"><img src="/images/ailivesim-swarm/config-egovehiclesettings.png" alt="Per-boat control-socket and sensor profile files" style="width:100%; max-width:760px; height:auto;"></div>
<div style="text-align: center;"><img src="/images/ailivesim-swarm/sensor-profile-content.png" alt="Sensor profile: filtered object getter and socket endpoint" style="width:100%; max-width:460px; height:auto;"></div>
<div style="text-align: center;"><img src="/images/ailivesim-swarm/filteredobjectgetter-xml.png" alt="Object-filter rule: match waypoints, return distance and position" style="width:100%; max-width:760px; height:auto;"></div>

### Remote control in Python
A Python layer orchestrates the run: it connects to the simulation control socket, loads the scenario, opens a dedicated control socket per boat, starts threaded sensor receivers, and launches one control thread per boat. Each boat thread reads its filtered waypoint list, computes a heading toward the current target, and steers until every target is reached — after which the scenario is torn down cleanly. The architecture separates simulation state, per-vehicle status, and threaded sensor reception into clear, reusable classes.
<div style="text-align: center;"><img src="/images/ailivesim-swarm/globalfunctions-classes.png" alt="Global functions and their supporting classes" style="width:100%; max-width:760px; height:auto;"></div>
<div style="text-align: center;"><img src="/images/ailivesim-swarm/control-sequence-diagram.png" alt="Sequence diagram of the launch and control flow" style="width:100%; max-width:820px; height:auto;"></div>
<div style="text-align: center;"><img src="/images/ailivesim-swarm/class-diagrams.png" alt="Class design: simulation context, vehicle status, threaded sensor receive" style="width:100%; max-width:760px; height:auto;"></div>
