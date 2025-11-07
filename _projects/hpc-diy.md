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
  using Raspberry Pi hardware, and open-source software stack (Linux/Slurm/OpenMPI/...).

## Access/storage node
The role of access node is held by a single-plate Raspberry Pi 5 computer with built-in 16GB RAM memory and 4 core CPU ARM 2.4 GHz. 
The power is supplied via USB. 
Access node is connected to the storage in a form of 2TB disk. 
Raspberry has only one network interface controller, so one network is connected through Ethernet wire and another one has additional USB network adapter. 
The Raspberry Pi is also connected to a temperature sensor through Goldpins and I/O pins. 

<figure>
    <img width="400px" src="/img/hpc-diy/access_storage_node.jpg">
    <figcaption>Access/storage node with cabling connecting to patch-panel Keystone connectors</figcaption>
</figure>

## Power supply and consumption monitoring
The external power supply is connected to a Bluetooth power consumption meter.
A power strip with six USB ports is used to supply all components including 
  a network switch which is connected directly into power strip. 
A 230V fan is connected to the power strip through a thermostat set to enable
  ventilation above 60C.
A temperature sensor is placed next to the thermostat to enable monitoring of the
  temperature.
Grounding layout uses a dedicated copper plate and cabling connecting the chasis,
  patch-panels and other metal items.

<figure>
    <img width="400px" src="/img/hpc-diy/power_supply.jpg">
    <figcaption>Power supply and grounding layout with ventilation fan, thermostat and temperature sensor</figcaption>
</figure>

## Compute nodes

...

<figure>
    <img width="400px" src="/img/hpc-diy/compute_nodes.jpg">
    <figcaption></figcaption>
</figure>
