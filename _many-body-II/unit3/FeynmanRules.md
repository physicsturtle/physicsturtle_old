---
layout: lesson
title: Feynman Rules
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
We will use the fact that we can write the Green function as a path integral to derive the Feynman rules. The Green function at zero temperature is simply the correlation function in the interacting ground state.

$$$$\begin{align}
G = -i\bra{GS}T[\chat_{\p}(t) \chat^\dagger_{\p}(0)]\ket{GS}
\end{align}$$$$

With 

$$$$\begin{align}
S = \int_0^\beta \bar{\psi}(\tau)\left(\frac{\partial}{\partial\tau} + \omega_0 - \mu\right)\psi(\tau) d\tau 
\end{align}$$$$

The correlation function for the fermionic oscillator is

$$\begin{align}
\left<\psi(\tau_1)\bar{\psi}(\tau_2)\right> =& \frac{\int \psi(\tau_1)\bar{\psi}(\tau_2) e^{-S} \D\psi }{\int e^{-S} \D\psi}\\
=& \frac{\tr(\psi(\tau_1)\bar{\psi}(\tau_2)e^{-S})}{\tr(e^{-S})}
\end{align}$$

To evaluate the correlation function, we rewrite both the effective action and the fields in terms of Matsubara frequency fields: 

$$\psi_{\tau} = \frac{1}{\sqrt{\beta}} \sum_\omega e^{-i\omega\tau}\psi_{\omega}, \quad \bar{\psi}_{\tau} = \frac{1}{\sqrt{\beta}}\sum_\omega e^{i\omega\tau} \bar{\psi}_{\omega}$$

For \\(\tau_1 > \tau_2\\), 

<div class="result">
<b>Result:</b>
The partition function for a fermionic theory is given by

$$Z = \int e^{-S[\bar{\psi},\psi]}\D\bar{\psi}\D\psi$$

whereby

$$S = \int_0^\beta \left[\bar{\psi}(\tau)\frac{\partial}{\partial\tau}\psi(\tau) + H(\bar{\psi},\psi) - \mu N(\bar{\psi},\psi)\right] \d\tau$$

and \\(\bar{\psi}(0) = -\bar{\psi}(\beta)\\) and \\(\psi(0) = -\psi(\beta)\\). 

</div>


