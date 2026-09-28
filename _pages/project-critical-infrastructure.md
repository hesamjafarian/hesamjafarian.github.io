---
title: "Critical Infrastructure Monitoring"
layout: single
permalink: /projects/critical-infrastructure/
author_profile: true
---

[← Back to Projects](/projects/) · Part of [Maritime Systems](/projects/maritime/)

This project explores a bridge-centered surveillance concept for protecting critical maritime infrastructure and improving situational awareness around sensitive waterways. Bridges, harbour approaches, navigation channels, and nearby support structures are difficult to monitor reliably with a single sensor because vessels may be partially occluded, appear at very different scales, or move through areas that are outside the field of view of an individual camera.

The approach therefore combines a simulated maritime environment with a distributed multi-camera layout. Cameras are positioned around the bridge to observe vessel approaches, bridge supports, navigation channels, exclusion zones, and other areas of operational interest. The simulation provides a controlled environment in which the complete monitoring geometry can be designed and evaluated before sensors are installed in the real world.
<div style="text-align: center;"><img src="/images/maritime/bridge-infrastructure-monitoring.jpg" alt="Bridge-based critical infrastructure monitoring with overlapping camera arrays" style="width:100%; max-width:820px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>Bridge-based critical infrastructure monitoring with overlapping camera arrays.</em></p>

### Multi-Camera Monitoring
The monitoring concept uses several cameras with partially overlapping fields of view rather than relying on a single observation point. Each camera covers a different part of the surrounding maritime area, while overlap between neighboring views provides redundancy and supports continuous observation of moving vessels.

Within each camera view, vessels can be detected and tracked over time. When a vessel approaches the boundary of one camera's coverage and enters another, cross-camera association can be used to determine that both observations correspond to the same vessel. This makes it possible to maintain a continuous vessel track across a much larger area.

Put together, monitoring begins by detecting and tracking a vessel within one camera, then links its appearances across neighbouring cameras into a single persistent identity. That continuous track is used to follow the vessel's trajectory and to flag unusual movement or events as they develop.

The multi-view approach is particularly useful around large infrastructure because structures themselves can create occlusions. A vessel hidden behind part of a bridge or outside the viewing angle of one camera may still be observable from another viewpoint.

### Camera Handover and Continuous Tracking
An important part of the concept is maintaining vessel identity as traffic moves through different camera coverage areas. Instead of creating a completely new track every time a vessel appears in another camera, information such as position, direction of travel, velocity, appearance, expected trajectory, and camera geometry can be used to associate observations across views. This enables camera-to-camera handover and produces a more continuous representation of vessel movement around the infrastructure.

For example, a vessel may first be detected several hundred metres from the bridge, move into the overlapping region of two cameras, pass underneath or alongside the structure, and later continue into another camera's coverage area. The monitoring system can preserve the vessel's trajectory throughout this transition rather than treating the observations as unrelated detections.

### Infrastructure-Aware Monitoring
The monitoring area is not treated simply as an open-water scene. The geometry of the infrastructure can be incorporated into the surveillance design. Different regions can be defined according to their importance, for example:

- bridge approaches and navigation channels
- bridge piers and support structures
- exclusion or restricted zones
- areas close to cables or other critical assets
- normal vessel transit corridors
- areas where vessels should not normally stop or loiter

This allows vessel behavior to be interpreted in relation to the infrastructure itself. A vessel following the normal navigation channel may represent ordinary traffic, while the same vessel slowing significantly, changing course toward a bridge support, entering a restricted region, or remaining close to the infrastructure for an unusual period can generate an event for further inspection.

### Simulation-Based Camera Layout Design
Simulation plays an important role because the effectiveness of a surveillance system depends strongly on where the cameras are installed. The virtual environment allows different camera positions, heights, orientations, focal lengths, fields of view, and sensing ranges to be evaluated systematically. Coverage maps can be generated to identify which areas are visible from each sensor and where blind spots remain.

Camera configurations can then be compared in terms of:

- total monitored area
- amount of overlapping coverage
- visibility of critical structures
- vessel detection distance
- expected vessel size in the image
- occlusion caused by the bridge or surrounding structures
- camera-to-camera transition regions
- remaining blind spots

This makes it possible to optimize the monitoring architecture before committing to physical installation.

### Different Traffic and Operating Conditions
The simulated environment also enables the camera network to be tested with different vessel types, sizes, speeds, trajectories, and traffic densities. Small craft, workboats, ferries, cargo vessels, and other maritime traffic can produce very different perception challenges. A small vessel far from the camera may occupy only a few pixels, while a large ship close to the bridge may extend across much of the image and temporarily occlude other objects.

Scenarios can therefore include normal transit, crossing traffic, vessels approaching from different directions, simultaneous vessels within the monitored area, stopped vessels, unusual manoeuvres, and approaches toward sensitive infrastructure. Lighting and environmental conditions can also be varied to evaluate how the surveillance configuration behaves under daylight, low light, rain, fog, snow, glare, and reduced visibility.

### Threat and Anomaly Awareness
The purpose of the monitoring system is not simply to detect vessels, but to provide contextual awareness of activity around critical infrastructure. Once a continuous vessel trajectory is available, the system can identify events that differ from normal traffic patterns, such as:

- unexpected approach toward a bridge support
- entrance into a protected area
- prolonged loitering near infrastructure
- unusual stopping or speed reduction
- unexpected changes in course
- repeated movement around the same protected region
- loss of visual tracking in a critical area
- conflicting observations between different cameras

These events can be highlighted for operator review or passed to a higher-level situational-awareness system.

### What the Project Demonstrates
The work demonstrates how simulation, infrastructure geometry, and multi-camera perception can be combined to design a practical monitoring architecture for maritime critical infrastructure. The project covers the complete concept from camera placement and coverage analysis to vessel detection, tracking, cross-camera handover, trajectory monitoring, and infrastructure-aware event detection.

The same architecture can later be extended with additional sensing modalities such as thermal cameras, radar, LiDAR, AIS, acoustic sensors, or environmental sensors, creating a broader multi-sensor monitoring system for bridges, ports, coastal infrastructure, and other strategically important maritime areas.
