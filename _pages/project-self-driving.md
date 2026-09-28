---
title: "Autonomous Self-Driving Platform (1/10 scale)"
layout: single
permalink: /projects/self-driving/
author_profile: true
---

[← Back to Projects](/projects/)

This project focused on building a 1/10-scale autonomous driving platform as a compact testbed for computer vision, control, simulation, and sim-to-real experimentation. The idea was to create a system where perception and driving algorithms could be developed quickly and tested repeatedly without the cost and complexity of a full-size autonomous vehicle.
<div style="text-align: center;"><img src="/images/autonomous-rc-car.jpg" alt="Autonomous RC car platform: hardware, test track, and camera/sensor view" style="width:100%; max-width:820px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>The autonomous RC-car platform: hardware, indoor test track, and an example camera/sensor view.</em></p>

The vehicle uses a forward-facing camera as its main perception source. During data collection, a human operator drives the car while camera images, steering commands, and throttle values are recorded at approximately 20 Hz. This produced around 10,000 synchronized driving samples covering different positions and orientations on the track.

A convolutional neural network was trained using behavioral cloning to learn the relationship between the camera view and the corresponding steering and throttle commands. During autonomous operation, the model processes the live camera stream and continuously controls the vehicle in real time.

### Simulation and synthetic data
I also developed a simulation environment to generate additional driving data before testing on the physical platform. A virtual car could be driven with a PS4 controller while left, centre, and right camera views were recorded together with the corresponding control inputs.

The additional viewpoints were useful for learning recovery behaviour. Instead of training only on ideal centre-line driving, the dataset could include situations where the car moved toward the edge of the track and needed to steer back to a stable trajectory.

Simulation also made it possible to generate repeatable driving scenarios, experiment with different camera views, and increase the diversity of the training data without constantly using the physical vehicle.

### Vision-based autonomous driving
The project demonstrates how a relatively simple sensing setup can support a complete autonomous driving system. Rather than relying on detailed maps or a large sensor suite, the vehicle learns its driving behaviour directly from visual examples collected during manual driving.

The platform was used to explore end-to-end vision-based control, imitation learning, real-time inference, steering and throttle prediction, autonomous track following, recovery from off-centre positions, synthetic data generation, and sim-to-real transfer.

### From simulation to the physical vehicle
One of the most useful parts of the project was seeing the difference between good offline model performance and reliable behaviour on the real vehicle.

A model can perform well on recorded images but still become unstable when it controls the car itself. Small steering errors change the vehicle's position on the track, which changes the next image seen by the model and can cause errors to build up over time. Testing therefore focused on the behaviour of the complete closed-loop system rather than only on prediction accuracy.

Well-trained models were able to follow the indoor track smoothly, while weaker models could oscillate, leave the track, or fail to recover from unfamiliar positions. This highlighted the importance of training-data quality, balanced driving examples, camera consistency, and recovery samples.

Lighting was also an important factor. Changes in brightness, shadows, reflections, and camera exposure could noticeably affect a vision-only driving system, making the project a useful example of the gap between controlled training conditions and real-world operation.

### Why a small-scale platform is useful
A 1/10-scale vehicle provides a practical way to experiment with autonomous-driving concepts while preserving many of the same challenges found in larger systems, including perception uncertainty, control latency, dataset bias, changing environmental conditions, and the interaction between prediction errors and vehicle dynamics.

The project covered the full development cycle, from data collection and preprocessing to model training, simulation, real-world testing, failure analysis, and retraining. This made the platform a useful environment for hands-on development in computer vision, machine learning, autonomous control, and sim-to-real validation.
