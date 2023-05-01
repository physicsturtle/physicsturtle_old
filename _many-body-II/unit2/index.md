---
layout: lesson
title: Bosonic Coherent State Path Integral
dept: physics
course: many-body-II
unit: unit2
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 2
---

We recall the ordinary path integral from single-particle quantum mechanics. We recall that the main motivation was to write the time evolution of a wave function as the integral of a kernel \\(K\\) times the wave function \\(\psi\\). We take the product of the wave function at time \\(t'\\), and evolve it to time \\(t\\):

$$$$\begin{align}
\psi(x,t) = \int K(x,t;x',t') \psi(x',t') \d x'.
\end{align}$$$$

Then, the kernel \\(K\\) can be written as a path integral using the Lagrangian of the theory. Instead of writing the kernel (also known as propagator) as a path intergral, we are typically interested in a different quantity when studying condensed matter physics: the partition function \\(Z = \tr e^{-\beta H}\\). 

Moving on to the technical details, we recall that, in order to construct the path integral for the propagator, we had to split the time evolution operator \\(\hat{U}(t,t') = e^{-i\Hhat(t-t')}\\) into infinitesimal time-intervals and then insert the resolution of identity between each time-slice. A similar procedure is necessary for constructing the coherent state path integral for bosons, so one of our tasks, in addition to defining these coherent states, is to figure out how to write the identity in terms of them. Furthermore, because we are constructing the partition function, we also need to learn how to write the trace of an operator on the bosonic Fock space. 

