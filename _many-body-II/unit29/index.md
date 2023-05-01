---
layout: lesson
title: Models of Electron-Phonon Coupling
dept: physics
course: many-body-II
unit: unit29
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 29
---

Consider a single band of conduction electrons
$$\Hhat_\text{el} = \sum_{\k\sigma} \xi_{\k}\chat^\dagger_{\k\sigma} \chat_{\k\sigma}$$

and also phonons with 3 possible polarizations 

$$\Hhat_\text{ph} = \sum_{\q j} \omega_{\q j}\left(\bhat^\dagger_{\q j} \bhat_{\q j} + \frac{1}{2}\right)$$

The coupling between electrons and phonons is given by the following:

$$\Hhat_\text{el-ph} = g \sum_{\k \sigma \q j} \chat^\dagger_{\k+\q,\sigma} \chat_{\k\sigma}\left(\bhat_{\q j} + \bhat^\dagger_{-\q,j}\right)$$

We can simplify notation by defining \\(\nhat_{\q} = \sum_{\k\sigma} \chat^\dagger_{\k+\q,\sigma} \chat_{\k\sigma}\\). Then 

$$\Hhat_\text{el-ph} = g \sum_{\q j} \nhat_{\q} \left(\bhat_{\q j} + \bhat^\dagger_{-\q,j}\right)$$

We can generate an attractive interaction between electrons by integrating out the phonons. Removing the zero point energy, the imaginary time action is 

$$S = \sum_{\k\omega\sigma} (-i\omega+\xi_{\k})\bar{c}_{\k\omega\sigma} c_{\k\omega\sigma} + \sum_{\q\nu j}(-i\nu + \omega_{\q j})b^{*}_{\q\nu j} b_{\q \nu j} + \frac{g}{\sqrt{\beta N}} \sum_{\q \nu j} n_{\q\nu} (b_{\q\nu j} + b^{*}_{-\q,-\nu,j})$$

where now 

$$n_{\q\nu} = \sum_{\k\omega\sigma} \bar{c}_{\k+\q,\omega+\nu,\sigma} c_{\k\omega\sigma}.$$

If we wish to integrate out the phonon fields, we can rewrite the interaction term as 

$$S_\text{el-ph} = \frac{g}{\sqrt{\beta N}} \sum_{\q \nu j} (n_{\q\nu} b_{\q\nu j} + n_{-\q,-\nu} b^{*}_{\q\nu j})$$

Now integrating out the phonons, we need to evaluate the integral

$$\int e^{-S_\text{ph} - S_\text{el-ph}} \D b^{*} \D b = \prod_{\q \nu j} \left[\int e^{-(-i\nu + \omega_{\q j})b^{*}_{\q \nu j} b_{\q \nu j} - g(n_{\q\nu} b_{\q\nu j} + n_{-\q-\nu} b^{*}_{\q \nu j})} \d b^{*}_{\q \nu j} \d b_{\q \nu j}\right]$$

Writing \\(b_{\q\nu j} = \Re(b_{\q\nu j}) + i\Im(b_{\q\nu j})\\), we evaluate this integral exactly to get 

$$\begin{align}
\int e^{-S_\text{ph} - S_\text{el-ph}} \D b^{*} \D b =& \prod_{\q \nu j} \exp\left(\frac{g^2}{\beta N} \frac{(n_{\q\nu} + n_{-\q,-\nu})^2}{4(-i\nu + \omega_{\q j})} - \frac{g^2}{\beta N}\frac{(n_{\q\nu} - n_{-\q,-\nu})^2}{4(-i\nu + \omega_{\q j})}\right) \\
=& \exp\left(\frac{g^2}{\beta N} \sum_{\q \nu j} \frac{n_{\q\nu} n_{-\q,-\nu}}{-i\nu + \omega_{\q j}}\right) \\
=& \exp\left(\frac{g^2}{\beta N} \sum_{\q \nu j} \frac{\omega_{\q j} n_{\q\nu} n_{-\q,-\nu}}{\nu^2 + \omega_{\q j}^2}\right) \\
\end{align}$$

Now, this gives us the effective action

$$S_\text{eff} = S_\text{el} - \frac{g^2}{\beta N} \sum_{\q\nu j} \frac{\omega_{\q j} n_{\q\nu} n_{-\q,-\nu}}{\nu^2 + \omega_{\q j}^2} $$

The interaction is attractive for small frequencies. This can be seen by analytically continuing \\(\nu \to -i\omega\\). Thus we require \\(\omega < \omega_{\q j}\\) for attraction to occur. 

\section{Superconductivity Beyond \\(s\\)-wave: the \\(t\\)-\\(J\\) Model}
In this section, we will study the \\(t\\)-\\(J\\) model. The model describes electrons hopping on a lattice in the presence of a large on-site repulsion. This large on-site repulsion restricts the Hilbert space to contain only singly occupied and empty sites, at least for less than half-filling. This is the the model that many believe to be the basis for high-\\(T_c\\) superconductivity in the cuprates. However, since this is a many-body physics course, not a superconductivity or magnetism course, we will be sloppy and pretend as though there are no constraints on the Hilbert space. In this simplified and approximate situation, we can study superconductivity in this model. 

The model is (without projectors)

$$H = -t\sum_{\left<i,j\right>,\sigma} \chat^\dagger_{i\sigma} \chat_{j\sigma} + J\sum_{\left<i,j\right>}\left(\hat{\textbf{S}}_i\cdot\hat{\textbf{S}}_j - \frac{\nhat_i\nhat_j}{4}\right)$$


