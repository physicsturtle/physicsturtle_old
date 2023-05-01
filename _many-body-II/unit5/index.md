---
layout: lesson
title: Fermionic Path Integrals
dept: physics
course: many-body-II
unit: unit5
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 5
---
If \\(\tau_2 > \tau_1\\), then \\(\bar{\psi}(\tau_1)\\) factor appears to the left of \\(\psi(\tau_2)\\).

$$$$\begin{align}\mathcal{G}(\tau_1 - \tau_2) = \frac{1}{Z}\tr(e^{-(\beta - \tau_2)H}\hat{\psi}^\dagger e^{-(\tau_2 - \tau_1)H}\hat{\psi}e^{-\tau_2 H}) = \int e^{-S} \bar{\psi}(\tau_2)\psi(\tau_1) \D\bar{\psi}\D\psi\end{align}$$$$

Grassmann variables anticommute, so

$$$$\begin{align}\mathcal{G}(\tau_1 - \tau_2) = -\frac{1}{Z}\int e^{-S} \psi(\tau_1)\bar{\psi}(\tau_2) \D\bar{\psi}\D\psi\end{align}$$$$

$$$$\begin{align}\mathcal{G}(\tau_1 - \tau_2) = -\left<\psi(\tau_1)\bar{\psi}(\tau_2)\right>\end{align}$$$$

where \\(\left<\right>\\) denotes ``average" weighted by \\(e^S\\) and integrated over \\(\D\bar{\psi}\D\psi\\). 

Feynman path integral is automatically time ordered. This is one of the reasons why - sign is appropriate in the definition of the \\(t\\) ordering for fermions, and why Matsubara green function is useful.

This carries over to multipoint green functions, 

$$$$\begin{align}\left<\psi(\tau_1)\cdots\psi(\tau_n)\bar{\psi}(\tau_{n+1})\cdots\bar{\psi}(\tau_{2n})\right> = e^{\beta\Omega}\tr e^{-\beta H}T[\hat{\psi}(\tau_1)\cdots\hat{\psi}(\tau_n)\hat{\psi}^\dagger(\tau_{n+1})\cdots\hat{\psi}^\dagger(\tau_{2n})]\end{align}$$$$

Let's check free electron green function

$$$$\begin{align}
S = \int_0^\beta (\bar{\psi}\frac{d\psi}{d\tau} + \epsilon\bar{\psi}\psi)\d\tau = \frac{1}{\beta}\sum_n\bar{\psi}(\omega_n)\psi(\omega_n)(-i\omega_n + \epsilon)
\end{align}$$$$

by above definition of Fourier transform. The Grassmann integrals factorize 

$$$$\begin{align}-\left<\psi(\omega_n)\bar{\psi}(\omega_n)\right> = \frac{\int d\bar{\psi}d\psi e^{\bar{\psi}\psi(i\omega_n - \epsilon)}\bar{\psi}\psi}{\int d\bar{\psi}d\psi e^{\bar{\psi}\psi(i\omega_n - \epsilon)}} = \frac{1}{i\omega_n - \epsilon}\end{align}$$$$

Note that

$$\begin{align}
\mathcal{G}(i\omega_n) =& -\int_0^\beta d\tau e^{i\omega_n\tau}\left<\psi(\tau)\bar{\psi}(0)\right> \\
=& -\left<\psi(\omega_n)\bar{\psi}(\tau = 0)\right> \\
=& -\frac{1}{\beta}\left<\psi(\omega_n)\bar{\psi}(\omega_n)\right> \\
=& \frac{1}{i\omega_n -\epsilon}
\end{align}$$

Correct answer! Simplify the inverse of quadratic of coefficient of \\(\bar{\psi}(\omega_n)\psi(\omega_n)\\) in \\(S\\) (divided by \\(\beta\\))

It extends \\(I\\) to multi-fermion models and multipoint Green functions.

We develop perturbation theory in \\(H_\text{int}\\) by Taylor expanding 

$$$$\begin{align}e^{-\int_0^\beta d\tau H_\text{int}[\bar{\psi}(\tau),\psi(\tau)]}\end{align}$$$$

factor in \\(e^S\\)

$$$$\begin{align}=\sum_{n=0}^\infty\frac{(-1)^n}{n!}\left(\int_0^\beta Hd\tau\right)^n\end{align}$$$$

Must evaluate Feynman integrals like

$$$$\begin{align}
\frac{1}{\beta^2}(\delta_{\omega_1,\omega_2}\left<\bar{\psi}(\omega_1)\psi(\omega_2)\right>\delta_{\omega_3,\omega_4}\left<\bar{\psi}(\omega_3)\psi(\omega_4)\right> - \delta_{\omega_1,\omega_4}\left<\bar{\psi}(\omega_1)\psi(\omega_4)\right>\delta_{\omega_2,\omega_3}\left<\bar{\psi}(\omega_3)\psi(\omega_2)\right>)
\end{align}$$$$

(at \\(\beta\to\infty\\))

Note that minus sign due to Fermi statistics - otherwise has similar structure to bosonic case. We can write Jellium model, for example, as a path integral 

$$$$\begin{align}\int_I = \int_0 + \int_{\text{int}}\end{align}$$$$

$$$$\begin{align}
S_0 = \frac{1}{\beta}\sum_{\omega_n,\k} \bar{\psi}(\k,\omega_n) \psi(\k,\omega_n) (i\omega_n - \epsilon_{\k})
\end{align}$$$$

$$$$\begin{align}S_\text{int} = -\frac{1}{2V\beta^3}\sum_{\k,\omega_1,\sigma_1,\k_2,\omega_2,\sigma_2,\q,\omega} V_{\q} \bar{\psi}_{\k_1+\q_1,\omega_1+\omega,\sigma_1}\bar{\psi}_{\k_2-\q,\omega_2 - \omega_1,\sigma_2}\psi_{\k_2,\omega_2,\sigma_2}\psi_{\k_1,\omega_1,\sigma}\end{align}$$$$

insert Feynman diagram here!

Momentum, imaginary frequency, and spin, are conserved at vertex which has a factor of \\(V_{\q}\\) associated with it. At \\(T\to 0\\), \\(\Delta\omega_n = 2\pi T\to 0\\) so 

$$$$\begin{align}
\frac{1}{\beta}\sum_{\omega_n}\to \int\frac{\d\omega}{2\pi}
\end{align}$$$$

and factors of \\(1/\beta\\) in \\(S_I\\) cancel. We will use the path integral to develop RG.

We will integrate out high energy states, far from Fermi surface - large \\(\epsilon_{\k}\\) - to get a low energy effective Hamiltonian (and action) for states close to Fermi surface. This gets complicated for \\(d=2\\) or 3 due to presence of Fermi surface. We we will first discuss simpler examples, that are still experimentally relevant.

