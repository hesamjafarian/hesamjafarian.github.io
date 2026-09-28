---
title: "Autonomous & Remotely-Operated Maritime Systems"
layout: single
permalink: /projects/maritime/
author_profile: true
---

[← Back to Projects](/projects/)

*2025 – present · Autonomous Intelligent Systems Lab (AISLab), Turku*

The USVA project (*Uncrewed Surface Vessels for Automated Maritime Critical Infrastructure Protection*) focuses on developing autonomous and remotely operated surface vessels for monitoring marine areas and protecting critical seabed infrastructure in the Baltic Sea. Coordinated by Turku UAS and funded by Business Finland with approximately €1.3 million, the project combines autonomous vessel development, simulation, digital twins, multi-sensor perception, and real-world field testing on operational platforms.

Within the project, my work focuses on the design and integration of autonomous vessel systems, data-collection pipelines, simulation environments, and sim-to-real validation. This includes developing monitoring concepts for critical maritime infrastructure, integrating sensors such as RGB and thermal cameras, LiDAR, radar, GNSS, and AIS, and building digital-twin environments for testing perception, navigation, and situational-awareness algorithms before deployment at sea. The simulation and real-world platforms are used together to evaluate sensor behavior, generate and collect data, validate autonomy functions, and improve the transfer of algorithms from virtual environments to operational vessels.

### Real platforms
The USVA pilot vessel is a 14-metre Watercat M12, formerly operated by the Finnish Navy and adapted with Marine Alutech for remote and autonomous operation. The vessel can be controlled from shore-based stations and provides a full-scale platform for developing and validating maritime autonomy, situational awareness, environmental monitoring, and underwater inspection capabilities. The platform is also used to study operation under degraded GNSS and communication conditions, as well as navigation and collision-avoidance behaviour in accordance with COLREG requirements.
<div style="text-align: center;"><img src="/images/maritime/usva-vessel.jpg" alt="USVA remotely-operated pilot vessel (Watercat M12)" style="width:100%; max-width:660px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>The USVA pilot vessel, a 14 m Watercat M12 adapted for remote operation. Photo: Turku UAS / USVA project.</em></p>

The lab's electric research vessel, eM/S Salama, serves as a complementary on-water test platform for sensor integration, data collection, system validation, and sim-to-real testing. Together, the two vessels provide different operating characteristics and testing scales, allowing algorithms and sensing systems to be evaluated across a broader range of maritime scenarios.
<div style="text-align: center;"><img src="/images/maritime/ems-salama.jpg" alt="eM/S Salama electric research vessel" style="width:100%; max-width:660px; height:auto;"></div>
<p style="text-align: center; font-size: 0.85em; color: #888;"><em>eM/S Salama, the lab's electric research vessel. Photo: Turku UAS.</em></p>

The development and validation work considers diverse vessel traffic, including vessels of different types, dimensions, speeds, headings, and manoeuvring characteristics. Test scenarios cover encounters such as crossing, overtaking, head-on approaches, close-range interactions, and operations around ports and critical infrastructure. Particular attention is given to how perception and tracking performance change as target vessels become smaller, more distant, partially occluded, or move at different relative speeds.

Environmental robustness is another important part of the work. Simulation and real-world data are used to assess sensing and autonomy under changing daylight, night-time operation, rain, fog, snow, glare, sea-state variation, wind, waves, and reduced visibility. These conditions affect RGB and thermal cameras, radar, LiDAR, GNSS, AIS, and other sensing modalities differently, making multi-sensor integration essential for maintaining reliable situational awareness.

By combining controlled simulation with data collected from real vessels, difficult and safety-critical conditions can be reproduced repeatedly before being tested on the water. This supports systematic evaluation of sensor coverage, detection range, tracking stability, communication loss, GNSS degradation, environmental disturbances, and interactions with different types of maritime traffic, ultimately improving the transfer of perception and autonomy functions from simulation to real operational environments.

In the media: [Yle](https://yle.fi/a/7-10104914) · [Kauppalehti](https://www.kauppalehti.fi/uutiset/a/2e27af04-232b-4904-b1d2-6ebdb9b342e9) · [Helsingin Sanomat](https://www.hs.fi/suomi/art-2000012256364.html)

### Explore the maritime work
- [Multi-View Vessel Detection & Tracking](/projects/multi-view-detection/)
- [COLREG-Aware Collision Intelligence](/projects/colreg/)
- [Critical Infrastructure Monitoring](/projects/critical-infrastructure/)
- [Digital Twin & Distributed Sensing](/projects/digital-twin/)
- [Sim-to-Real Validation](/projects/sim-to-real/)
