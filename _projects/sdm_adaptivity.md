---
title: SDM Adaptive Timestepping
subtitle: <a href="https://arxiv.org/abs/2509.05536">arXiv:2509.05536</a>

description: |
  The project introduces an original adaptive time-stepping logic
    for the SDM Monte-Carlo coagulation algorithm.

people:
  - piotr_bartman
  - emma_ware
  - sylwester_arabas

layout: project
last-updated: 2025-10-24
image: "/img/adaptivesdm.jpg"
---

<p>
The original adaptive time-stepping scheme proposed herein extends the Super-Droplet Method (SDM) Monte Carlo algorithm.
In SDM, each computational particle (super droplet) stands for a weighted ensemble of real droplets, allowing for 
  detailed stochastic modeling of collision–coalescence. 
However, with a fixed timestep, the method can introduce a systematic bias which we refer to as the collision deficit,
  where too few collision events are realised compared to their statistical expectation.
</p>

<p>
The adaptive scheme dynamically adjusts the timestep to eliminate this deficit, 
  improving accuracy without compromising computational efficiency.
Validation in benchmark test cases shows that it reproduces the precision of short fixed timesteps while 
  retaining the speed of longer ones. 
Implemented in the open-source PySDM model, this approach enhances the reliability of probabilistic 
  coalescence modeling and provides a framework for more faithful representations of cloud microphysics.
</p>

<h4>Publications</h4>
<ul>
  <li><a href="https://ams.confex.com/ams/103ANNUAL/meetingapp.cgi/Paper/419078">Bartman &amp; Arabas 2023 (AMS Annual Meeting)</a>: "<em>Adaptive Time-Stepping for Particle-Based Cloud Microphysics: Super-Droplet Transport, Collisions and Condensational Growth</em>"</li>
  <li><a href="https://www.igf.fuw.edu.pl/en/seminars/presentation/adaptive-time-stepping-within-the-super-droplet-me-2024-2025-043b0a">Ware 2025 (Univ. Warsaw seminar talk)</a>: "<em>Adaptive Time-Stepping within the Super-Droplet Method Monte-Carlo Coagulation Scheme</em>"</li>
  <li><a href="https://arxiv.org/abs/2509.05536">Ware et al. 2025 (arXiv)</a>: "<em>Adaptive time-stepping for the Super-Droplet Method Monte Carlo collision-coalescence scheme</em>"</li>
</ul>
