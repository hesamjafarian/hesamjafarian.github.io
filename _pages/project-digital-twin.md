---
title: "Digital Twin & Distributed Sensing"
layout: single
permalink: /projects/digital-twin/
author_profile: true
---

[← Back to Projects](/projects/) · Part of [Maritime Systems](/projects/maritime/)

A digital twin connects a real vessel with a synchronized simulation environment, creating a virtual counterpart that reflects the vessel's position, heading, speed, motion state, and sensor information in near real time. Through a distributed communication architecture using Fast DDS, MQTT, TCP/IP, and UDP, data can flow between the physical vessel, simulation environment, sensor models, and autonomy components.

This creates a common development environment where real telemetry can be combined with simulated sensors and scenarios. RGB and thermal cameras, radar, LiDAR, AIS, GNSS, environmental sensors, and other data sources can be represented within the same virtual system, allowing the behaviour of the vessel and its perception stack to be studied under controlled conditions.
<div style="text-align: center;"><img src="/images/maritime/digital-twin-telemetry.jpg" alt="Digital twin and live telemetry integration" style="width:100%; max-width:820px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>Architecture linking live vessel telemetry with the digital twin, simulated sensors, and the AI/autonomy stack for safe, repeatable testing.</em></p>

### Why Digital Twins Matter in Maritime Systems
Testing autonomous and remotely operated vessels directly at sea is expensive, weather-dependent, time-consuming, and often difficult to repeat. Many of the most important situations are also the hardest to test safely, such as close vessel encounters, degraded navigation signals, communication loss, sensor failure, poor visibility, or emergency manoeuvres.

A digital twin provides a safe and repeatable environment for reproducing these situations before they are tested on the water. The same scenario can be executed many times while changing one parameter at a time, making it possible to understand how the vessel, sensors, and algorithms respond under different conditions.

This is especially valuable in maritime applications because the operating environment is highly variable. Vessel traffic, waves, wind, visibility, communication quality, sensor performance, and navigation conditions can change continuously. A digital twin makes these variables controllable and measurable.

### Real-to-Virtual Synchronization
Live telemetry from the vessel can be streamed into the simulation so that the virtual vessel follows the real platform in position, orientation, speed, and other available state variables. This enables:

- live visualization of vessel movement
- real-time synchronization between the physical and virtual platforms
- comparison of real and simulated trajectories
- monitoring of sensor and communication behaviour
- replay of recorded missions inside the simulation
- reconstruction of events for analysis and debugging

Recorded vessel missions can also be replayed later, allowing the same real-world event to be analysed repeatedly without returning to the test area.

### Testing Autonomy Before Going to Sea
One of the main benefits of the digital twin is the ability to test navigation and autonomy functions before deploying them on the vessel. The environment can be used to evaluate:

- waypoint navigation
- route following
- path planning
- obstacle avoidance
- collision-risk assessment
- COLREG-based decision making
- docking and harbour manoeuvres
- target search and inspection missions
- return-to-base behaviour
- remote-operation support
- autonomous mission execution

Different vessel types, speeds, headings, and traffic densities can be introduced to create controlled encounters and evaluate how the autonomy system reacts.

### Failure and Degraded-Mode Testing
Digital twins are particularly useful for situations that are unsafe or impractical to reproduce deliberately with a real vessel. Examples include:

- GNSS degradation or complete GNSS loss
- AIS loss or inconsistent AIS information
- communication interruption
- delayed sensor data
- camera failure
- radar or LiDAR degradation
- incorrect or noisy sensor measurements
- temporary loss of remote control
- actuator limitations
- unexpected vessel behaviour
- conflicting sensor observations

These scenarios can be introduced systematically to determine whether the system remains stable and whether the vessel can continue operating safely.

### Environmental and Weather Testing
Maritime perception systems are strongly affected by environmental conditions. The digital twin can therefore be used to evaluate system behaviour under a wide range of simulated environments. Examples include:

- daytime and night-time operation
- low sun and glare
- fog and reduced visibility
- rain and snow
- changing cloud cover
- different sea states
- waves and vessel motion
- wind and gusts
- varying water reflections
- different traffic densities

This is especially important when evaluating cameras, thermal imaging, radar, LiDAR, and sensor-fusion algorithms because each sensing modality reacts differently to environmental changes.

### Synthetic Multi-Sensor Data
The simulation environment can also generate synchronized synthetic sensor observations. Instead of collecting every possible condition at sea, controlled datasets can be created from simulated RGB cameras, thermal cameras, radar, LiDAR, AIS, GNSS, and other sensors. This supports:

- perception algorithm development
- object detection and tracking
- sensor-fusion development
- rare-event dataset generation
- testing under difficult weather conditions
- controlled comparison between sensing modalities

Synthetic data can then be compared with real sensor recordings to study the differences between simulation and reality.

### Sim-to-Real Validation
A key objective of the digital twin is to reduce the gap between simulation and real operation. Real vessel telemetry and sensor measurements can be compared with simulated outputs to determine where the virtual environment accurately represents the physical system and where additional modelling or calibration is required. This comparison can include:

- vessel trajectories
- acceleration and turning behaviour
- sensor observations
- detection and tracking results
- navigation decisions
- communication timing
- autonomy outputs

By continuously comparing simulation and real-world operation, models can be refined and algorithms can be validated progressively before more demanding sea trials.

### Scenario-Based Validation
The digital twin also enables structured validation rather than relying only on opportunistic field testing. A scenario library can be created covering normal operation, difficult encounters, sensor degradation, environmental disturbances, and rare edge cases. The same scenarios can then be reused whenever the navigation, perception, or control system is updated. This provides a more systematic way to answer questions such as:

- Does the vessel detect another craft early enough?
- Does tracking remain stable when visibility decreases?
- What happens if AIS disappears but the vessel remains visible?
- How does the system respond when GNSS becomes unreliable?
- Does the vessel choose a safe manoeuvre during a crossing encounter?
- Does the same algorithm behave consistently in simulation and on the real vessel?

### Closed Development and Validation Loop
Together, the real vessel and its digital twin form a continuous development loop. Telemetry and sensor data gathered on the water feed the twin, where scenarios are generated and algorithms are tested and validated, and the proven changes are deployed back to the vessel for the next round of field testing.

This allows issues discovered during field testing to be reproduced in simulation, analysed, corrected, and retested before returning to the water. The result is a safer and more efficient development process for maritime autonomy, perception, navigation, situational awareness, and remote-operation systems.
