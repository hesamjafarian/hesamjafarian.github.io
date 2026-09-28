---
title: "RoboCup Small Size League (2009–2011)"
layout: single
permalink: /projects/robocup/
author_profile: true
---

[← Back to Projects](/projects/)

I worked on a high-speed autonomous multi-robot platform for RoboCup, where several omni-directional robots had to perceive the field, coordinate as a team, avoid obstacles, and react to a fast-changing game in real time. The project combined computer vision, multi-agent decision-making, path planning, wireless communication, embedded control, and simulation in one complete robotic system.

A set of overhead cameras provided a global view of the field, tracking the robots, opponents, and ball. The vision system converted these observations into field coordinates and continuously estimated position, orientation, velocity, and movement. This shared world model was then used by the central computer for role assignment, tactical decisions, path planning, and coordinated team behaviour.
<div style="text-align: center;"><img src="/images/ssl-simulation.jpg" alt="Simulation of the Small Size League field with a team of omni-directional robots" style="width:100%; max-width:700px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>Simulation of the Small Size League field, used to develop and test the team.</em></p>

At the robot level, the platform used ARM processing together with an Altera Cyclone FPGA. The FPGA handled timing-critical tasks such as motor control and PID execution, while the higher-level control and communication were managed by the embedded processor. Commands were transmitted wirelessly to the robots at roughly 60 updates per second, allowing the team to react quickly to changes in the field.
<div style="text-align: center;"><img src="/images/ssl-robot.png" alt="An omni-directional Small Size League robot with FPGA/ARM electronics" style="width:100%; max-width:480px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>One of the omni-directional robots (FPGA/ARM electronics).</em></p>

A simulation environment was also used to develop and test strategy, coordination, obstacle avoidance, and control before running new behaviours on the physical robots. This made it possible to reproduce game situations, refine algorithms, and reduce development time on the real platform.

The project gave me hands-on experience with the full autonomous robotics stack, from perception and world modelling to multi-robot coordination, embedded control, and physical execution. The team placed 1st in the national RoboCup competition and 3rd in the RoboCup 2010 Small Size League world championship.
<div style="text-align: center;"><img src="/images/robocup2010.jpg" alt="At the RoboCup 2010 Small Size League world championship" style="width:100%; max-width:600px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>At the RoboCup 2010 world championship.</em></p>
