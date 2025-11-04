---
title: SDM meets Isotopes

description: |
  The goal of the project is to develop a novel particle-based Monte-Carlo cloud microphysics model 
    resolving water isotopic composition of precipitation. 

people:
  - agnieszka_zaba
  - sylwester_arabas

image: "img/isotopes.jpg"
layout: project
last-updated: 2025-10-19
---

## Isotopic composition of water in the atmosphere
We model the evolution of stable water isotopologues 
  (e.g. $\mathrm{H_2O}$, $\mathrm{HDO}$, $\mathrm{H_2^{18}O}$, $\mathrm{H_2^{17}O}$) 
  in clouds and during precipitation.

The _super-droplet method_ (SDM) is particularly well-suited to this task 
  due to its favorable scaling with the number of particle attributes.
This allow us to extend the multi-dimensional space of attributes
  without excessive computational cost.
In addition to standard droplet properties (radius, temperature, hygroscopicity, etc.), 
  we introduce new super-droplet attributes representing the  moles of heavy isotopes 
  $(\mathrm{D}$, $\mathrm{^{17}O}$, $\mathrm{^{18}O})$.
The isotopic composition of each droplet is updated to account for fractionation effects for $\mathrm{D/H},$ $^{18}\mathrm{O}/^{16}\mathrm{O}$, and $^{17}\mathrm{O}/^{16}\mathrm{O}$.

Our two main objectives are:
 - to improve understanding of cloud microphysics, such as mixing and supersaturation, through analysis of isotope tracers, and
 - to advance hydrological and paleoclimate interpretation by applying cloud-resolving models to isotopic data (e.g. from ice cores).

We are extending PySDM, a particle-based modeling framework, 
  with support from our group’s specialists in isotope modeling, measurements, and instrumentation at AGH.

