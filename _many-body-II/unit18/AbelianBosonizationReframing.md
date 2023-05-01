---
layout: lesson
title: Abelian Bosonization Reframing
dept: physics
course: many-body-II
unit: unit18
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 18
---
In abelian bosonization, we derived the relationship

$$\psihat(x) = \frac{\Fhat}{\sqrt{2\pi a}}e^{-i\Phihat(x)}.$$

There is no direct analogue of this to derive for nonabelian bosonization, but there is a different relation. The current operators are given by 

$$\Jhat_R(z^{*}) = :\psihat^\dagger_R(z^{*})\psihat_R(z^{*}):,\quad \Jhat_L(z) = :\psihat^\dagger_L(z)\psihat_L(z):$$

Note that it should be no coincidence that these current operators look identical to the density operators. This is because the continuity equation which relates these two quantities takes a particularly simple form due to the fact that the position and time coordinates appear together in a linear combination when the dispersion relation is linear in \\(k\\). 



We start with the free fermion Hamiltonian that we derived above from the tight-binding model, but this time for spinless fermions:

$$H_0 = v_F\sum_k k\left[-:\psihat^\dagger_{kL}\psihat_{kL}: + :\psihat^\dagger_{kR}\psihat_{kR}:\right]$$

We now Fourier transform the fields according to 

$$\psihat_L(x) = \sum_k e^{ikx} \psihat_{Lk},\quad \psihat_R(x) = \sum_k e^{ikx} \psihat_{Rk}$$

which gives us the position space Hamiltonian

$$H_0 = -iv_F\int_0^\ell \left[:\psihat^\dagger_R(x)\partial_x\psihat_R(x): - :\psihat^\dagger_L(x)\partial_x\psihat_L(x):\right] \d x$$

Let us now determine the dynamics of the left and right moving Fermi fields in imaginary time. We find that FILL IN THE DETAILS

$$\begin{align}
\psihat_R(x,\tau) =& e^{\tau \Hhat_0} \psihat_R(x) e^{-\tau\Hhat_0} \\
=& \psihat_R(x+iv_F\tau) 
\end{align}$$

and similarly for the left moving field \\(\psihat_L(x,\tau) = \psihat_L(x-i\tau)\\). We define insteasd \\(\psihat_R(x+iv_F\tau) \to \psihat_R(v_F\tau-ix)\\) and \\(\psihat_L(x-iv_F\tau)\to \psihat_L(v_F\tau + ix)\\). This is just 'factoring' and \\(i\\) out of the arguments. Now, we  define \\(z = v_F\tau + ix\\) and \\(z^{*} = v_F\tau - ix\\). Now, the left-moving quantities will depend on \\(z\\), whereas the right-moving quantities will depend on \\(z^{*}\\). This is a signature of conformal invariance; the linear dispersion is crucial for this. 


