---
title: SDM meets Isotopes

description: |
  The goal of the project is to develop a novel particle-based Monte-Carlo cloud microphysics model 
    resolving water isotopic composition of precipitation. 

people:
  - agnieszka_zaba
  - sylwester_arabas

image: "/img/isotopes.jpg"
layout: project
last-updated: 2025-10-19
---

## Modelling isotopic signatures in precipitation using particle-based cloud microphysics
We model the evolution of isotopic composition of water droplets and ambient vapour.
Our focus is on stable water isotopologues: H<sub>2</sub>O, <a href="https://en.wikipedia.org/wiki/Semiheavy_water">HDO</a>, 
  <a href="https://en.wikipedia.org/wiki/Heavy_water#Heavy-oxygen_water">H<sub>2</sub><sup>18</sup>O, H<sub>2</sub><sup>17</sup>O</a>.
Among considered processes are the diffusional and collisional growth/breakage 
  of droplets and the concurrent <a href="https://en.wikipedia.org/wiki/Kinetic_fractionation">isotopic kinetic fractionation</a>.

We use the Lagrangian particle-based approach for modelling cloud microphysics.
Particle-resolved formulation, using the so-called super-droplet Monte-Carlo method, 
  offers a uniquely suitable framework 
  for simulating the isotopic fractionation in clouds and precipitation.
This is due to the ability to represent, with high fidelity, the dynamics of particles in
  a multidimensional space of attributes.

Among the attributes of super-particles are such extensive quantities 
  as mass of water per droplet,
  and the multiplicity, i.e. the number of real-world particles 
  represented by a computational super-particle.
In this project, the set of attributes is extended to include: moles of deuterium
(D), oxygen-17 (<sup>17</sup>O), and oxygen-18 (<sup>18</sup>O}.
The evolution in time of a droplet water isotopic composition is driven by
  kinetically limited diffusion processes (condensation, evaporation, 
  deposition, sublimation), and is further modulated by collision-triggered <a href="https://en.wikipedia.org/wiki/Coalescence_(physics)">coalescence</a> and breakage.

Defining and prototyping a new model of the above phenomena, 
  we use [PySDM](https://open-atmos-krk.github.io/projects/pysdm.html) -
  a Python particle-based cloud microphysics package developed and maintained in our group.

Our objective is to create a novel tool enabling:
 - usage of isotopic composition data to constrain the unknown aspects of cloud microphysical processes 
   such as evolution of supersaturation, turbulent mixing, and formation of hydrometeors;
 - improvements in methods for inferring atmospheric thermodynamic state from meteoric water 
   isotopic composition data (e.g., from ice cores). 

#### Potential BEng/MSc projects
- Extending PySDM to explicitly resolve droplet heat budget and thus capture non-equilibrium drop temperature 
  (as an alternative to the current equilibrium approximation). 

#### Acknowledgement
This project received support from
<a href="https://ncn.gov.pl/en">Polish National Science Centre</a> (SONATA grant no. <a href="https://projekty.ncn.gov.pl/en/index.php?projekt_id=499886">2020/39/D/ST10/01220</a>) and the
<a href="https://excellence.agh.edu.pl/">Excellence Initiative – Research University pragramme at the AGH University of Krakow</a> (priority research area: Water-Energy-Climate).

