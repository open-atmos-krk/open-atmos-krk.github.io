---
title: PyPartMC

description: |
  PyPartMC is a C++-implemented Python interface to <a href="https://lagrange.mechse.illinois.edu/partmc/">PartMC</a>, 
    a particle-resolved Monte-Carlo code for atmospheric aerosol simulation. 
  The Python API facilitates using PartMC from Julia, Matlab, etc.

people:
  - gracjan_adamus
  - sylwester_arabas

layout: project
no-link: true
image: "/img/logo_pypartmc.png"
---

<p>
PyPartMC is a jointly developed effort between <a href="https://www.atmos.illinois.edu/~nriemer/">Nicole Riemer's group at University of Illinois Urbana-Champaign</a>,
  and our team at AGH University of Krakow, as well as an open contributor and user community.
The goal of the project is to provide a maintainable, multi-platform, and pip-installable Python interface to 
  <a href="http://compdyn.github.io/partmc">PartMC</a> — an open-source aerosol dynamics simulation framework. 
PartMC itself has been under active development for nearly two decades and has been used in computational studies 
  ranging from chamber-experiment modelling, through cloud-microphysics process studies, to large-scale air pollution modelling.
With its modular Fortran&nbsp;90 codebase and dependencies such as <a href="https://computing.llnl.gov/projects/sundials">SUNDIALS</a>, 
  <a href="https://en.wikipedia.org/wiki/NetCDF">netCDF</a>, <a href="https://doi.org/10.5194/gmd-15-3663-2022">CAMP</a>, 
  PartMC represents a robust but technically demanding HPC tool. 
PyPartMC bridges this complexity by enabling seamless interoperability between the Python ecosystem and the existing Fortran-based computational core.
</p>

<p>
The PyPartMC project aims to enhance accessibility for both seasoned PartMC users and newcomers to atmospheric modelling by simplifying 
  the previously intricate setup, compilation, and analysis workflows into a unified Python environment.
The package, distributed via <a href="https://pypi.org/">PyPI</a> in both source and binary forms for Linux, Windows, and macOS, 
  relies on a <a href="https://en.wikipedia.org/wiki/CMake">CMake-based</a> build system that statically links all dependencies. 
Its design retains the unmodified Fortran core while using <a href="https://nanobind.readthedocs.io/">nanobind</a> 
  for implementing automatic garbage collection for Fortran objects, and offering a JSON-based configuration system compatible with the original 
  Fortran-implemented custom "spec file" input API.
Comprehensive test coverage ensures maintainability of the codebase, and interoperability across platforms.
Integration with Matlab and Julia is depicted with examples included in the PyPartMC documentation.
</p>

<h3>Resources</h3>
<p>
<ul>
  <li><a href="https://github.com/open-atmos/PyPartMC/">PyPartMC GitHub repository</a></li>
  <li><a href="https://open-atmos.github.io/PyPartMC/">PyPartMC Documentation</a></li>
  <li><a href="https://pypi.org/project/PyPartMC/">PyPI PyPartMC package page</a></li>
  <li><a href="https://doi.org/10.5281/zenodo.7662635">PyPartMC Zenodo release archive</a></li>
  <li><a href="https://www.pyopensci.org/python-packages.html">pyOpenSci package listing</a> with PyPartMC included</li>
</ul>
</p>

<h3>Project publications</h3>
<p>
<ul>
  <li><a href="https://agu.confex.com/agu/fm22/meetingapp.cgi/Paper/1125642">Curtis et al. 2022 (AGU Fall Meeting, Chicago, IL, USA)</a>: "<em>PyPartMC: Aerosol model intercomparisons with particle resolved models via Python bindings to C++ and Fortran</em>"</li>
  <li><a href="https://ams.confex.com/ams/103ANNUAL/meetingapp.cgi/Paper/421645">D'Aquino et al. 2023 (AMS Annual Meeting, Denver, CO, USA)</a>: "<em>PyPartMC: a Pythonic Interface to a Particle-Resolved Monte-Carlo Aerosol Simulation Framework</em>"</li>
  <li><a href="https://archive.fosdem.org/2024/schedule/event/fosdem-2024-2338-pypartmc-engineering-python-to-fortran-bindings-in-c-for-use-in-julia-and-matlab/">Arabas et al. 2024 (FOSDEM, Université Libre de Bruxelles, Belgium)</a>: "<em>PyPartMC: engineering Python-to-Fortran bindings in C++, for use in Julia and Matlab</em>"</li>
  <li><b><a href="https://doi.org/10.1016/j.softx.2023.101613">D'Aquino et al. 2024 (SoftwareX 25)</a>: "<em>PyPartMC: A Pythonic interface to a particle-resolved, Monte Carlo aerosol simulation framework</em>"</b></li>
</ul>
</p>

<h3>Project overview talk videos</h3>
<figure>
  <iframe src="https://www.youtube-nocookie.com/embed/uZwqEpjp8xc?si=sE4VgoMQHsnBKtt1&amp;start=5587" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  <figcaption>Zach D'Aquino (UIUC) presenting on "<em>PyPartMC: A Pythonic interface to a particle-resolved Monte Carlo aerosol simulation framework</em>" at the <a href="https://airquality.ucdavis.edu/events/2023-international-aerosol-modeling-algorithms-conference">International Aerosol Modeling and Algorithms Conference 2023</a>, UCDavis, CA, USA</figcaption>
</figure>
<figure>
  <iframe src="https://www.youtube-nocookie.com/embed/PgLGlfSPE7E?si=QF8xTyhdKQ4miVbS&amp;start=135" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  <figcaption>Sylwester Arabas (AGH) presenting on "<em>PyPartMC Aerosol Dynamics Package: Engineering Python-to-Fortran Bindings in C++</em>" at the <a href="https://leap.columbia.edu/">LEAP Science and Technology Center, Columbia University, NY, USA</a></figcaption>
</figure>

<h3>Student project opportunities</h3>
<ul>
  <li>Engineering and documenting a way to use PyPartMC C++ classes as C++ bindings to PartMC Fortran codebase</li>
  <li>Engineering semi-automated binding-generation layer to reduce boilerplate Fortran and C code in PyPartMC (informed by the existing C++ abstractions)</li>
  <li>Developing a new Python package, based on PyPartMC solutions, for exposing to Python selected routines from the <a href="https://github.com/scale-met/scale/">RIKEN SCALE</a> Fortran codebase</li>
</ul>
