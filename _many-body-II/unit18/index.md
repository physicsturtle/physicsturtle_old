---
layout: lesson
title: Nonabelian Bosonization
dept: physics
course: many-body-II
unit: unit18
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 18
---
QUESTION: CAN WE KEEP USING THE SAME FOURIER TRANSFORM OR DOES THIS MESS UP LEFT VS. RIGHT MOVERS? IF WE USE THE CORRECT DISPERSION RELATION, ARE WE GOING TO BE OK?

Let us establish a few conventions. For left movers, we will have \\(\xi_k = -v_Fk\\), for right movers, we will have \\(\xi_k = v_Fk\\). We will also set \\(\{\psihat(x),\psihat^\dagger(y)\} = \delta(x-y)\\). With the following Fourier transforms 

$$\psihat(x) = \frac{1}{\sqrt{\ell}}\sum_k e^{ikx} \psihat(k), \quad \psihat^\dagger(x) = \frac{1}{\sqrt{\ell}} \sum_k e^{-ikx} \psihat^\dagger(k)$$
$$\psihat(k) = \frac{1}{\sqrt{\ell}}\int_{-\ell/2}^{\ell/2} e^{-ikx} \psihat(x) \d x,\quad \psihat^\dagger(k) = \frac{1}{\sqrt{\ell}}\int_{-\ell/2}^{\ell/2} e^{ikx} \psihat^\dagger(x) \d x$$

we can derive the following canonical anticommutation relations for the Fourier transformed operators: \\(\{\psihat(k),\psihat^\dagger(k')\} = \delta_{kk'}\\). When we are later computing ground state correlators for the purposes of using Wick's theorem, we need to define a Hamiltonian whose ground state is the desired one. We define the following Hamiltonian (of left movers) to be 

$$H = -v_F\sum_k k\psihat^\dagger(k) \psihat(k) = .$$

The time-ordered ground state correlators are then given by 

$$\begin{align}
\mathcal{G}(x,\tau;x',\tau') =& -\langle T_\tau[\psihat(x,\tau) \psihat^\dagger(x',\tau')]\rangle \\
=& -\frac{1}{2\pi}\frac{1}{\frac{\beta v_F}{\pi}\sin\frac{\pi}{\beta v_F}(z-z')}
\end{align}$$

where \\(z = \tau + ix\\), \\(z' = \tau' + ix'\\). The important cases are wanting to compute (for \\(|x-x'|\\) small)

$$\langle \psihat(x)\psihat^\dagger(x') \rangle = -\lim_{\tau\to\tau^{\prime +}}\mathcal{G}(x,\tau;x',\tau') = \frac{1}{2\pi i(x-x')}$$
$$\langle \psihat^\dagger(x')\psihat(x) \rangle = \lim_{\tau'\to\tau^+} \mathcal{G}(x,\tau;x',\tau') = \frac{1}{2\pi i(x'-x)}$$

These will appear when we apply Wick's theorem.

GENERALLY SPEAKING: we can have left and right movers with opposite Fourier transform convention but the same energy, OR, we can have the same Fourier transform convention but opposite (negative of each other) energy. 

