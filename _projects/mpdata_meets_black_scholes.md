---
title: MPDATA&thinsp;meets&thinsp;Black-Scholes
status: inactive

description: |
  We explore a robust numerical method for option pricing that recasts the Black-Merton-Scholes equation 
    as an advection problem and applies the high-order, non-oscillatory MPDATA scheme (originally from geophysical 
    fluid dynamics) to consistently handle all PDE terms with a single numerical operator, demonstrating 
    effectiveness across European-, American-, and Asian-type contracts.

people:
  - pawel_magnuszewsk
  - sylwester_arabas

layout: project
image: "/img/money.jpg"
---

We explore a simple yet robust numerical method for integrating PDEs applied to pricing of options (financial instruments).
We use the the non-oscillatory forward-in-time second-order MPDATA finite-difference scheme, which originates from 
  geophysical fluid dynamics. 
The valuation methodology involves casting the Black-Merton-Scholes equation as a transport problem by first transforming 
  it into a homogeneous advection-diffusion PDE via variable substitution, and then expressing the diffusion term as an advective 
  flux using the pseudo-velocity technique. 
As a result, all terms of the Black-Merton-Sholes equation are consistently represented using a single high-order numerical scheme for the advection operator.
So far, we have demonstrated the methodology for [European-, American-](https://doi.org/10.1016/j.cam.2019.05.023) 
  and [Asian-style](https://arxiv.org/abs/2505.24435) contracts.

