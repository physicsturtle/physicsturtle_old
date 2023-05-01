---
layout: lesson
title: Effective Action of the Kondo Model (my notes)
dept: physics
course: many-body-II
unit: unit13
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 13
---
The partition function is given by 

$$$$\begin{align}
Z = \int e^{-S} \D\bar{c}\D c
\end{align}$$$$

where the action is given by

$$$$\begin{align}
S = \int_0^\beta\left(\sum_{\k\sigma} \bar{c}_{\k\tau\sigma}\partial_\tau c_{\k\tau\sigma} + H\right)\d\tau
\end{align}$$$$

and the Hamiltonian in terms of Grassmann variables (including the Fedotov-Popov chemical potential) is 

$$\begin{align}
H[\bar{c},c,\bar{f},f] =& \sum_{\k\sigma}\epsilon_{\k} \bar{c}_{\k\tau\sigma}c_{\k\tau\sigma} + J\bar{c}_{0\tau\alpha}c_{0\tau\beta}\boldsymbol{\sigma}_{\alpha\beta}\cdot\textbf{S}(\tau) \\
=& \sum_{\k\sigma}\epsilon_{\k} \bar{c}_{\k\tau\sigma}c_{\k\tau\sigma} + \frac{J}{N_s}\sum_{\k,\k'}\bar{c}_{\k\tau\alpha}c_{\k'\tau\beta}\boldsymbol{\sigma}_{\alpha\beta}\cdot\textbf{S}(\tau)
\end{align}$$

To perform the RG procedure, we will proceed in 3 steps:

<ul>
<li> Split the conduction electrons into slow and fast fields
</li> 
 <li> integrate out the fast fields, leaving the Gaussian part invariant
</li> 
 <li> Find out how the coupling constants are changed upon this removal of fast modes
\end{itemize}

We take the path integral and write it as an integral over slow and fast fields:

$$$$\begin{align}
Z = \int e^{-S_{0<}} \left(\int e^{-S_{0>}} e^{-S_\text{int}} \D\bar{c}_> \D c_>\right)\D\bar{c}_< \D c_<
\end{align}$$$$

The inner integral can be written as a correlation function if we multiply and divide by \\(Z_{0>}\\). Thus, we get 

$$$$\begin{align}
Z =Z_{0>} \int e^{-S_{0<}} \left< e^{-S_\text{int}}\right>_{0>}\D\bar{c}_< \D c_<
\end{align}$$$$

The expectation \\(\left<e^{-S_\text{int}}\right>_{0>}\\) needs to be written as a cumulant expansion:

$$$$\begin{align}
\left<e^{-S_\text{int}}\right>_{0>} = e^{-S_\text{eff}}
\end{align}$$$$

whereby 

$$$$\begin{align}
S_\text{eff} = S_{0<} + \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n!} \left<S^n_\text{int}\right>_{0>,c}
\end{align}$$$$

and we now need to evaluate \\(S_\text{eff}\\). 


