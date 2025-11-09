---
title: open-atmos-jupyter-utils
subtitle: <a href="https://pypi.org/p/open-atmos-jupyter-utils">PyPI.org/p/open-atmos-jupyter-utils</a>

description: |
  We develop and maintain utility routines for embedding vector graphics and animations in Python Jupyter notebooks 
    using matplotlib (with focus on testing and Colab & GitHub compatibility).

people:
  - agnieszka_zaba
  - michal_wronski
  - pawel_magnuszewski
  - sylwester_arabas

layout: project
no-link: true
last-updated: 2025-10-15
image: "/img/utils.jpg"
---

<p>
Ever wondered how come Jupyter defaults to raster inline graphics format (and not svg), 
  does not offer a "save as pdf/svg" button below every plot and does not offer a 
  way to include animated graphics that render on GitHub? 
Our feelings exactly! 
Here are our solutions: just replace <code><a href="https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.show.html">pyplot.show()</a></code> 
  with <code><a href="https://open-atmos.github.io/jupyter-utils/open_atmos_jupyter_utils/show_plot.html#show_plot">show_plot()</a></code> 
  and use <code><a href="https://open-atmos.github.io/jupyter-utils/open_atmos_jupyter_utils/show_anim.html#show_anim">show_anim()</a></code> for animations.
</p>

<p>open-atmos-jupyter-utils has been developed for and used in numerous Jupyter notebooks 
  in <a href="https://github.com/open-atmos/PySDM">PySDM</a>, <a href="https://github.com/open-atmos/PyMPDATA">PyMPDATA</a> and <a href="https://github.com/open-atmos/PyPartMC">PyPartMC</a> projects.
</p>

<h4>Project resources</h4>
<ul>
  <li><a href="https://open-atmos.github.io/jupyter-utils">Documentation</a></li>
  <li><a href="https://pypi.org/project/open-atmos-jupyter-utils/">PyPI package page</a></li>
  <li><a href="https://github.com/open-atmos/jupyter-utils/">GitHub repository</a></li>
</ul>

<h4>Project overview video (FOSDEM lightning talk)</h4>
<figure>
  <video controls width="640">
    <source src="https://ftp.fau.de/fosdem/2025/k1105/fosdem-2025-6674-lightning-lightning-talks.av1.webm#t=1475" type="video/webm">
    Your browser does not support the video tag.
  </video>
  <figcaption>Agnieszka Żaba presenting a <a href="https://archive.fosdem.org/2025/schedule/event/fosdem-2025-6674-lightning-lightning-talks/">lightning talk on open-atmos-jupyter-utils at FOSDEM 2025</a></figcaption>
</figure>
