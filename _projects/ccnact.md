---
title: ccnact

description: |
  KISS SciPy-based CCN activation model 

people:
  - agnieszka_zaba
  - sylwester_arabas

layout: project
image: "/img/ccnact.png"
---
[![github-ccnact](https://img.shields.io/badge/github-ccnact-blue?logo=github)](https://github.com/open-atmos-krk/ccnact)

Single-file KISS-engineered Python package offering adiabatic parcel model with moving-sectional/point-particle
  representation of cloud condensation nuclei (CCN) activation process, i.e. the key mechanism responsible for
  formation of cloud droplets in the atmosphere.
The package is lightweight in dependencies - depends on [SciPy](https://scipy.org/),
  [NumPy](https://numpy.org/) & [Pint](https://pint.readthedocs.io/) only.
It offers sub-second execution times for typical parameter settings, and allows for 
  using user-defined values for all constants use in the model.
The source code is written leveraging dimensional analysis abstractions thus 
  allowing to ensure at test time that all arithmetic expressions are valid in terms of physical dimensions, 
  while not incurring any overhead outside of the test session scope.

<h3>🎓 Student project opportunities</h3>
<ul>
  <li>speed up integration by replacing finite-difference Jacobian with an analytic formulation</li>
  <li>engineer a workflow for constructing climate-model CCN activation parameterisation using ccnact</li>
</ul>

<br />
