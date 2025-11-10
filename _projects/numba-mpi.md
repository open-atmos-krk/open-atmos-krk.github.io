---
title: Numba-MPI

description: |
  Numba-MPI provides Python wrappers to the C MPI API callable from within Numba JIT-compiled code and
    enabling distributed-memory parallelism. 

people:
  - kacper_derlatka
  - oleksii_bulenok
  - michal_wronski
  - sylwester_arabas

layout: project
no-link: true
image: "/img/logo_numbampi.png"
---

<p>
The Numba-MPI package enables just-in-time (JIT) compiled Python code using <a href="https://numba.pydata.org/">Numba</a> 
  to call <a href="https://en.wikipedia.org/wiki/Message_Passing_Interface">Message Passing Interface (MPI)</a>
  routines directly, allowing parallel communication without leaving compiled execution blocks.
Designed as a lightweight, NumPy-based wrapper around the MPI C API, it provides cross-platform high-performance 
  communication capabilities, bridging the gap between Python productivity and native MPI efficiency.
We have outlined the project design, features and performance in a 
  <a href="https://doi.org/10.1016/j.softx.2024.101897">SoftwareX paper (Derlatka, Manna, Bulenok, Zwicker & Arabas 2024)</a>. 
</p>

<p>
Numba-MPI has been developed by an open group of developers from Jagiellonian University in Kraków, Poland,
  from the Max Planck Institute for Dynamics and Self-Organization, Göttingen, Germany, from
  our team at the AGH University of Krakow, Poland, with much appreciated contributions from the users' community.
</p>

<p>
Numba-MPI is an optional dependency of <a href="https://pypi.org/project/py-pde/">py-pde</a> 
  and <a href="https://pypi.org/project/pympdata-mpi/">PyMPDATA-MPI</a>.
</p>

<h3>Project resources</h3>
<ul>
  <li><a href="https://numba-mpi.github.io/numba-mpi/">Documentation</a></li>
  <li><a href="https://pypi.org/project/numba-mpi/">PyPI package</a></li>
  <li><a href="https://anaconda.org/conda-forge/numba-mpi">Anaconda package</a></li>
  <li><a href="https://aur.archlinux.org/packages/python-numba-mpi">AUR package (Arch Linux)</a></li>
  <li><a href="https://github.com/numba-mpi/numba-mpi/">GitHub repository</a></li>
  <li><a href="https://zenodo.org/badge/latestdoi/316911228">Zenodo release archive</a></li>
</ul>

<h3>Project overview video (FOSDEM talk)</h3>
<figure>
  <video controls>
   <source src="https://video.fosdem.org/2023/UD2.120%20(Chavanne)/numba_mpi.webm" type="video/webm"> 
   Your browser does not support the video tag.
  </video>
  <figcaption><a href="https://archive.fosdem.org/2023/schedule/event/numba_mpi/">FOSDEM 2023 Numba-MPI talk at the HPC, Big Data, and Data Science Devroom</a></figcaption>
</figure>

<h3>Student project opportunities</h3>
<ul>
  <li>Engineering support for <code>MPI_Type_create_struct</code> (mapping to Numpy structured arrays)</li>
  <li>Redesigning the API to allow for custom JIT-compiler flags to be passed to Numba (e.g., <code>boundscheck</code>, <code>fastmath</code>, <code>nogil</code>, <code>cache</code> or <code>error_model</code>)</li>
  <li>Extending the API to support non-default communicators (for subsetting groups of processes)</li>
  <li>Engineering support for <code>MPI_IN_PLACE</code> in [<code>all</code>]<code>gather</code>/<code>scatter</code> and <code>allreduce</code></li>
  <li>Extending the test suite to include hybrid threading+MPI parallelism with performance checks</li>
</ul>
