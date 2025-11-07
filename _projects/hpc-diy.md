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

We are building, from scratch, a multi-node GPU-enabled <a href="https://en.wikipedia.org/wiki/Computer_cluster">computing cluster</a>
  using <a href="https://en.wikipedia.org/wiki/Raspberry_Pi">Raspberry Pi</a> single-board computers and other commodity hardware.
We aim for open-source software stack (Linux/<a href="https://en.wikipedia.org/wiki/Slurm_Workload_Manager">Slurm</a>/<a href="https://en.wikipedia.org/wiki/Open_MPI">OpenMPI</a>/...).
The project is truly a team-wide effort and has multiple goals:
<ul>
  <li>to provide a fully controllable development and testing environment for our MPI-based projects:  
   <a href="https://open-atmos-krk.github.io/projects/numba-mpi.html">Numba-MPI</a> and 
   <a href="https://open-atmos-krk.github.io/projects/pympdata.html">PyMPDATA-MPI</a>;</li>
  <li>to offer a (multi)-GPU environment for the development and testing of the <a href="https://open-atmos-krk.github.io/projects/pysdm.html">PySDM</a> project;</li>
  <li>to provide a playground cluster for learning and teaching parallel computing (MPI + threading and GPUs);</li>
  <li>to build up DevOps know-how on cluster configuration and maintenance;</li>
  <li>to bring a tangible element to our software-focused research for presenting at open days and outreach events (cluster mounted on a mobile platform);</li>
  <li>last but not least, to have fun tinkering together with DIY hardware project!</li>
</ul>

## Compute nodes and interconnection network
As of the present proof-of-concept stage, we start of with two compute nodes. 
Both are off-the-shelf ARM-based <a href="https://en.wikipedia.org/wiki/Nvidia_Jetson">NVIDIA Jetson nano</a> boxes (reComputer J1010) with 4GB and 128-core CUDA GPUs.
The compute nodes and the access node are connected using a <a href="https://en.wikipedia.org/wiki/Gigabit_Ethernet">Gigabit Ethernet</a> switch.
For debugging and demonstration purposes, we use an HDMI switch and a 7-inch (800x480 pixel, TC-8589556) screen mounted inside the chasis.

<figure>
    <img width="400px" src="/img/hpc-diy/compute_nodes.jpg">
</figure>

## Access/storage node
The role of access node is held by a single-plate <a href="https://en.wikipedia.org/wiki/Raspberry_Pi#Series_and_generations">Raspberry Pi 5</a> 
  computer with built-in 16GB RAM memory and 4-core ARM 2.4 GHz CPU. 
Access node has a 16&nbsp;GB microSD memory card, and is connected via USB to a 2.5" 2TB <a href="https://en.wikipedia.org/wiki/Solid-state_drive">SSD</a> (Seagate FireCuda). 
Raspberry has only one network interface controller, so one network is connected through Ethernet wire and another one has additional USB network adapter. 
The Raspberry Pi is also connected (through goldpins) to a temperature sensor. 

<figure>
    <img width="400px" src="/img/hpc-diy/access_storage_node.jpg">
</figure>

## Power supply and consumption monitoring, thermal control, electrical wiring
The external power supply is connected to a Bluetooth power consumption meter (Voltcraft SEM6000).
A power strip with six USB ports (2.1&nbsp;A power per pair) is used to supply all components including 
  the Gigabit Ethernet switch which is connected directly into power strip. 
A 230V fan (Elmeko 10&nbsp;080&nbsp;150) is connected to the power strip through a thermostat (Siemens 8MR2171-2BB)
  which is factory-set to enable ventilation above 60C.
A temperature sensor (Joy-it SEN-DHT22 with AM2302 chip) is placed next to the thermostat to enable monitoring of the
  temperature.
We use a dedicated grounding busbar connected to the chasis, patch-panels and other metal items.

<figure>
    <img width="400px" src="/img/hpc-diy/power_supply.jpg">
</figure>

## Chasis and cable management
The system is mounted within a 9-unit <a href="https://en.wikipedia.org/wiki/19-inch_rack#10-inch_rack">10-inch rack</a>.
Most of the cabling is routed through two 12-port <a href="https://en.wikipedia.org/wiki/Patch_panel">patch-panels</a>
  with USB, Ethernet and HDMI <a href="https://en.wikipedia.org/wiki/Keystone_module">Keystone modules</a>. 

<figure>
    <img width="400px" src="/img/hpc-diy/chasis.jpg">
</figure>
