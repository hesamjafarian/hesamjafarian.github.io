---
title: "Industrial Robotics & Interpretable AI"
layout: single
permalink: /projects/industrial-robotics/
author_profile: true
---

[← Back to Projects](/projects/)

I worked on industrial robotic simulation, digital twins, collision detection, and data-driven motion planning for automated work cells. The work focused on using simulation to model robot behaviour, evaluate safety, generate collision data, and test planning strategies before deployment on physical systems.

### Robotic work-cell simulation
I developed digital twins of industrial work cells, including multi-robot automotive environments with ABB manipulators, conveyors, tooling, cameras, workpieces, and safety zones.
<div style="text-align: center;"><img src="/images/industrial-robotics/industrial-robot-cell.jpg" alt="Simulated multi-robot automotive work cell with ABB manipulators" style="width:100%; max-width:760px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>Simulated multi-robot automotive work cell with ABB manipulators.</em></p>

The simulation environment was used to study robot reachability, workspace layout, multi-robot coordination, path planning, and collision-free motion. Different robot trajectories and cell configurations could be tested virtually before being transferred to a real production environment.

A key part of the work was modelling the geometry of both the robots and their surroundings so that potential collisions could be identified during motion planning.

### Collision detection and path planning
Collision detection is one of the most computationally demanding parts of robot path planning. A planner may evaluate thousands of possible robot configurations while searching for a safe route from a start pose to a target pose.

I worked with geometric collision-detection methods such as the Separating Axis Theorem and Bounding Volume Hierarchies to detect:

- robot self-collisions
- collisions with work-cell structures
- robot–tool and robot–workpiece interactions
- interference between multiple robots
- violations of safety regions

<div style="text-align: center;"><img src="/images/industrial-robotics/collision-scenario.jpg" alt="Self-collision checking for a robot manipulator in the work cell" style="width:100%; max-width:680px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>Self-collision checking.</em></p>

These geometric models provided the ground truth for evaluating robot motion and generating collision datasets.

### Learning the robot collision space
To make collision checking significantly faster, I developed data-driven models that learn the relationship between a robot's joint configuration and its collision state. Instead of repeating a full geometric collision calculation for every new configuration, the learned model can rapidly estimate whether a robot state is safe or in collision.

For a UR5 manipulator, approximately 300,000 joint-space configurations were generated and used to train an NGBoost collision model. The resulting approach increased collision-checking throughput from roughly 625 to 938,000 checks per minute, enabling much faster evaluation of candidate configurations during planning.

The probabilistic output also provides information about uncertainty, which is useful when evaluating configurations close to collision boundaries.

### Interpretable robot safety models
Another part of the work focused on making learned collision models easier to understand.
<div style="text-align: center;"><img src="/images/industrial-robotics/interpretable-collision-demo.png" alt="Interpretable collision-detection demo: collision (red) vs clear (blue) states" style="width:100%; max-width:720px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>Interpretable collision detection — collision (red) vs clear (blue) states.</em></p>

I explored shallow neural networks and rule-based models that can approximate the robot collision space while still providing insight into why a particular configuration is considered safe or unsafe. This is especially valuable in industrial robotics, where model transparency and predictable behaviour are important for safety analysis and engineering validation.

### Simulation-driven development
The overall workflow combines simulation, geometry, and machine learning:

> Digital twin → robot configuration generation → geometric collision checking → collision dataset → learned collision model → path-planning evaluation

The same simulation environment can be used to test new cell layouts, robot configurations, tools, obstacles, and planning strategies without risking physical equipment or interrupting production.

The robot models and collision datasets were developed through the Simulbotics robotics simulation platform. The work has also contributed to publications in robotics, simulation, and intelligent manufacturing — see [Publications](/publications/).
