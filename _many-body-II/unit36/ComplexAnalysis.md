---
layout: lesson
title: Complex Analysis
dept: physics
course: many-body-II
unit: unit36
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 36
---

\subsubsection{Integral over the complex plane}
The notation 

$$\int f(z,z^{*}) \d z^{*} \d z$$

frequently arises in many-body physics. To my knowledge, there is no rigorous definition of this notation in terms of ``summing over \\(\Delta z^{*}\\) and \\(\Delta z\\) (like a Riemann sum). Rather, we define it in terms of the well-known 

$$\int f(z,z^{*}) \d z^{*} \d z := \int f(z,z^{*}) \d\Re(z)\d\Im(z).$$

Note that some authors will include factors of \\(2\pi\\) or \\(i\\) in definitions such as these. However, these do not really matter. 

\subsubsection{Sokhotski-Plemelj Theorem}

The theorem says 

$$\lim_{\eta\to 0^+} \frac{1}{x\pm i \eta} = \mathcal{P}\left(\frac{1}{x}\right) \mp i\pi \delta(x)$$

The proof of this is 


