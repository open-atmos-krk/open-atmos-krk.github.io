---
title: MPDATA&thinsp;meets&thinsp;Black&dash;Scholes

description: |
  We apply the MPDATA scheme to option pricing by reformulating the Black-Scholes-Merton equation 
    as an advection problem. 
  This novel application enables all PDE terms to be handled consistently with a single non-oscillatory,
    high-order and positive-definite numerical operator.

people:
  - pawel_magnuszewski
  - sylwester_arabas

layout: project
image: "/img/money.jpg"
---

<p>
We explore a simple yet robust numerical method for integrating PDEs applied to pricing of options (financial instruments).
We use the the non-oscillatory forward-in-time second-order MPDATA finite-difference scheme, which originates from 
  geophysical fluid dynamics. 
The valuation methodology involves casting the <a href="https://en.wikipedia.org/wiki/Black%E2%80%93Scholes_model">Black-Scholes-Merton equation</a> 
  as a transport problem by first transforming it into a homogeneous <a href="https://en.wikipedia.org/wiki/Convection%E2%80%93diffusion_equation">advection-diffusion PDE</a> 
  via variable substitution, and then expressing the diffusion term as an advective flux using the pseudo-velocity technique. 
As a result, all terms of the <a href="https://en.wikipedia.org/wiki/Black%E2%80%93Scholes_model">Black-Sholes-Merton equation</a>
  are consistently represented using a single high-order numerical scheme for the advection operator.
So far, we have demonstrated the methodology for <a href="https://en.wikipedia.org/wiki/European_option">European-</a>,
  <a href="https://en.wikipedia.org/wiki/American_option">American-</a> and <a href="https://en.wikipedia.org/wiki/Asian_option">Asian-style</a> 
  contracts in the following papers:
<ul>
  <li><a href="https://doi.org/10.1016/j.cam.2019.05.023">Arabas &amp; Farhat 2020</a>: "<em>Derivative pricing as a transport problem: MPDATA solutions to Black–Scholes-type equations</em>"</li>
  <li><a href="https://arxiv.org/abs/2505.24435">Magnuszewski &amp; Arabas 2025</a>: "<em>Path-dependent option pricing with two-dimensional PDE using MPDATA</em>"</li>
</ul>
All figures and tables from the above papers are reproducible with Jupyter notebooks maintained as examples in the 
  <a href="https://open-atmos-krk.github.io/projects/pympdata.html">PyMPDATA package</a>.
</p>


<h3>Student project opportunities</h3>
<ul>
  <li>Pricing Amerasian (Hawaiian) options and other exotics with MPDATA</li>
  <li>Geomeric-average Asian option valuation using MPDATA (requires a source term) for comparison with analytic solution</li>
  <li>Achieving third-order temporal/spatial accuracy for the Black-Scholes problem using MPDATA</li>
</ul>
