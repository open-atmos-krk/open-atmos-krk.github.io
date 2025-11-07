---
title: HPC DIY
subtitle: Ceci n'est pas un superordinateur.

description: |
  We are building, from scratch, a multi-node GPU-enabled computing cluster
  using Raspberry Pi hardware, and open-source software stack (Linux/Slurm/OpenMPI/...)

people:
  - gracjan_adamus
  - michal_wronski
  - kacper_derlatka
  - aleksandra_strzabala
  - daria_klimaszewska
  - agnieszka_zaba
  - sylwester_arabas

layout: project
image: "/img/magritte.jpg"
last-updated: 2025-10-25
---

We are building, from scratch, a multi-node GPU-enabled computing cluster
  using <a href="https://en.wikipedia.org/wiki/Raspberry_Pi">Raspberry Pi</a> hardware, 
  and open-source software stack (Linux/<a href="https://en.wikipedia.org/wiki/Slurm_Workload_Manager">Slurm</a>/<a href="https://en.wikipedia.org/wiki/Open_MPI">OpenMPI</a>/...).
The project is truly a team-wide effort and has multiple goals:
<ul>
  <li>to provide a fully controllable development and testing environment for our MPI-based projects:  
   <a href="https://open-atmos-krk.github.io/projects/numba-mpi.html">Numba-MPI</a> and 
   <a href="https://open-atmos-krk.github.io/projects/pympdata.html">PyMPDATA-MPI</a>;</li>
  <li>to offer a (multi)-GPU environment for the development and testing of the <a href="https://open-atmos-krk.github.io/projects/pysdm.html">PySDM</a> project;</li>
  <li>to provide a playground cluster for teaching parallel computing courses (MPI + threading and GPUs);</li>
  <li>to build up DevOps know-how on cluster configuration and maintenance;</li>
  <li>to bring a tangible element to our software-focused research for presenting at open days and outreach events (cluster mounted on a mobile platform);</li>
  <li>last but not least, to have fun tinkering together with DIY hardware project!</li>
</ul>

## Compute nodes
As of the present proof-of-concept stage, we start of with two compute nodes. 
Both are off-the-shelf ARM-based <a href="https://en.wikipedia.org/wiki/Nvidia_Jetson">NVIDIA Jetson nano</a> boxes (reComputer J1010) with 4GB and 128-core CUDA GPUs.
The compute nodes and the access node are connected using a Gigabit Ethernet switch.
For debugging and demonstration purposes, we use an HDMI switch and a 7-inch (800x480 pixel) screen mounted inside the chasis.

<figure>
    <img width="400px" src="/img/hpc-diy/compute_nodes.jpg">
    <figcaption></figcaption>
</figure>

## Access/storage node
The role of access node is held by a single-plate Raspberry Pi 5 computer with built-in 16GB RAM memory and 4-core ARM 2.4 GHz CPU. 
The power is supplied via USB. 
Access node is connected via USB to a 2.5" 2TB SSD (Seagate FireCuda). 
Raspberry has only one network interface controller, so one network is connected through Ethernet wire and another one has additional USB network adapter. 
The Raspberry Pi is also connected (through goldpins) to a temperature sensor. 

<figure>
    <img width="400px" src="/img/hpc-diy/access_storage_node.jpg">
    <figcaption>Access/storage node with cabling connecting to patch-panel Keystone connectors</figcaption>
</figure>

## Power supply and consumption monitoring
The external power supply is connected to a Bluetooth power consumption meter (Voltcraft SEM6000).
A power strip with six USB ports is used to supply all components including 
  the Gigabit Ethernet switch which is connected directly into power strip. 
A 230V fan is connected to the power strip through a thermostat (Siemens 8MR2171-2BB)
  which is factory-set to enable ventilation above 60C.
A temperature sensor (Joy-it SEN-DHT22 with AM2302 chip) is placed next to the thermostat to enable monitoring of the
  temperature.
Grounding layout uses a dedicated copper plate and cabling connecting the chasis,
  patch-panels and other metal items.

<figure>
    <img width="400px" src="/img/hpc-diy/power_supply.jpg">
    <figcaption>Power supply and grounding layout with ventilation fan, thermostat and temperature sensor</figcaption>
</figure>

## Chasis



<figure>
    <img width="400px" src="/img/hpc-diy/chasis.jpg">
    <figcaption></figcaption>
</figure>
