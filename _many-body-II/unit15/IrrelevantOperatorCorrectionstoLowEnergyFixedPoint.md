---
layout: lesson
title: Irrelevant Operator Corrections to Low Energy Fixed Point
dept: physics
course: many-body-II
unit: unit15
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 15
---
We may think of \\(\lambda\to\infty\\) (in a sense) as \\(\D\to 0\\) fixed point in Kondo problem.

Low energy behaviour of the \\(\lambda = \infty\\) model is just free fermions with

<ul>
	<li> \\(\pi/2\\) phase shift in s-wave channel
	</li> 
 <li> no impurity spin
\end{itemize}

This gives most physical behaviour in zero energy (infinite length) limit

We can go further and calculate leading corrections to this behaviour when \\(T\ll T_K\\)

This is determined (in any model) by the leading irrelevant operators at low energy fixed point. 

We can approach this using the ``anything not forbidden by symmetry will occur" approach.

enumerate possible interaction in \\(S_\text{eff}\\) as \\(D\to\infty\\).

They should

<ul>
	<li> be local - occurring only at \\(x = 0\\) - can expand in derivatives there
	</li> 
 <li> not involve impurity spin-screened - eliminated from low energy theory - A bit like strongly coupled spins in problem set 3.
	</li> 
 <li> repeat \\(\SU(2)\\) spin-rotation symmetries
	</li> 
 <li> respect particle-hole symmetry of microscopic model had it (assume for simplicity) 
\end{itemize}

thus, 2 allowed operators scaling as \\(1/s\\)

$$$$\begin{align}\lambda_1\sum_\alpha\left[\psi^\dagger_\alpha \frac{d}{dx}\psi_\alpha - \frac{d}{dx}\psi^\dagger_\alpha \psi_\alpha\right] \qquad (x=0) + \lambda_2\sum_{\alpha,\beta}[\psi_\alpha^\dagger\psi_\alpha - \left<\psi^\dagger_\alpha\psi_\alpha\right>][\psi^\dagger_\beta\psi_\beta - \left<\psi^\dagger_\beta\psi_\beta\right>]\end{align}$$$$

$$$$\begin{align}\psi(\tau,s)\to s^{-1/2}\psi(\tau,s)\end{align}$$$$

after Fourier transform. \\(x\to sx\\), \\(\tau \to s\tau\\)

$$$$\begin{align}\int(\bar{\psi}\frac{d}{dx}\psi) d\tau\to s\cdot s^{-1/2} s^{-1/2}\frac{1}{2}\propto \frac{1}{2}\end{align}$$$$


similarly for \\(\int (\bar{\psi}\psi)^2 d\tau\\)

Normalize \\(\psi(x)\\) so \\(\{\psi(x),\psi^\dagger(y)\} = 2\pi\delta(x-y)\\).

so \\(\psi\\) has units of inverse root length, and \\(\lambda_0\\) has units of energy times length squared.

We can estimate \\(\lambda_i\\) from dimensional analysis. What is the largest quantity we can construct from available parameters with right dimensions? 

$$$$\begin{align}\lambda_i \sim \frac{v_F^2}{T_K}\end{align}$$$$

actually, an argument can be given to determine ratio \\(\lambda_1/\lambda_2\\) exactly.

It is based on ``spin-charge separation" in Dirac (direct?) Fermion model. (Affleck - Phys B 336, 517, 1990)

So there is only one unknown parameter of \\(O(1)\\), and \\(\lambda_1\\) in units of \\(v_F^2/T_K\\). 

We can predict many low energy properties in terms of it (specific heat, magnetic susceptibility, resistance), and it drops out of ratios made from these quantities. 

Consider contribution of \\(\lambda_1\\) to resistivity

Gives \\(k\\)-dependence to phase shifts

$$$$\begin{align}\delta = \frac{\pi}{2} + \alpha(k-k_F)\frac{v_F}{T_K},\qquad \alpha\sim O(1)\end{align}$$$$

so that 

$$$$\begin{align}\frac{1}{T}\propto sm^2\delta = \cos^2\alpha(k-k_F)\frac{v_F}{T_K} = \frac{1}{2}(1+\cos(2\alpha(k-k_F)v_F/T_K)) = 1-\alpha^2(k-k_F)^2\frac{v_F^2}{T_K^2}\end{align}$$$$

$$$$\begin{align}\delta\rho \sim\left(\frac{v_F}{T_K}\right)^2\int(k-k_F)^2\frac{dn_F}{d\epsilon}d^3\k\end{align}$$$$

\\(v_F(k-k_F)\sim \epsilon\\)?

$$$$\begin{align}\int \epsilon^2 \frac{dn}{d\epsilon}d\epsilon\sim T^2\end{align}$$$$

so

$$$$\begin{align}\delta\rho \propto \left(\frac{T^2}{T_K}\right)^2\end{align}$$$$ 

also a similar contribution from \\(\lambda_2\\)

(insert graph here)

\\(C\propto \lambda_1^2\\) (in units of \\(v_F^2/T_K\\))

can also calculate magnetic susceptibility vanishes at \\(\lambda_i = 0\\) since there is no impurity in fixed point \\(H\\).

$$$$\begin{align}H_\text{eff} = iv_F\int_{-\infty}^\infty \psi^\dagger \frac{d}{dx}\psi dx\end{align}$$$$

\\(x_\text{imp} = n_\text{imp}x_\text{const}/T_K\\) (first order in \\(\lambda_1\\) and \\(\lambda_2\\))

Unknown constant in \\(\lambda_1\\) drops out in Wilson ratio: \\(\delta x/x/(\delta_c/c) = 2\\)

Many other quantities can be calculated in a similar way - RG improved perturbation theory in \\(\lambda\\) (Kondo coupling) at high energies 

Lowest order perturbation theory in \\(\lambda_1\\) (leading irrelevant operator) at low energies

\\(M(H)\\), \\(\rho(H)\\), density oscillations, knight shift, 

obtain good agreement with other theoretical techniques at high and low energies - Bethe constants and numerical renormalization group show graphic

So brilliant guess about low energy fixed point was correct

only cross over regime, \\(T\sim T_K\\) is difficult and requires more numerically intensive methods.

agreement with experiments is good at qualitative level but more realistic model is usually needed (larger impurity spin magnitude \\(s > 1/2\\), charge fluctuation of magnetic impurity atom (andersom model), finite impurity concentrations, realistic band strucutre non \\(\delta\\) function Kondo interaction, other, nonmagnetic impurities...)

Nonetheless, Kondo model is a nice illustration of the Rg at work. 

Both higher energy and low energy behaviour are accessible with minimal numerical work.


