---
layout: lesson
title: Fermion-Boson Mapping
dept: physics
course: many-body-II
unit: unit19
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 19
---

Now, we need to compute 

$$\partial_x \psi_{\p}m(x) = \partial_x \left(\frac{1}{\sqrt{2\pi\alpha}} e^{\pm i\sqrt{4\pi}\phi_{\p}m(x)}\right)$$

One can do this by applying the definition of the derivative and Taylor expanding, but we can also apply the formula for the derivative of a matrix exponential:

$$\begin{align}
\partial_x \psihat_{\p}m(x) =& \frac{1}{\sqrt{2\pi\alpha}} \int_0^1 e^{\pm(1-u) i\sqrt{4\pi}\phihat_{\p}m(x)} \partial_x\left(\pm i\sqrt{4\pi}\phihat_{\p}m(x)\right) e^{\pm ui\sqrt{4\pi}\phi_{\p}m(x)} \d u \\
=& \frac{\pm i\sqrt{4\pi} }{\sqrt{2\pi\alpha}} e^{\pm i\sqrt{4\pi}\phi_{\p}m(x)}  \int_0^1 e^{\mp u i\sqrt{4\pi}\phi_{\p}m(x)} \left(\partial_x\phi_{\p}m(x)\right) e^{\pm ui\sqrt{4\pi}\phi_{\p}m(x)} \d u \\
\end{align}$$

Since \\(\partial_x \phi_{\p}m = \frac{1}{2}\left(\mp \pi(x) + \partial_x\phi\right)\\), 

