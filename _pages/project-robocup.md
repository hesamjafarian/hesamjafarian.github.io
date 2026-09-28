---
title: "RoboCup Small Size League (2009–2011)"
layout: single
permalink: /projects/robocup/
author_profile: true
---

[← Back to Projects](/projects/)

As a member of the MRL Small Size League team, I worked on a high-speed autonomous multi-robot system designed for RoboCup soccer. The objective of the platform was to coordinate a team of small mobile robots in a highly dynamic environment where perception, decision-making, communication, and motion control all had to operate in real time.

A key part of the system was the overhead vision architecture. Cameras mounted above the playing field provided a global view of the robots, opponents, and ball. The vision system converted these images into field coordinates, allowing the central computer to continuously estimate positions, orientations, and movement across the entire game area. This centralized perception concept is characteristic of the RoboCup Small Size League, where field objects are tracked by an overhead vision system and the resulting information is processed by off-field computers.
<div style="text-align: center;"><img src="/images/robocup2010_mrl.jpg" alt="MRL at RoboCup 2010" style="width:100%; max-width:600px; height:auto;"></div>

The central computer used this global state to run the team AI, including tactical decision-making, role assignment, path planning, obstacle avoidance, and multi-robot coordination. Based on the current game situation, motion commands were generated for each robot and transmitted wirelessly to the team. This architecture allows several robots to behave as a coordinated system rather than as independent units, which is one of the main research challenges of the Small Size League.

A simulation of the Small Size League environment supported development and testing of team strategy, multi-robot coordination, and control before running on the physical robots. It models the field, goals, ball, and the full team of omni-directional robots, allowing tactics and behaviors to be evaluated in a repeatable virtual setting.
<div style="text-align: center;"><img src="/images/ssl-simulation.jpg" alt="Simulation of the Small Size League field with the MRL team of omni-directional robots" style="width:100%; max-width:700px; height:auto;"></div>

At the robot level, the work focused on real-time sensing, motion control, and distributed hardware/software integration. The electronics combined an ARM processor with an Altera Cyclone FPGA, with computationally parallel and timing-critical tasks such as motor control and PID execution handled at the FPGA level. The 2010 redesign centered on an ARM-plus-FPGA architecture and a new wireless system for the low-level robot platform.
<div style="text-align: center;"><img src="/images/mrl_robot.png" alt="MRL Small Size League robot" style="width:100%; max-width:480px; height:auto;"></div>

The overall control loop can be summarized as:

> Overhead cameras → global object localization → team AI and strategy → path and motion generation → wireless robot commands → FPGA/ARM motor control → robot motion

This created a fast closed-loop autonomous system capable of continuously observing the environment, deciding how the team should react, and executing coordinated movement across multiple robots.

### Main objectives

- Real-time localization of robots and the ball using overhead cameras
- Centralized world-state estimation from global visual information
- Multi-agent strategy and coordinated team behavior
- Dynamic path planning and obstacle avoidance
- High-frequency wireless command distribution
- Precise omni-directional motion and motor control
- FPGA-based execution of time-critical control tasks
- Integration of perception, AI, communications, electronics, and mechanics into a complete autonomous robotic system

The broader goal was not simply to build soccer-playing robots, but to investigate how multiple autonomous agents can perceive a shared environment, coordinate decisions, communicate efficiently, and execute precise motion under strict real-time constraints.

MRL placed 1st at the national RoboCup and 3rd at the RoboCup 2010 world championship:

| Place | Team |
|:-----:|------|
| 1 | Skuba |
| 2 | CMDragons |
| 3 | MRL |
| 4 | KIKS |
