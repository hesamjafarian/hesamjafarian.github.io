---
title: "COLREG-Aware Collision Intelligence"
layout: single
permalink: /projects/colreg/
author_profile: true
---

[← Back to Projects](/projects/) · Part of [Maritime Systems](/projects/maritime/)

This work focuses on interpretable collision-risk assessment and validation for autonomous maritime systems, combining vessel geometry, motion uncertainty, probabilistic trajectory prediction, COLREG reasoning, and large-scale scenario generation.

### Encounter types and parameters
The approach I developed considers the main COLREG encounter types, including head-on, crossing, and overtaking situations, as well as more complex cases involving converging trajectories, close-quarter situations, multi-vessel interactions, and encounters in constrained waterways. Vessel heading, velocity, dimensions, separation distance, relative bearing, turn rate, and environmental conditions are systematically varied to generate thousands or millions of controlled encounter scenarios.
<div style="text-align: center;"><img src="/images/maritime/colreg-scenarios.jpg" alt="COLREG encounter types (head-on, crossing, overtaking) and large-scale scenario generation" style="width:100%; max-width:820px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>COLREG encounter types and large-scale scenario generation.</em></p>

The framework explicitly distinguishes between give-way and stand-on responsibilities and evaluates how collision risk evolves as an encounter develops. This makes it possible to study not only whether two vessels may collide, but also when a situation becomes critical, which vessel has manoeuvring responsibility, and how much time remains for a safe corrective action.

### Geometry- and uncertainty-aware risk
Traditional indicators such as closest point of approach and time to closest point of approach can be combined with geometric and probabilistic representations of the vessels. Instead of representing a ship as a single point, the method considers vessel dimensions, orientation, safety margins, and uncertainty in future motion. This provides a more realistic description of collision risk, particularly for large vessels, asymmetric encounters, and situations where trajectories are changing.
<div style="text-align: center;"><img src="/images/maritime/colreg-risk-zone.jpg" alt="Geometric, uncertainty-aware collision-risk assessment between a large vessel and an approaching craft" style="width:100%; max-width:820px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>Geometric, uncertainty-aware collision-risk assessment between vessels.</em></p>

Uncertainty in vessel state and geometry is propagated through possible future configurations to estimate where and how collision risk develops. Position uncertainty, speed variation, heading error, delayed manoeuvres, uncertain intent, and sensor inaccuracies can all influence the predicted encounter. By modelling these effects explicitly, the framework can generate spatial risk regions and probability distributions rather than relying on a single deterministic trajectory.

### Manoeuvre analysis
Different manoeuvring behaviours can also be analysed, including course alterations, speed reductions, emergency turns, delayed reactions, and combinations of speed and heading changes. This allows alternative avoidance strategies to be compared and helps identify whether a manoeuvre actually reduces risk or simply shifts the hazardous region to another point in the encounter.

### Scenario coverage
The framework can be applied to a wide range of scenarios, including:

- head-on encounters
- port-side and starboard-side crossing encounters
- overtaking and being overtaken
- close-quarter and near-miss situations
- multiple vessels converging on the same area
- interactions between vessels with very different sizes and speeds
- manoeuvres near ports, channels, bridges, or critical infrastructure
- degraded AIS, GNSS, radar, or camera information
- delayed or uncertain vessel manoeuvres
- poor visibility and adverse weather conditions
- communication loss or incomplete knowledge of another vessel's intent

### Large-scale scenario generation and rare-event testing
An important part of the work is large-scale scenario generation. Instead of relying only on recorded traffic, encounter parameters can be systematically sampled to produce controlled datasets covering both common and rare situations. This makes it possible to test collision-risk algorithms under conditions that may occur only occasionally in real maritime traffic but are important for safety validation.

Scenario generation also supports rare-event and edge-case testing. Dangerous encounters, late evasive actions, simultaneous multi-vessel conflicts, sensor failures, and unusual vessel behaviours can be reproduced repeatedly in simulation without creating risk to real vessels or infrastructure.

### Scenario-driven verification and interpretability
The resulting framework supports scenario-driven verification of autonomous navigation and situational-awareness systems. Predicted risks and avoidance decisions can be compared against known scenario parameters, simulated ground truth, recorded vessel trajectories, or real-world sensor observations. This provides a structured way to evaluate whether an autonomous system detects risk early enough, interprets the encounter correctly, and responds consistently across a wide variety of maritime situations.

The broader objective is to provide a collision-risk representation that is not only accurate, but also interpretable. Rather than producing a single opaque risk score, the framework aims to show where the risk originates, how it evolves over time, which encounter geometry is responsible, how uncertainty affects the prediction, and how the situation relates to the applicable COLREG rules.

This makes the approach suitable for autonomous surface vessels, maritime situational awareness, collision avoidance, digital twins, simulation-based verification, operator decision support, and sim-to-real validation using both simulated and real-world data.
