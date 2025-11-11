---
title: PySDM

description: |
  🎓 PySDM is a particle-based cloud microphysics package with box,
    parcel & 1D/2D prescribed-flow examples in Python, Julia and Matlab. 
  PySDM is a Pythonic high-performance (CPU/GPU) implementation of the Super-Droplet Method (SDM)
    Monte-Carlo scheme for collisional growth (<a href="https://doi.org/10.1002/qj.441">Shima et al. 2009</a>) 
    with original drop-breakage and adaptive-time-stepping extensions.

people:
  - piotr_bartman
  - oleksii_bulenok
  - emma_ware
  - aleksandra_strzabala
  - sanket_bhiogade
  - konrad_bodzioch
  - agnieszka_zaba
  - agnieszka_makulska
  - sylwester_arabas

layout: project
no-link: true
image: "/img/logo_pysdm.png"
---

<h3>pure-Python, open-source implementation of the SDM algorithm</h3>
<p>
<b>PySDM</b> is built around a Pythonic implementation of the Super-Droplet Method Monte-Carlo scheme for 
  coagulation (<a href="https://doi.org/10.1002/qj.441">Shima et al. 2009</a>). 
The package features two number-crunching backends: multi-threaded CPU backend using <a href="https://numba.pydata.org/">Numba</a>
  and a CUDA GPU backend using <a href="https://github.com/fynv/ThrustRTC?tab=readme-ov-file#thrustrtc">ThrustRTC</a>
  and <a href="https://github.com/fynv/CURandRTC?tab=readme-ov-file#curandrtc">CURandRTC</a>.
PySDM ships with a set of examples shipped as Jupyter-notebooks, and covering simulation setups spanning
  box-model cases, adiabatic parcel simulations, single-column and two-dimensional kinematic frameworks (see animation below).
<a href="https://open-atmos.github.io/PySDM/">Documentation of the package</a> covers the API as well as 
  tutorials exemplifying usage of PySDM from Python, Julia and Matlab.
Development of PySDM is <a href="https://github.com/open-atmos/PySDM">hosted on GitHub</a>.
</p>

<figure>
  <img src="https://github.com/open-atmos/PySDM/releases/download/tip/docs_intro_animation_ubuntu-24.04.gif" />
  <figcaption>Two-dimensional prescribed-flow warm-rain simulation using PySDM</figcaption>
</figure>

<h3>Release history and papers on PySDM</h3>
<p>PySDM v1 constituted the <a href="https://www.ap.uj.edu.pl/diplomas/141204/">MSc thesis of Piotr Bartman (Jagiellonian University, 2020)</a> who had
   developed PySDM API, adaptive numerical solvers and package architecture.
  Features and examples of PySDM v1 are summarised in a <a href="https://doi.org/10.21105/joss.03219">Bartman et al. 2022 JOSS paper</a>.
  Subsequent developments had been largely spearheaded by&nbsp;<a href="https://github.com/ekdejong">Emily de Jong</a> and 
   <a href="https://claresinger.github.io/">Clare Singer</a> during their PhD studies at the <a href="https://clima.caltech.edu">Caltech CliMA team</a>, and
   are summarised in the <a href="https://doi.org/10.21105/joss.04968">de Jong, Singer et al. 2023 JOSS paper</a>.
  The original collisional breakup scheme (maintaining the key constant-state-vector size trait of SDM)
   had been defined and validated in <a href="https://doi.org/10.5194/gmd-16-4193-2023">de Jong et al. 2023 GMD paper</a> 
   (with section 3 based on <a href="https://www.ap.uj.edu.pl/diplomas/166879/">MSc thesis of Oleksii Bulenok (Jagiellonian University, 2023)</a>).
  The original adaptive time-stepping scheme for SDM introduced in PySDM v1 has been the topic of further research
   by <a href="https://emmaware.weebly.com/">Emma Ware</a> which has been summarised in 
   <a href="https://doi.org/10.48550/arXiv.2509.05536">Ware et al. 2025 arXiv preprint</a>.
</p>

<h3>Publications using PySDM</h3>
<ul>
  <li><a href="https://doi.org/10.1029/2022MS002994">Bieli et al. 2022 (JAMES)</a>: "<em>An Efficient Bayesian Approach to Learning Droplet Collision Kernels: Proof of Concept Using “Cloudy,” a New n-Moment Bulk Microphysics Scheme</em>"</li>
  <li><a href="https://doi.org/10.1029/2022MS003186">de Jong e al. 2022 (JAMES)</a>: "<em>Spanning the Gap From Bulk to Bin: A Novel Spectral Microphysics Method</em>"</li>
  <li><a href="https://doi.org/10.5194/gmd-16-4193-2023">de Jong et al. 2023 (GMD)</a>: "<em>Breakups are complicated: an efficient representation of collisional breakup in the superdroplet method</em>"</li>
  <li><a href="https://ams.confex.com/ams/103ANNUAL/meetingapp.cgi/Paper/408596">Singer et al. 2023 (AMS Annual Meeting)</a>: "<em>Surface-Active Organics: Results from a Particle-Based Microphysics Model Calibrated with Laboratory Experiments</em>"</li>
  <li><a href="https://doi.org/10.1016/j.softx.2023.101613">D'Aquino et al. 2024 (SoftwareX)</a>: "<em>PyPartMC: A Pythonic interface to a particle-resolved, Monte Carlo aerosol simulation framework</em>"</li>
  <li><a href="https://doi.org/10.1029/2023MS004028">Azimi et al. 2024 (JAMES)</a>: "<em>Training Warm-Rain Bulk Microphysics Schemes Using Super-Droplet Simulations</em>"</li>
  <li><a href="https://doi.org/10.1029/2024MS004770">Arabas et al. 2025 (JAMES)</a>: "<em>Immersion Freezing in Particle-Based Aerosol-Cloud Microphysics: A Probabilistic Perspective on Singular and Time-Dependent Models</em>"</li>
  <li><a href="https://doi.org/10.48550/arXiv.2509.05536">Ware et al. 2025 (arXiv)</a>: "<em>Adaptive time-stepping for the Super-Droplet Method Monte Carlo collision-coalescence scheme</em>"</li>
</ul>

<h3>🎓 Student project opportunities</h3>
<ul>
  <li>Distributed-memory parallelism for PySDM using <a href="https://doi.org/10.1016/j.softx.2024.101897">Numba-MPI</a></li>
  <li>Brownian coagulation in PySDM and development of aerosol-related examples</li>
  <li>Super-particle attribute initialisation using <a href="https://en.wikipedia.org/wiki/Copula_(statistics)">copulae</a></li>
  <li>Immersion freezing and coagulation: effective freezing-temperature spectra under singular and time-dependent models</li>
  <li>Venusian cloud particle-based microphysics (e.g., using the models introduced in <a href="https://doi.org/10.1029/2025JE009177">Ando et al. 2025</a>)</li>
</ul>
