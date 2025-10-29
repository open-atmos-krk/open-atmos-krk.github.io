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
## pure-python, open-source implementation of the MPDATA algorithm
<b>PyMPDATA</b> is a high-perforamance Numba-accelerated Python package implementing the <it>MPDATA</it> algorithm by [Smolarkiewicz et al.](#papers-on-the-mpdata-algorithm) aimed at solving generalised convection-diffusion PDEs used in geophysical fluid dynamics and more. It numerically solves equations of form: <br> <center>
$$
\partial_t (G\psi) + \nabla \cdot (Gu\psi) + \mu \Delta (G\psi) = 0
$$ </center>
where $$\psi$$ is the advectee, $$u$$ is the advector and the $$G$$ factor describes the coordinate transformation. The last term is related to Fickian diffiusion and is optional. 
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
The package depends on [Numpy](https://numpy.org/), [Numba](https://numba.pydata.org/) and [Numba-MPI](https://pypi.org/project/numba-mpi/0.30/). This allows for taking advantage of  Just In Time compilation provided by Numba, and in case of computational clusters, distributed memory parallelism with [PyMPDATA-MPI](https://pypi.org/project/pympdata-mpi/). PyMPDATA has an example gallery available as a separate Python package, showing how it can be used to solve equations such as the [Black-Scholes](https://en.wikipedia.org/wiki/Black%E2%80%93Scholes_equation) equation, [Burgers'](https://en.wikipedia.org/wiki/Burgers%27_equation) equation and [Shallow-Water](https://en.wikipedia.org/wiki/Shallow_water_equations) equations. The project can be found on [PyPI](https://pypi.org/project/pympdata/), with its source code hosted on [GitHub](https://github.com/open-atmos/PyMPDATA), along with the [documentation and example gallery](https://open-atmos.github.io/PyMPDATA/). 

## Papers on the MPDATA algorithm
 - [Smolarkiewicz 2006 (Int. J. Numer. Methods Fluids 50)](https://doi.org/10.1002/fld.1071) - overview article
 - [Smolarkiewicz 1984 (J. Comp. Phys. 54)](https://doi.org/10.1016/0021-9991(84)90121-9)

## Papers on PyMPDATA
 - [Bartman et al. 2022 (J. Open Soruce Soft. 7)](https://doi.org/10.21105/joss.03896)
 - [Olesik et al. 2022 (Geosci. Model Dev. 15)](https://doi.org/10.5194/gmd-15-3879-20220)
 - [Magnuszewski et al. 2025 (arXiv)](https://doi.org/10.48550/arXiv.2505.24435)
