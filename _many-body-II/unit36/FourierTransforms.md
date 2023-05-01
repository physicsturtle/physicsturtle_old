---
layout: lesson
title: Fourier Transforms
dept: physics
course: many-body-II
unit: unit36
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 36
---
If we have a Bravais lattice, and we have imposed periodic boundary conditions, we will Fourier transform conduction electron operators/Grassmann numbers like:

$$c_{i\tau} = \frac{1}{\sqrt{\beta N_s}}\sum_{\k,i\omega} e^{-i\omega t} e^{i\k\cdot\textbf{R}_i}c_{\k\omega}$$

where \\(\k\\) is summed over the first Brillouin zone. 

If we have a continuum operator (this is at zero temperature, otherwise the Matsubara frequencies aren't continuous)

$$\psi(\x,\tau) = \int_{-\infty}^\infty\int \psi(\k,\omega) \frac{\d^d\k}{(2\pi)^d} \frac{\d\omega}{2\pi}$$


