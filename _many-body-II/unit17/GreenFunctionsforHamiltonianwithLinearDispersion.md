---
layout: lesson
title: Green Functions for Hamiltonian with Linear Dispersion
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
In this section, we will discuss how to obtain the Green functions for a Hamiltonian with a linear dispersion. Consider a Hamiltonian 

$$\Hhat = \sum_{k\alpha} \epsilon_{k\alpha} \psihat^\dagger_{k\alpha} \psihat_{k\alpha}$$

Here, the dispersions \\(\epsilon_{k\alpha}\\) are linear in \\(k\\), but may have different velocities. We want to compute the imaginary-time evolution of the position space operator 

$$\psihat_\alpha(ix) = \frac{1}{\sqrt{\ell}}\sum_k e^{ikx} \psihat_{k\alpha}, \quad \psihat_{k\alpha} = \frac{1}{\sqrt{\ell}}\int_0^\ell e^{-ikx} \psihat_\alpha(ix)$$

The position space operator time evolution is given by 

$$\begin{align}
e^{\tau\Hhat}\psihat_\alpha(ix)e^{-\tau\Hhat} =& \frac{1}{\sqrt{\ell}}\sum_k e^{ikx} e^{\tau\Hhat} \psihat_{k\alpha} e^{-\tau\Hhat}
\end{align}$$

Noting the anticommutation relation \\(\{\psihat_{k\alpha},\psihat^\dagger_{k'\alpha'}\} = \delta_{kk'}\delta_{\alpha\alpha'}\\), we can write 

$$\begin{align}
e^{\tau\Hhat} \psihat_{k\alpha} e^{-\tau\Hhat} =& \sum_{n=0}^\infty \frac{\tau^n}{n!}[\Hhat,[\Hhat,\dots,[\Hhat,\psihat_{k\alpha}],\dots]]
\end{align}$$

We therefore need to compute 

$$[\Hhat,\psihat_{k\alpha}] = -\epsilon_{k\alpha}\psihat_{k\alpha}$$

Thus we find that 

$$\begin{align}
e^{\tau\Hhat} \psihat_{k\alpha} e^{-\tau\Hhat} =& \sum_{n=0}^\infty \frac{\tau^n(-\epsilon_{k\alpha})^n}{n!} \psihat_{k\alpha} \\
=& e^{-\tau\epsilon_{k\alpha}}\psihat_{k\alpha}
\end{align}$$

Plugging this back in, we find that for the case of a right-moving field (\\(\epsilon_{k\alpha} = v_Fk\\)), the time evolution is 

$$\begin{align}
e^{\tau\Hhat}\psihat_\alpha(ix)e^{-\tau\Hhat} =& \psihat_\alpha(ix-\tau v_F)
\end{align}$$

For the case of a right-moving field we actually write \\(\psihat_\alpha(-ix)\\) and \\(\psihat_\alpha(v_F\tau - ix)\\). Thus, the Heisenberg time evolution of a right-moving field depends on \\(z^{*} = v_F\tau - ix\\), whereas the Heisenberg time evolution of a left-moving field depends on \\(z = v_F\tau + ix\\). Now that we have this established, we may compute the Matsubara Green functions for each of these types of fields. For a left-moving field, 

$$\mathcal{G}_L(x,\tau;x',\tau') = -\langle T_\tau[\psihat(x,\tau)\psihat^\dagger(x',\tau') ]\rangle.$$

We know how to compute this in momentum space, and the simple answer yields 

$$\mathcal{G}_L(k,\tau;k',\tau') = -(\theta(\tau-\tau') - n_F(\xi_k))e^{-(\tau-\tau')\xi_k} \delta_{kk'}$$

Now, we need to Fourier transform this back to position space. Doing this gives us 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& \frac{1}{L}\sum_{kk'}e^{ikx}e^{-ik'x'}\mathcal{G}_L(k,\tau;k',\tau') \\
=& -\frac{1}{L}\sum_{kk'}e^{ikx}e^{-ik'x'}(\theta(\tau-\tau')-n_F(\xi_k))e^{-(\tau-\tau')\xi_k}\delta_{kk'} \\
=& -\frac{1}{L}\sum_{k}e^{ik(x-x')}(\theta(\tau-\tau')-n_F(\xi_k))e^{-(\tau-\tau')\xi_k}
\end{align}$$

If you wish, you may evaluate this integral as an exercise using contour methods.

