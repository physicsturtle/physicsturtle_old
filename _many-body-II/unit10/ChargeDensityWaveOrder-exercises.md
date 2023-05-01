---
layout: lesson
title: Charge Density Wave Order - Exercises
dept: physics
course: many-body-II
unit: unit10
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 10
---
<ol>
\question Reverse the Hubbard-Stratonovich transformation of the interaction 
$$\begin{align}
S_\text{int} =& \frac{1}{2U\beta N}\sum_k \phi_k \phi_{-k} - \frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k(\bar{c}_{k+p,\sigma}c_{p\sigma} - \rho + \rho).
\end{align}$$
by integrating out the \\(\phi\\) field, and determine how the original action purely in terms of fermions needs to be modified such that \\(\Delta S^{(1)}_\text{eff} = 0\\). 

\begin{solution}
We start by inverting the Fourier transforms from earlier by doing:

$$\phi_k = \int_0^\beta\sum_i e^{ik_0\tau - i\textbf{R}_i\cdot\k}\phi_{i\tau}\d\tau $$
and also
$$c_{k\sigma} = \frac{1}{\sqrt{N\beta}}\int_0^\beta\sum_i e^{ik_0\tau - i\textbf{R}_i\cdot\k} c_{i\tau\sigma} \d\tau,\quad \bar{c}_{k\sigma} = \frac{1}{\sqrt{N\beta}}\int_0^\beta\sum_i e^{-ik_0\tau + i\textbf{R}_i\cdot\k} \bar{c}_{i\tau\sigma}\d\tau .$$

We plug these representations in to \\(S_\text{int}\\)

$$\begin{align}
S_\text{int} =& \frac{1}{2U\beta N}\sum \int_0^\beta\int_0^\beta\sum_{i,i'} e^{ik_0\tau - i\textbf{R}_i\cdot\k} e^{-ik_0 + i\textbf{R}_i\cdot\k} \phi_{i\tau}\phi_{i'\tau'}\d\tau\d\tau' - \frac{i}{\beta N}\sum_{k,p,\sigma}\int_0^\beta 
\end{align}$$


\end{solution}

\end{questions}

