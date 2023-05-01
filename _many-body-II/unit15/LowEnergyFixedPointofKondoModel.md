---
layout: lesson
title: Low Energy Fixed Point of Kondo Model
dept: physics
course: many-body-II
unit: unit15
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 15
---
For AF Kondo, coupling \\(\lambda(\D)\\) becomes \\(O(?)\\) at \\(\D\sim T_K\\). 

Perturbation theory fails at lower energies and perturbative RG isn't enough

Naively we might guess \\(\lambda\to\infty\\) at \\(\epsilon\to 0\\)

What would this imply for resistivity? \\(s?(maybe \rho)\to\infty\\)! Seems unlikely (impossible)

For dilute impurities

To get some intuition it is very convenient to study a tight-binding model, e.g. in 1D 

$$$$\begin{align}H = -t\sum_{i=-\infty}^\infty \sum_\alpha (\chat^\dagger_{i\alpha}\chat_{i\alpha} + h.c.) + J\chat_0^\dagger\frac{\boldsymbol{\sigma}}{2}\chat_0\cdot\textbf{S}\end{align}$$$$

Impurity couples to site 0 only.

We are really interested in case where bare coupling \\(J\ll t\\), but since \\(\lambda\\) may flow to \\(\infty\\) at low \\(E\\), it is interesting to consider model with large bare coupling \\(J\gg t\\)

Remarkably, we can easily solve if exactly in that limit! 

For simplicity let's consider model at \\(\frac{1}{2}\\) filling.

\\(J\gg t\\) is equivalent to \\(t\to 0\\)

$$$$\begin{align}
H = J\chat_0^\dagger \frac{\boldsymbol{\sigma}}{2}\chat_o \cdot\textbf{S} = J\textbf{s}_0\cdot\hat{\textbf{S}}
\end{align}$$$$

$$$$\begin{align}[\hat{n}_0,H] = 0\end{align}$$$$

For \\(n_0 = 0,2\\), \\(\textbf{s}_0 = 0\\) - spin zero state

\\(E_0 = E_2 = 0\\) - doublets.

With \\(n_0 = 1\\), \\(s_0 = \frac{1}{2}\\). \\(H\\) is Hamiltonian for 2 coupled \\(s = \frac{1}{2}s\\)

$$$$\begin{align}H = J\left[\frac{1}{2}(\textbf{S}+\textbf{s}_0)^2 - \frac{3}{4}\right] = J\left[\frac{1}{2}s_\tau s_{\tau+1} - \frac{3}{4}\right] = \begin{cases}
	-\frac{3J}{4} & s_\tau = 0\\
	\frac{J}{4} & s_\tau = 1
\end{cases}\end{align}$$$$

Ground state has 1 electron at origin, forming spin singlet with impurity

$$$$\begin{align}\ket{\psi_0} = \frac{1}{\sqrt{2}}[\chat^\dagger_{0\uparrow}\ket{0}\ket{\downarrow} - \chat^\dagger_{0\downarrow}\ket{1}\ket{\uparrow}]\end{align}$$$$

Other states have energies higher by \\(O(J)\\).

What do other electrons do?

At \\(t = 0\\), anything they like except enter site 0.

For small \\(t\ll J\\), can do degenerate perturbation theory.

Other electrons form a free electron ground state (filled Fermi sea) with wave functions vanishing at \\(j = 0\\). Even parity wave functions modified from \\(\phi_i^{(e)}\propto\cos k_i\\), \\(J = 0\\) to \\(s\\) in \\(k|i|\\), \\(J\to\infty\\)

Odd parts \\(\phi^{(0)}_i = s\\) in \\(k\\) unchanged.

Phase shifts:

$$$$\begin{align}\phi^{(e)}_i = \cos(k_i +\delta^{(e)}(k))\end{align}$$$$

$$$$\begin{align}\delta^{(e)} = \pi/2,\qquad \delta^{(0)} = 0\end{align}$$$$

How might we apply this int??tion to interesting case \\(J\ll t\\). 

i.e. bare to dimeionless coupling small but renormalized coupling at energy scale \\(\lesssim T_K\\) large - perhaps lower energy behaivour is similar ot above description.

We might imagine an electron forms a spin singlet with impurity (Kondo screening) but there is no reason to think that electron sits at \\(i=0\\)

Only low energy electrons \\(|\epsilon| \lesssim T_K\\) are strongly perturbed by Kondo interaction 

These have wave vectors \\(|k - k_F|\lesssim T_K/v_F\\)

A screening wave function constructed from such a small band of wave vectors would be spread out over a distance of order \\(\xi_K = v_F/T_K\\) and would oscillate at \\(k_F\\). \\(\xi_K\sim a e^{1/\tau}\gg a\\) is a very large scale. (could be ?? in expt)

We might speculate that studying a Kondo impurity with a very long wave length probe \\(\lambda \gg \xi_K\\) would see the \\(\pi/2\\) phase shift. 

Free electrons with \\(\pi/2\\) phase shift in even parity channel could be universal description of low energy long distance physics.

But more complicated physics must occur at intermediate energy and/or length scales 

i.e. a conjecture for low energy fixed point Hamiltonian is free electrons with impurity spin removed and \\(\pi/2\\) phase shift in even parity channel (corresponding to a vanishing boundary condition at origin)

Let's assume this is correct and explore its consequences

We can then check if they agree with experiments and other theoretical calculations.

What does this assumption predict for resistivity at \\(T = 0\\)?

Should be the same as that of a random array of potential scatterers with very short range repulsion - corresponding to a \\(\pi/2\\) phase shift in \\(s\\)-wave channel (only)

Note: extending strong coupling solution to 3D model we only get \\(\pi/2\\) phase shift in s-wave 

Short range interaction doesn't affect other harmonics since wave functions vanish at origin

Such a model gives largest possible resistance from potential scatterers of given (low) density \\(\rho_\text{imp}\\) ``unitary limit" 
\\(T\\) matrix for potential scattering is

$$$$\begin{align}T = \frac{i}{2\pi\nu}(e^{2i\delta} - 1)\end{align}$$$$

for \\(s\\) wave phase shift \\(\delta\\) (see Mahan, chap 4)

\\(T = -\frac{i}{2\pi \nu}\\) for \\(\delta = \pi/2\\)

Resistivity can be expressed in terms of \\(\Im(T)\\) as before.

In general, 

$$$$\begin{align}\frac{1}{2\tau} = -\Im(T) = \frac{1}{\pi\nu}\sin^2\delta\end{align}$$$$\

Largest scattering rate for \\(\delta = \pi/2\\).

``unitary limit" \\(T\propto -i(1-S)\\). \\(S\\) matrix \\(e^{2i\delta}\\) must be unitary.

From \\(1/T\\) we get resistivity from Kubo formula as before.

$$$$\begin{align}\rho = \frac{3}{2\pi e^2 v_F^2 \nu}\rho_\text{imp} = \rho_\text{un}\rho_\text{imp}\end{align}$$$$

Finte value at \\(T\to 0\\). 

This agrees with other theoretical approaches and experiments. 


