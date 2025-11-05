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

## Modelling isotopic signatures in precipitation using particle-based cloud microphysics
We model the evolution of isotopic composition of water droplets and ambient vapour.
Our focus is on stable water isotopologues: $\mathrm{H_2O},$ $\mathrm{HDO},$
  $\mathrm{H_2^{18}O},$ $\mathrm{H_2^{17}O}.$
Among considered processes are the diffusional and collisional growth/breakage of droplets 
  and the concurrent isotopic fractionation (including kinetic effects).

We use the Lagrangian approach for modelling cloud microphysics. 
The particle-resolved models offer a uniquely suitable framework 
  for simulating the above phenomena.
This is due to their ability to represent

The _super-droplet method_ (SDM) is particularly well-suited to this task 
  due to its favorable scaling with the number of particle attributes.
This allow us to extend the multi-dimensional space of attributes
  without excessive computational cost.
In addition to standard droplet properties (radius, temperature, hygroscopicity, etc.), 
  we introduce new super-droplet attributes representing the  moles of heavy isotopes 
  $(\mathrm{D}$, $\mathrm{^{17}O}$, $\mathrm{^{18}O})$.
The isotopic composition of each droplet is updated to account for fractionation effects for $\mathrm{D/H},$ $^{18}\mathrm{O}/^{16}\mathrm{O}$, and $^{17}\mathrm{O}/^{16}\mathrm{O}$.

Our two main objectives are related :
 - to improve understanding of cloud microphysics, such as mixing and supersaturation, 
   through analysis of isotope tracers, and
 - to develop novel tools hydrological and paleoclimate interpretation by applying cloud-resolving models 
   to isotopic data (e.g. from ice cores).

We are extending PySDM, a particle-based modeling framework, 
  with support from our group’s specialists in isotope modeling, measurements, and instrumentation at AGH.
open-source
#### Potential BEng/MSc projects
- Extending PySDM to explicitly resolve droplet heat budget and thus capture non-equilibrium drop temperature 
  (as an alternative to the current equilibrium approximation). 

#### Acknowledgement
This project received support from
<a href="https://ncn.gov.pl/en">Polish National Science Centre</a> (SONATA grant no. <a href="https://projekty.ncn.gov.pl/en/index.php?projekt_id=499886">2020/39/D/ST10/01220</a>) and the
<a href="https://excellence.agh.edu.pl/">Excellence Initiative – Research University pragramme at the AGH University of Krakow</a> (priority research area: Water-Energy-Climate).

