---
title: "AIS–Camera Fusion for Maritime Vessel Monitoring"
layout: single
permalink: /projects/multi-view-detection/
author_profile: true
---

[← Back to Projects](/projects/) · Part of [Maritime Systems](/projects/maritime/)

This project focuses on combining Automatic Identification System (AIS) data with camera-based vessel perception to improve maritime situational awareness, vessel tracking, and identity association. The approach uses AIS information such as vessel position, speed, heading, and MMSI together with visual detections and trajectories extracted from video streams.

The fusion framework is designed to connect what is observed visually with what is reported through AIS. This makes it possible to maintain a more reliable understanding of vessel movement, identity, and behavior across ports, coastal waterways, and other monitored maritime environments.

### AIS–Monocular Fusion
The first part of the work uses monocular camera data together with AIS. Vessels are detected and tracked in the camera stream, while AIS positions are transformed into a common spatial representation.

Because AIS and video observations are not always perfectly synchronized, the approach I developed compares their trajectories over time rather than relying only on instantaneous position matching. Trajectory similarity, motion consistency, and temporal association are then used to link visual tracks with AIS identities.

This enables a visual vessel observation to be associated with information such as vessel identity, MMSI, speed, course, and reported trajectory, producing a fused representation of the maritime scene. The resulting framework improves vessel identification and tracking while reducing reliance on either AIS or camera observations alone.
<div style="text-align: center;"><img src="/images/maritime/ais-camera-fusion.jpg" alt="AIS-camera fusion: detected vessels annotated with MMSI, speed, course, and position" style="width:100%; max-width:860px; height:auto;"></div>

### Multi-View Vessel Detection and Tracking
The framework was extended from a single camera to multiple camera viewpoints in order to support wider-area maritime monitoring and more continuous vessel tracking.

Each camera independently performs vessel detection and multi-object tracking. Tracks observed from different viewpoints are then associated so that the same vessel can maintain a consistent identity when moving between camera coverage areas. AIS information provides an additional source for validating vessel identity and trajectory.

The resulting system combines three levels of information:

- Local vessel detection and tracking within each camera
- Cross-camera vessel association
- Global AIS-based identity and trajectory validation

This allows a vessel to be followed across multiple viewpoints instead of treating every camera observation as an independent object.
<div style="text-align: center;"><img src="/images/maritime/multi-view-diagram.jpg" alt="Multi-view detection and tracking: per-camera RT-DETR/YOLO + BoT-SORT, cross-camera association, and AIS validation" style="width:100%; max-width:860px; height:auto;"></div>
<div style="text-align: center;"><img src="/images/maritime/multi-view-real-environment.jpg" alt="Real-environment multi-view detection with AIS explorer tracks (Ports of Shimonoseki and Moji)" style="width:100%; max-width:900px; height:auto;"></div>

### Helsinki Port Case Study
As a real-world example, the framework was applied to the Port of Helsinki (West Harbour) using public harbour cameras. The same vessel is detected simultaneously from two viewpoints — the north and south harbour cameras — and localized on the harbour map, demonstrating cross-camera association and consistent vessel identity across overlapping fields of view in a live port environment.
<div style="text-align: center;"><img src="/images/maritime/helsinki-port-case-study.jpg" alt="Port of Helsinki West Harbour: the same vessel detected from the north and south cameras and localized on the map" style="width:100%; max-width:900px; height:auto;"></div>

### AIS Modality Loss and Anomaly Monitoring
A further objective of the project is to identify situations where the available sensing modalities become inconsistent.

AIS is highly valuable for maritime monitoring, but it cannot always be assumed to be continuously available or reliable. AIS information may disappear because of communication coverage limitations, equipment problems, reception gaps, or intentional changes in transmission behavior. At the same time, a vessel may remain visible to one or more cameras.

The multi-view fusion framework can therefore compare visual vessel observations against the expected AIS information. If a vessel continues to be visually tracked while its AIS information disappears, becomes inconsistent, or no longer corresponds to the observed motion, the event can be flagged for further investigation.

This provides an anomaly-awareness layer for detecting situations such as:

- AIS signal or modality loss
- Vessel observations without corresponding AIS information
- Identity inconsistencies
- Unexpected trajectory changes
- Differences between reported and visually observed vessel motion
- Potentially suspicious or abnormal maritime behavior

The system does not automatically classify such events as illicit activity. Instead, it identifies discrepancies that may require additional monitoring or operator investigation.
<div style="text-align: center;"><img src="/images/maritime/real-environment-dashboards.jpg" alt="Real-environment test dashboards: multi-view monitoring and modality-loss / anomaly awareness" style="width:100%; max-width:900px; height:auto;"></div>
<div style="text-align: center;"><img src="/images/maritime/ais-trajectory-map.jpg" alt="Data visualization of tracked vessel trajectories" style="width:100%; max-width:780px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>Data visualization of the tracked vessels illustrated in the figures.</em></p>

### Maritime Monitoring and Situational Awareness
The main advantage of the approach is that the monitoring system does not depend on a single source of information. Cameras provide direct observations of the physical environment, while AIS provides vessel identity and navigation information. Combining these complementary sources creates a more complete and robust representation of maritime traffic.

The framework can support applications such as:

- Port and harbor surveillance
- Coastal and inland-waterway monitoring
- Vessel traffic monitoring
- Critical infrastructure surveillance
- Maritime anomaly detection
- Autonomous maritime situational awareness
- Multi-sensor maritime perception systems

By combining visual perception, trajectory analysis, cross-camera tracking, and AIS information, the system can maintain better vessel identity continuity and improve awareness of what is actually happening within the monitored maritime environment.
