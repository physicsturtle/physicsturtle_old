---
layout: lesson
title: Real Space Path Integral
dept: physics
course: many-body-II
unit: unit1
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 1
---
First, let's start with the standard real space path integral. The approach is based on correspondence between classical and quantum theory. Start with the classical action. Consider a single particle moving in a potential \\(V(\x)\\). The Lagrangian for this system is found in the typical way: the minimization of the action reproduces Newton's equations of motion.

$$$$\begin{align}L = \frac{m}{2}\x^2 - V(\x).\end{align}$$$$

The Lagrangian is a function of the two variables, the position and the velocity: \\(\L = \L(\x,\dot\x)\\). The canonical momentum is given by a derivative of the Lagrangian with respect to the velocity

\\(p_i = \frac{\partial\L}{\partial \dot{x}^i}\\). From this, one can obtain the Hamiltonian through the Legendre transformation

$$$$\begin{align}
H = \sum_i p_i \dot{x}^i - \L.
\end{align}$$$$

We recall that the Hamiltonian is so-defined because it means that the Hamiltonian is not a function of the velocity, but rather the position and canonical momentum. These formulae generalize to essentially arbitrary Lagrangians with more coordinates; we can work in any number of dimensions with any number of particles. 

In order to quantize the theory, we need to promote the coordinates \\(\hat{x}_i\\) and \\(\hat{p}_i\\) to operators, as well as impose the canonical commutation relation \\([\hat{x}_j, \hat{p}_k] = i\hbar\delta_{jk}\\). All other commutators are zero. 

The Lagrangian approach generalizes to quantum field theory in both condensed matter physics and high energy physics. In condensed matter physics we will deal largely with interacting fermions. For interacting fermions, we write the action in terms of electron field \\(\hat{\psi}_\sigma(\r,t)\\). 

$$$$\begin{align}
\L = i\int \sum_\sigma \psi^\dagger_\sigma(\r,t)\frac{\partial}{\partial t}\psi_\sigma(\r,t)d^3\r - H
\end{align}$$$$

the conjugate momentum to \\(\psi_\sigma(\r)\\) is given by 

$$$$\begin{align}
\Pi_\sigma(\r) = \frac{\delta\L}{\delta\dot\psi_\sigma(\r)} = i\psi_\sigma^\dagger(\r)
\end{align}$$$$

Canonical quantization is obtained by imposing anticommutation relations, 

$$$$\begin{align}
\{\psi_\sigma(\r),\Pi_{\sigma'}(\r')\} = i\delta_{\sigma\sigma'}\delta^{(3)}(\r-\r')
\end{align}$$$$
$$$$\begin{align}
\{\psi_\sigma(\r),i\psi^\dagger_{\sigma'}(\r')\} = i\delta_{\sigma\sigma'}\delta^{(3)}(\r-\r')
\end{align}$$$$

Note: For fermions, canonical quantization is modified by imposing anticommutation relations. Also, $$$$\begin{align}\{\psi_\sigma,\psi_{\sigma'}\} = \{\psi_\sigma^\dagger \psi_{\sigma'}^\dagger\} = 0\end{align}$$$$

This fact that these agree with ones obtained from other considerations shows we wrote correct Lagrangian action \\(S = \int \L dt\\). 

Let's now discuss the Feynman path integral in single particle quantum mechanics. Consider the following expression 

$$$$\begin{align}
\bra{\x_f(t_f)}_S\ket{\x_i(t_i)}_S = \bra{\x_f}_H e^{i(t_f - t_i)H}\ket{\x_i}_H,
\end{align}$$$$

which is equal to the probability amplitude that a particle at position \\(\x_i\\) at time \\(t_i\\) ends up at position \\(\x_f\\) at time \\(t_f\\). If we insert resolutions of the identity many times in the form

$$$$\begin{align}
\1 = \int \ket{\x} \bra{\x} d\x,
\end{align}$$$$

then we get 

, then this is proportional to the integral 

$$$$\begin{align}
\int e^{iS[\x(t)]/\hbar} \D\x
\end{align}$$$$

where

$$$$\begin{align}
S[\x] = \int_{t_i}^{t_f}L(\x(t))\d t
\end{align}$$$$

We sum over all the paths starting at \\(\x_i\\) at time \\(t_i\\), and ending at position \\(\x_f\\) at time \\(t = t_f\\). The notation \\(\int \D\x\\) means the sum over all such paths, not just classical ones. 

This can be defined by defining a set of times \\(t_1,t_2,\dots t_N\\) between \\(t_i\\) and \\(t_f\\), so that

$$$$\begin{align}\int \D\x = \prod_{i=1}^N\int \d\x_i\end{align}$$$$

where \\(\x_i\\) is ?? at \\(t_i\\) (do it for each component)

Must take the limit as \\(N\to\infty\\). See Feynman \& Hibbs or Peskin and Schroeder for more details.

This is called a Feynman path integral - a functional integral over all paths \\(x(t)\\). 

The classical limit is recovered as \\(\hbar\to 0\\) because integral is dominated by classical path.

This follows from the ``method of steepest descents", stationary points where

$$$$\begin{align}\frac{\delta S}{\delta x_a(t)} = 0\end{align}$$$$

which implies that

$$$$\begin{align}\frac{d}{dt}\frac{\partial \L}{\partial \dot{x}_a} = \frac{\partial\L}{\partial x_a}\end{align}$$$$

which is the Euler-Lagrange equation. In second quantized theory, fundamental objects are functions of space and time, 

<ul>
	<li> \\(\textbf{S}_\textbf{R}(t)\\) is a spin operator in the Heisenberg model
	</li> 
 <li> \\(\psi_\sigma(\r,t)\\) is an electron field
\end{itemize}

so 

$$$$\begin{align}\bra{\x_f}e^{-\beta H}\ket{\x_i} = \int e^{S_I}\D\x\end{align}$$$$

where \\(S_I = -\int \L d\tau\\).

Functional integrals are now over these functions of space and time. Time is always a continuous variable, although we may discretize it as an approximation, space is discrete in lattice models, e.g. Heisenberg but continuous in continuum models like Jellium.

We weight a given path, i.e. field configuration at all space time points by classical action. There is a very profound analogy between the Feynman path integral in quantum many body theory and classical Boltzmann sum in classical statistical mechanics. 

