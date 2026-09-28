---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

A selection of my work in autonomous systems — from the maritime autonomy stack I currently lead, through industrial robotics and interpretable AI, to the platforms where I started in real-time robotics.

<style>
.pgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;margin:26px 0 12px;}
@media(max-width:800px){.pgrid{grid-template-columns:repeat(2,1fr);}}
@media(max-width:520px){.pgrid{grid-template-columns:1fr;}}
.pcard{display:flex;flex-direction:column;background:#fff;border:1px solid #e5e7eb;border-radius:12px;overflow:hidden;text-decoration:none!important;color:inherit;box-shadow:0 1px 3px rgba(0,0,0,.06);transition:transform .15s,box-shadow .15s;}
.pcard:hover{transform:translateY(-3px);box-shadow:0 8px 22px rgba(0,0,0,.12);}
.pcard-thumb{aspect-ratio:16/10;overflow:hidden;border-bottom:1px solid #eee;}
.pcard-thumb img{width:100%;height:100%;object-fit:cover;display:block;margin:0;border:0;border-radius:0;}
.pcard-body{padding:12px 14px 14px;}
.pcard-tag{display:inline-block;background:#eaf1f8;color:#2a6db5;font-size:.72em;font-weight:600;padding:3px 9px;border-radius:999px;}
.pcard-body h3{font-size:1.0em;margin:9px 0 5px;line-height:1.3;color:#111;}
.pcard-body p{font-size:.85em;color:#555;margin:0;line-height:1.45;}
</style>
<div class="pgrid" markdown="0">
<a class="pcard" href="/projects/maritime/"><div class="pcard-thumb"><img src="/images/maritime/usva-vessel.jpg" alt="Maritime systems"></div><div class="pcard-body"><span class="pcard-tag">Maritime Autonomy</span><h3>Autonomous &amp; Remotely-Operated Maritime Systems</h3><p>USVA uncrewed vessels for Baltic critical-infrastructure protection.</p></div></a>
<a class="pcard" href="/projects/swarm/"><div class="pcard-thumb"><img src="/images/ailivesim-swarm/swarm-waypoints-overview.jpg" alt="Swarm simulation"></div><div class="pcard-body"><span class="pcard-tag">Simulation</span><h3>Concurrent Swarm Simulation</h3><p>Two autonomous boats reaching distributed targets, each on its own socket.</p></div></a>
<a class="pcard" href="/projects/multi-view-detection/"><div class="pcard-thumb"><img src="/images/maritime/real-environment-dashboards.jpg" alt="AIS-camera fusion"></div><div class="pcard-body"><span class="pcard-tag">Perception</span><h3>AIS–Camera Fusion for Vessel Monitoring</h3><p>Fusing AIS with multi-view camera perception for detection, tracking, identity, and modality-loss anomaly monitoring.</p></div></a>
<a class="pcard" href="/projects/colreg/"><div class="pcard-thumb"><img src="/images/maritime/colreg-risk-zone.jpg" alt="COLREG collision intelligence"></div><div class="pcard-body"><span class="pcard-tag">Safety</span><h3>COLREG-Aware Collision Intelligence</h3><p>Interpretable, geometry- and data-driven collision-risk assessment.</p></div></a>
<a class="pcard" href="/projects/critical-infrastructure/"><div class="pcard-thumb"><img src="/images/maritime/bridge-infrastructure-monitoring.jpg" alt="Critical infrastructure monitoring"></div><div class="pcard-body"><span class="pcard-tag">Surveillance</span><h3>Critical Infrastructure Monitoring</h3><p>Bridge camera arrays for protected zones and vessel traffic.</p></div></a>
<a class="pcard" href="/projects/digital-twin/"><div class="pcard-thumb"><img src="/images/maritime/digital-twin-telemetry.jpg" alt="Digital twin"></div><div class="pcard-body"><span class="pcard-tag">Digital Twin</span><h3>Digital Twin &amp; Distributed Sensing</h3><p>Live vessel telemetry linked to simulation.</p></div></a>
<a class="pcard" href="/projects/sim-to-real/"><div class="pcard-thumb"><img src="/images/maritime/sim-to-real-platform.jpg" alt="Sim-to-real validation"></div><div class="pcard-body"><span class="pcard-tag">Validation</span><h3>Sim-to-Real Validation</h3><p>Quantifying and closing the simulation-to-reality gap.</p></div></a>
<a class="pcard" href="/projects/industrial-robotics/"><div class="pcard-thumb"><img src="/images/industrial-robotics/industrial-robot-cell.jpg" alt="Industrial robotics"></div><div class="pcard-body"><span class="pcard-tag">Industrial Robotics</span><h3>Industrial Robotics &amp; Interpretable AI</h3><p>Digital twins and interpretable collision detection (~1000&times; faster checks).</p></div></a>
<a class="pcard" href="/projects/self-driving/"><div class="pcard-thumb"><img src="/images/car3.jpg" alt="Self-driving platform"></div><div class="pcard-body"><span class="pcard-tag">Robotics</span><h3>Autonomous Self-Driving Platform</h3><p>Behavioral-cloning autopilot on a 1/10-scale vehicle.</p></div></a>
<a class="pcard" href="/projects/robocup/"><div class="pcard-thumb"><img src="/images/ssl-simulation.jpg" alt="RoboCup"></div><div class="pcard-body"><span class="pcard-tag">Earlier Work</span><h3>RoboCup Small Size League</h3><p>Real-time control and distributed comms for autonomous soccer robots.</p></div></a>
</div>
