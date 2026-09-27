---
title: "Autonomous Self-Driving Platform (1/10 scale)"
layout: single
permalink: /projects/self-driving/
author_profile: true
---

[← Back to Projects](/projects/)

A deep-learning self-driving platform (Python, based on DonkeyCar) for fast experimentation with autopilots before committing to a full-size vehicle. It uses a single forward-facing camera and a CNN trained by behavioral cloning (imitation learning): a human drives to collect ~10,000 samples — camera image, throttle, and steering — at 20 Hz, the data is cleaned, and the network learns to map images to control commands in real time.
<div style="text-align: center;"><img src="/images/car3.jpg" alt="1/10-scale autonomous car platform" style="width:100%; max-width:620px; height:auto;"></div>

I also built a simulator for synthetic data generation — driving a virtual car with three cameras (left/centre/right) via a PS4 controller — to enlarge and diversify the dataset before real-world training.
<div style="text-align: center;"><img src="/images/simulator.jpg" alt="Driving simulator for synthetic data generation" style="width:100%; max-width:620px; height:auto;"></div>

A well-fit network drives smoothly on a controlled indoor track, while an under-fit one fails — underlining how much data quality and lighting consistency matter for vision-only autopilots.
<div style="text-align: center;"><img src="/images/successful_auto_pilot.gif" alt="Trained CNN autopilot driving autonomously" style="width:100%; max-width:620px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>Trained CNN autopilot driving autonomously.</em></p>
