---
layout: lesson
title: Mean-Field Theory
dept: physics
course: many-body-II
unit: unit32
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 32
---
We consider the partition function for the effective action in terms of the mean-field uniform solution \\(\Delta = \const\\). The effective action in terms of the gap \\(\Delta\\) is given by 

$$S_\text{eff}[\Delta^{*},\Delta] = \frac{\beta N_s}{U}|\Delta|^2 - \log\left<\exp\left(-\int_0^\beta\sum_i \left(\Delta \bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow} + \Delta^{*} c_{i\tau\downarrow} c_{i\tau\uparrow}\right)\d\tau\right)\right>_0$$

The effective action is related to the Landau free energy by

$$\mathcal{F} = \frac{1}{\beta} S_\text{eff}.$$

We seek to minimize the Landau free energy. Thankfully, for the uniform \\(\Delta\\) case, it is possible to exactly evaluate \\(S_\text{eff}\\). For this case, we find that 

$$\begin{align}
\Delta S_\text{eff} =& - \log\left<\exp\left(-\int_0^\beta\sum_i \left(\Delta \bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow} + \Delta^{*} c_{i\tau\downarrow} c_{i\tau\uparrow}\right)\d\tau\right)\right>_0 \\
=& - \log\left<\exp\left(-\sum_k \left(\Delta \bar{c}_{k\uparrow}\bar{c}_{-k,\downarrow} + \Delta^{*} c_{-k,\downarrow} c_{k\uparrow}\right)\right)\right>_0 \\
=& - \log\left(\int \right)
\end{align}$$

What we find is that the free energy is given by 

$$F = \frac{N_s |\Delta|^2}{U} - \frac{2V}{\beta}\int \log\left[\cosh\left(\frac{\beta E_{\k}}{2}\right) \right] \frac{\d^3\k}{(2\pi)^3} $$

As \\(T\to 0\\), \\(\beta\to\infty\\) and the free energy goes to 

$$\begin{align}
F =& \frac{N_s\beta |\Delta|^2}{U} - \frac{2\V}{\beta}\int \log\left[\frac{1}{2}\exp\left(\frac{\beta E_{\k}}{2}\right) \right]\frac{\d^3\k}{(2\pi)^3} \\
=& \frac{N_s\beta |\Delta|^2}{U} - \V \int \sqrt{\xi_{\k}^2 + |\Delta|^2}\frac{\d^3\k}{(2\pi)^3} + \const
\end{align}$$

We minimize this free energy with respect to \\(\Delta\\). This free energy btw is given by

$$F = U - TS - J\Delta$$

where \\(J\\) is the generalized force coupled to the order parameter \\(\Delta\\). 

\subsection{Heat Capacity}
We now calculate the heat capacity of the superconductor in the superconducting state. 


