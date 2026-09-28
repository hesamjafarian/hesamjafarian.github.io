---
title: "COLREG-Aware Collision Intelligence"
layout: single
permalink: /projects/colreg/
author_profile: true
---

[← Back to Projects](/projects/) · Part of [Maritime Systems](/projects/maritime/)

This work focuses on interpretable collision-risk assessment and validation for autonomous maritime systems, combining vessel geometry, motion uncertainty, probabilistic trajectory prediction, COLREG reasoning, and large-scale scenario generation.
<div style="text-align: center;"><img src="/images/maritime/colreg-risk-zone.jpg" alt="Collision-risk assessment between a large vessel and an approaching craft, with detection overlay and risk zone" style="width:100%; max-width:820px; height:auto;"></div>

The approach I developed considers the main COLREG encounter types, including head-on, crossing, and overtaking situations. Vessel heading, velocity, dimensions, separation distance, and environmental conditions are systematically varied to generate thousands or millions of controlled encounter scenarios.
<div style="text-align: center;"><img src="/images/maritime/colreg-scenarios.jpg" alt="COLREG encounter types (head-on, crossing, overtaking) and large-scale scenario generation" style="width:100%; max-width:820px; height:auto;"></div>

Uncertainty in vessel state and geometry is propagated through possible future configurations using geometric representations and collision analysis to estimate where and how collision risk develops. This makes it possible to identify high-risk regions, understand which factors contribute most to the risk, and relate predicted vessel interactions to the applicable COLREG situation.

The generated scenarios also support scenario-driven validation and rare-event testing, including situations that are difficult, expensive, or unsafe to reproduce with real vessels. The framework is intended for autonomous surface vessels, maritime situational awareness, collision avoidance, and simulation-based verification using both simulated and real-world data.
