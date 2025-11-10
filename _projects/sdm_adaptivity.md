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
image: "/img/adaptivesdm.jpg"
---

<p>
The original adaptive time-stepping scheme proposed herein extends the Super-Droplet Method (SDM) Monte Carlo algorithm.
In SDM, each computational particle (super droplet) stands for a weighted ensemble of real droplets, allowing for 
  detailed stochastic modelling of collisional coalescence and breakage. 
However, with a fixed timestep, the method can introduce a systematic bias which we refer to as the collision deficit,
  where too few collision events are realised compared to their statistical expectation.
</p>

<p>
The adaptive scheme dynamically adjusts the timestep to eliminate this deficit, 
  improving accuracy without compromising computational efficiency.
Validation in benchmark test cases shows that it reproduces the precision of short fixed timesteps while 
  retaining the speed of longer ones. 
Implemented in the open-source <a href="https://open-atmos-krk.github.io/projects/pysdm.html">PySDM</a> 
  and <a href="https://github.com/emmacware/droplets.jl">Droplets.jl</a> packages, 
  this approach enhances the reliability of probabilistic 
  coalescence modelling and provides a framework for more faithful representations of cloud microphysics.
</p>

<h3>Presentations and publications on the adaptive time-stepping for SDM</h3>
<ul>
  <li><a href="https://www.igf.fuw.edu.pl/en/seminars/presentation/pysdm-pythonic-particle-based-cloud-microphysics-2020-20211/">Bartman 2020 (Atmospheric Physics Seminar talk, Univ. Warsaw, Poland)</a>: "<em>PySDM: Pythonic particle-based cloud microphysics package</em>"</li>
  <li><a href="https://ams.confex.com/ams/103ANNUAL/meetingapp.cgi/Paper/419078">Bartman &amp; Arabas 2023 (AMS Annual Meeting, Denver, CO, USA)</a>: "<em>Adaptive Time-Stepping for Particle-Based Cloud Microphysics: Super-Droplet Transport, Collisions and Condensational Growth</em>"</li>
  <li><a href="https://www.igf.fuw.edu.pl/en/seminars/presentation/adaptive-time-stepping-within-the-super-droplet-me-2024-2025-043b0a">Ware 2025 (Atmospheric Physics Seminar talk, Univ. Warsaw, Poland)</a>: "<em>Adaptive Time-Stepping within the Super-Droplet Method Monte-Carlo Coagulation Scheme</em>"</li>
  <li><a href="https://arxiv.org/abs/2509.05536">Ware, Bartman-Szwarc et al. 2025 (arXiv e-print)</a>: "<em>Adaptive time-stepping for the Super-Droplet Method Monte Carlo collision-coalescence scheme</em>"</li>
</ul>
