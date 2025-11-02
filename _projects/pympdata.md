---
title: PyMPDATA
subtitle: <a href="https://pypi.org/p/pympdata">PyPI.org/p/PyMPDATA</a>

description: |
  PyMPDATA is a Numba-accelerated Pythonic implementation of the MPDATA algorithm of Smolarkiewicz et al. 
    used in geophysical fluid dynamics and beyond for numerically solving generalised convection-diffusion PDEs.
  PyMPDATA ships with examples in Python, Julia, Rust and Matlab.

people:
  - piotr_bartman
  - michael_olesik
  - michal_wronski
  - pawel_magnuszewski
  - kacper_derlatka
  - sylwester_arabas

layout: project
no-link: true
last-updated: 2025-10-10
image: "/img/logo_pympdata.png"
---
<script type="text/javascript" async
     src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>
## pure-Python, open-source implementation of the MPDATA algorithm
<b>PyMPDATA</b> is a high-perforamance Numba-accelerated Python package implementing the <it>MPDATA</it> algorithm by [Smolarkiewicz et al.](#papers-on-the-mpdata-algorithm) 
  aimed at solving generalised advection-diffusion PDEs in geophysical fluid dynamics and beyond.
It numerically solves equations of form: <br> <center>
  $$
  \partial_t (G\psi) + \nabla \cdot (G\vec{u}\psi) + \mu \Delta (G\psi) = 0
  $$ </center>
  where $$\psi$$ is the advectee, $$u$$ is the advector and the $$G$$ factor describes the coordinate transformation. 
The last term is related to Fickian diffiusion and is optional. 
The crux of the method lies in iterative application of the [upwind scheme](https://en.wikipedia.org/wiki/Upwind_scheme). 
The first iteration employs the advective velocity $$\vec{u}$$, while each subsequent iteration employs a so-called antidiffusive velocity which 
  corrects solution from prior iteration reducing the [numerical diffusion](https://en.wikipedia.org/wiki/Numerical_diffusion). 
The antidiffusive velocities are formulated through modified equation analysis of the upwind scheme and feature cross-dimensional dependencies 
  (i.e., applying MPDATA in multiple dimensions is not equivalent to application of one-dimensional MPDATA in all dimensions), 
  the scheme is thus not [dimensionally split](https://en.wikipedia.org/wiki/Strang_splitting), hence "M" in the algorithm name. 
Since each iteration of the scheme constitutes a [forward-in-time](https://en.wikipedia.org/wiki/Explicit_and_implicit_methods) upwind pass, the scheme inherits characteristics of the upwind scheme: 
  [CFL stability criterion](https://en.wikipedia.org/wiki/Courant%E2%80%93Friedrichs%E2%80%93Lewy_condition), conservativeness, embarrassingly parallel domain decomposition, and sign-preservation. 
For non-negative fields $$\psi$$, sign-preservation translates to [positive definiteness](https://en.wikipedia.org/wiki/Positive-definite_function), hence the "PD" in the algorithm name. 
Application of the corrective iterations improves scheme [convergence rate](https://en.wikipedia.org/wiki/Rate_of_convergence) compared with first-order upwind. 
<center>
<div style="display:flex; align-items:center; justify-content: center;">
<figure>
    <p style="margin-bottom:50px"> </p>
    <img height="300px" src="https://github.com/open-atmos/PyMPDATA/releases/download/tip/n_iters.3_rank_0_size_1_c_field_.0.5.0.25._mpi_dim_0_n_threads_3-CartesianScenario-anim.gif">
	<p style="margin-bottom:50px"> </p>
	<figcaption><b>Fig 1.</b> : Basic 2D advection</figcaption>
</figure>
<figure>
    <img height="400px" src="https://github.com/open-atmos/PyMPDATA/releases/download/tip/boussinesq_2d_anim.gif">
	<figcaption><b>Fig 2.</b> : Burgers equation example</figcaption>
</figure>
</div>
</center>
The package depends on [Numpy](https://numpy.org/), [Numba](https://numba.pydata.org/) and [Numba-MPI](https://pypi.org/project/numba-mpi/). 
This allows for taking advantage of Just-In-Time (JIT) compilation provided by Numba, and in case of computational clusters, distributed memory parallelism 
  with [PyMPDATA-MPI](https://pypi.org/project/pympdata-mpi/). 
PyMPDATA has an example gallery available as a separate Python package, showing how it can be used to solve equations such as 
  the [Black-Scholes](https://en.wikipedia.org/wiki/Black%E2%80%93Scholes_equation) equation, 
  [Burgers'](https://en.wikipedia.org/wiki/Burgers%27_equation) equation and 
  [Shallow-Water](https://en.wikipedia.org/wiki/Shallow_water_equations) equations. 
The project can be found on [PyPI](https://pypi.org/project/pympdata/), with its source code hosted on [GitHub](https://github.com/open-atmos/PyMPDATA), 
  along with the [documentation and example gallery](https://open-atmos.github.io/PyMPDATA/). 

## Selected papers on the MPDATA algorithm (features implemented in PyMPDATA)
 - [Smolarkiewicz 1983 (Mon. Weather Rev. 111)](https://doi.org/10.1175/1520-0493(1983)111%3C0479:ASPDAS%3E2.0.CO;2): "<em>A Simple Positive Definite Advection Scheme with Small Implicit Diffusion</em>" 
 - [Smolarkiewicz 1984 (J. Comp. Phys. 54)](https://doi.org/10.1016/0021-9991(84)90121-9): "<em>A fully multidimensional positive definite advection transport algorithm with small implicit diffusion</em>"
 - [Smolarkiewicz & Grabowski 1990](https://doi.org/10.1016/0021-9991(90)90105-A): "<em>The multidimensional positive definite advection transport algorithm: nonoscillatory option</em>"
 - [Smolarkiewicz & Margolin 1998 (J. Comp. Phys. 140)](https://doi.org/10.1006/jcph.1998.5901): "<em>MPDATA: A Finite-Difference Solver for Geophysical Flows</em>"
 - [Smolarkiewicz 2006 (Int. J. Numer. Methods Fluids 50)](https://doi.org/10.1002/fld.1071): "<em>Multidimensional positive definite advection transport algorithm: an overview</em>"
 - [Margolin & Shashkov 2006 (Int. J. Numer. Methods Fluids 50)](https://doi.org/10.1002/fld.1070): "<em>MPDATA: gauge transformations, limiters and monotonicity†</em>"
 - [Jaruga et al. 2015 (Geosci. Model Dev. 8)](https://doi.org/10.5194/gmd-8-1005-2015): "<em>libmpdata++ 1.0: a library of parallel MPDATA solvers for systems of generalised transport equations</em>"

## Papers on or using PyMPDATA
 - [Bartman et al. 2022 (JOSS 7)](https://doi.org/10.21105/joss.03896): "<em> PyMPDATA v1: Numba-accelerated implementation of MPDATA with examples in Python, Julia and Matlab</em>"
 - [Olesik et al. 2022 (Geosci. Model Dev. 15)](https://doi.org/10.5194/gmd-15-3879-20220): "<em>On numerical broadening of particle-size spectra: a condensational growth study using PyMPDATA 1.0</em>"
 - [Derlatka et al. 2024 (SoftwareX 28)](https://doi.org/10.1016/j.softx.2024.101897): "<em>Numba-MPI v1.0: Enabling MPI communication within Numba/LLVM JIT-compiled Python code</em>"
 - [Magnuszewski et al. 2025 (arXiv)](https://doi.org/10.48550/arXiv.2505.24435): "<em> Path-dependent option pricing with two-dimensional PDE using MPDATA</em>"

## Potential MSc projects
 - [traffic flow](https://en.wikipedia.org/wiki/Macroscopic_traffic_flow_model) dynamics with PyMPDATA
 - [immersed boundary method](https://en.wikipedia.org/wiki/Immersed_boundary_method) with PyMPDATA
 - [fully third-order MPDATA](https://doi.org/10.1016/j.jcp.2018.01.005) variant for PyMPDATA
 - coupling PyMPDATA's Boussinesq solver with [PySDM](https://open-atmos-krk.github.io/projects/pysdm.html) to simulate convective cloud
 - [shallow-water equations](https://en.wikipedia.org/wiki/Shallow_water_equations) on a sphere using PyMPDATA
