---
layout: lesson
title: Tomonaga Form of Hamiltonian
dept: physics
course: many-body-II
unit: unit18
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 18
---

With the following formula for the OPE of two currents, 

$$\begin{align}
\Jhat(z_1^{*})\Jhat(z_2^{*}) =& \frac{1}{z_{12}^{*2}} +\partial_{z^{*}}\psihat^\dagger(z_2^{*})\psihat(z_2^{*}) - \psihat^\dagger(z_2^{*})\partial_{z^{*}}\psihat(z_2^{*})
\end{align}$$

we can take the normal ordering of both sides to subtract the divergence and find 

$$\begin{align}
:\Jhat(z_1^{*})\Jhat(z_2^{*}): =& \partial_{z^{*}}\psihat^\dagger(z_2^{*})\psihat(z_2^{*}) - \psihat^\dagger(z_2^{*})\partial_{z^{*}}\psihat(z_2^{*})
\end{align}$$

We recognize this as (after doing integration by parts and dividing by 2), what appears in the Hamiltonian!

$$\Hhat = \int_0^\ell \frac{1}{2}:\Jhat(ix)\Jhat(ix): \frac{\d x}{2\pi} $$

THerefore, we can rewrite this in terms of the stress-energy tensor 

$$\Hhat = \int_0^\ell \That(z) \frac{\d x}{2\pi} - \frac{2\pi}{\ell} \frac{c}{24}$$

\subsection{Spin charge separation}
Consider the Hamiltonian

$$\Hhat = i\frac{v_F}{2}\int_{-\infty}^\infty \left(\psihat^\dagger_\sigma \frac{\d}{\d x}\psihat_\sigma  - \frac{\d}{\d x}\psihat^\dagger_\sigma \psihat_\sigma\right)\d x$$

One option for writing this Hamiltonian in terms of bosonic currents is that we could use the abelian bosonization construction from earlier twice: once for each flavour of fermion. However, this Hamiltonian has \\(\SU(2)\\) invariance, and we want to write the Hamiltonian in a manifestly \\(\SU(2)\\) invariant way after the introduction of the bosonic currents. For this, we define a charge current and a spin current:

$$\Jhat(x) = :\psihat_\alpha^\dagger(x) \sigma^0_{\alpha\beta} \psihat_\beta(x):,\quad \hat{\boldsymbol{J}}(x) = :\psihat_\alpha^\dagger(x) \frac{\boldsymbol{\sigma}_{\alpha\beta}}{2}\psihat_\beta(x):$$

