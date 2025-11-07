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

## Access/storage node
The role of access node is held by a single-plate Raspberry Pi 5 computer with built-in 16GB RAM memory and 4 core CPU ARM 2.4 GHz. The power is supplied via USB. Access node is connected to the storage in a form of 2TB disk. Raspberry has only one network interface controller, so one network is connected through Ethernet wire and another one has additional USB network adapter. The Raspberry Pi is also connected to a temperature sensor through Goldpins and I/O pins. 

<figure>
    <img height="300px" src="/img/hpc-diy/access_storage_node.jpg">
    <figcaption>Access/storage node with cabling connecting to patch-panel Keystone connectors</figcaption>
</figure>

## Power supply and consumption monitoring
The external power supply is brought in through a power cable equipped with a Bluetooth module that monitors power consumption and plug in the power strip. From there USB wires are routed out. Modules that need a 230V power supply like network switch are connected directly into power strip. Minus is also routed out to ground strips. A fan is connected to power strip, ground strip and temperature sensor mentioned in the previous section. 

<figure>
    <img height="300px" src="/img/hpc-diy/power_supply.jpg">
    <figcaption>Power supply and grounding layout with ventilation fan, thermostat and temperature sensor</figcaption>
</figure>
