---
layout: lesson
title: RKKY Interaction
dept: physics
course: many-body-II
unit: unit31
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 31
---
The RKKY (Ruderman-Kittel-Kasuya-Yosida) interaction describes the effective interaction between local moments mediated by the conduction electrons. To derive what this interaction is, we need to integrate out of the fermions. The effective action for the Kondo lattice is simply

$$$$\begin{align}
S = S^S_0 + \int_0^\beta \left( \sum_{\k\sigma} \bar{c}_{\k\tau\sigma} (\partial_\tau + \xi_{\k})c_{\k\tau\sigma} + J\sum_i \bar{c}_{i\tau\alpha} c_{i\tau\beta} \frac{\boldsymbol{\sigma}_{\alpha\beta}}{2}\cdot \textbf{S}_{i\tau} \right)\d\tau
\end{align}$$$$

Where \\(S^S_0\\) is the Berry term for the spin coherent states. The precise form of this term is not important because we are only interested in integrating out the fermions. Details of the spin coherent state path integral are in section ??. The partition function for the system is simply

$$$$\begin{align}
Z = \int e^{-S} \D \bar{c}\D c \D\textbf{S}
\end{align}$$$$

The action is then written as 

$$$$\begin{align}
S = S^S_0 + \int_0^\beta \left( \sum_{\k\sigma} \bar{c}_{\k\tau\sigma} (\partial_\tau + \xi_{\k})c_{\k\tau\sigma} + J\sum_i \bar{c}_{i\tau\alpha} c_{i\tau\beta} \frac{\boldsymbol{\sigma}_{\alpha\beta}}{2}\cdot \textbf{S}_{i\tau} \right)\d\tau
\end{align}$$$$

We wish to rewrite the partition function as

$$$$\begin{align}
Z = \int e^{-S_\text{eff}}\D\textbf{S}
\end{align}$$$$

To compute the effective action by integrating out fermions, we need to change everything to momentum space. We do this by defining the Fourier transformed Grassmann fields (in both space and in imaginary time)

$$$$\begin{align}
c_{i\tau\sigma} = \frac{1}{\sqrt{\beta N_s}} \sum_k e^{i(\textbf{R}_i\cdot\k - k_0\tau)} c_{k\sigma}, \quad \bar{c}_{i\tau\sigma} = \frac{1}{\sqrt{\beta N_s}} \sum_k e^{-i(\textbf{R}_i\cdot\k - k_0\tau)} \bar{c}_{k\sigma}, \quad \textbf{S}_{i\tau} = \frac{1}{\beta N_s} \sum_k e^{i(\textbf{R}_i\cdot\k - k_0\tau)}
\end{align}$$$$

where \\(k_0\\) is a Fermionic Matsubara frequency, and \\(k = (k_0,\k)\\) represents the momentum-Matsubara frequency 4-vector. Now, we Fourier transform everything

$$$$\begin{align}
S = S^S_0 + \sum_{k\sigma} \bar{c}_{k\sigma} (-ik_0 + \xi_{\k})c_{k\sigma} + \frac{J}{\beta N_s} \sum_{kq} \bar{c}_{k\alpha} c_{q\beta} \frac{\boldsymbol{\sigma}_{\alpha\beta}}{2}\cdot\textbf{S}_{k-q}
\end{align}$$$$

One final rewriting brings us to a simple form which will be easy to integrate out:

$$$$\begin{align}
S = S^S_0 - \sum_{kq\alpha\beta} \bar{c}_{k\alpha}\left[\delta_{kq}\delta_{\alpha\beta}\mathcal{G}^{-1}_0(\k,ik_0) - \frac{J}{2\beta N_s}\boldsymbol{\sigma}_{\alpha\beta}\cdot\textbf{S}_{k-q} \right] c_{k\beta}
\end{align}$$$$

where the free Green function is \\(\mathcal{G}_0(\k,ik_0) = \frac{1}{ik_0 - \xi_{\k}}\\). Then, using the common formula 

$$$$\begin{align}
\int e^{\bar{c}A c} \D\bar{c}\D c = \det(A)
\end{align}$$$$

we can write the partition function as 

$$$$\begin{align}
Z = \int e^{-S^S_0} \left[\int\exp\left(\sum_{kq\alpha\beta} \bar{c}_{k\alpha}\left[\delta_{kq}\delta_{\alpha\beta}\mathcal{G}^{-1}_0(\k,ik_0) - \frac{J}{2\beta N_s}\boldsymbol{\sigma}_{\alpha\beta}\cdot\textbf{S}_{k-q} \right] c_{k\beta}\right) \D\bar{c}\D c \right]\D\textbf{S}
\end{align}$$$$

and then doing the integration we find that 

$$$$\begin{align}
Z = \int e^{-S^S_0} \det\left(\delta_{kq}\delta_{\alpha\beta}\mathcal{G}^{-1}_0(\k,ik_0) - \frac{J}{2\beta N_s}\boldsymbol{\sigma}_{\alpha\beta}\cdot\textbf{S}_{k-q}  \right)\D\textbf{S}
\end{align}$$$$

where the determinant is computed over both the spin indices and 4-momenta. We factor this to get 

$$$$\begin{align}
Z = \underbrace{\det\left(\mathcal{G}^{-1}_0(\k,ik_0)\right)}_{Z_0} \int e^{-S^S_0} \det\left(\delta_{kq}\delta_{\alpha\beta} - \frac{J}{2\beta N_s}\mathcal{G}_0(\k,ik_0)\boldsymbol{\sigma}_{\alpha\beta}\cdot\textbf{S}_{k-q}  \right)\D\textbf{S}
\end{align}$$$$

Now, we use the formula \\(\det(A) = e^{\tr\log A}\\) to get 

$$$$\begin{align}
Z = Z_0 \int e^{-S^S_0} \exp\left[\tr\log\left(\delta_{kq}\delta_{\alpha\beta} - \frac{J}{2\beta N_s}\mathcal{G}_0(\k,ik_0)\boldsymbol{\sigma}_{\alpha\beta}\cdot\textbf{S}_{k-q} \right) \right]\D\textbf{S}
\end{align}$$$$

Then, the effective action is given by 

$$$$\begin{align}
S_\text{eff} = S^S_0 - \tr\log\left(\delta_{kq}\delta_{\alpha\beta} - \frac{J}{2\beta N_s}\mathcal{G}_0(\k,ik_0)\boldsymbol{\sigma}_{\alpha\beta}\cdot\textbf{S}_{k-q}\right)
\end{align}$$$$

We now need to Taylor expand the logarithm and take the trace. The first order correction is zero because \\(\tr\boldsymbol{\sigma} = 0\\), but the second order correction corresponds to the RKKY interaction and is given by 

$$$$\begin{align}
S_\text{eff}^{(2)} = -\frac{1}{2}\frac{J^2}{4\beta^2N_s^2} \sum_{\substack{ k_1q_1\alpha_1\beta_1 \\ k_2q_2\alpha_2\beta_2}}\left(\mathcal{G}_0(\k_1,i\omega_1)\boldsymbol{\sigma}_{\alpha_1\beta_1}\cdot\textbf{S}_{k_1-q_1}\right)\delta_{q_1k_2}\delta_{\beta_1\alpha_2}\left(\mathcal{G}_0(\k_2,i\omega_2)\boldsymbol{\sigma}_{\alpha_2\beta_2}\cdot\textbf{S}_{k_2-q_2}\right)\delta_{q_2k_1}\delta_{\beta_2\alpha_1}
\end{align}$$$$

Simplifying this gives 

$$$$\begin{align}
S_\text{eff}^{(2)} = -\frac{1}{2}\frac{J^2}{4\beta^2N_s^2} \sum_{kq\alpha\beta} \left(\mathcal{G}_0(\k,ik_0) \boldsymbol{\sigma}_{\alpha\beta}\cdot\textbf{S}_{k-q}\right)\left(\mathcal{G}_0(\q,iq_0)\boldsymbol{\sigma}_{\beta\alpha} \cdot\textbf{S}_{q-k}\right)
\end{align}$$$$

Then, we use the relation that \\(\tr\left(\sigma^{\ell_1}\sigma^{\ell_2}\right) = 2\delta_{\ell_1\ell_2}\\). This gives 

$$$$\begin{align}
S_\text{eff}^{(2)} = -\frac{J^2}{4\beta^2N_s^2} \sum_{kq} \mathcal{G}_0(\k,ik_0)\mathcal{G}_0(\q,iq_0)\textbf{S}_{k-q}\cdot \textbf{S}_{q-k}
\end{align}$$$$

We now replace \\(k-q\mapsto k\\) so that 
 
$$$$\begin{align}
S_\text{eff}^{(2)} = -\frac{J^2}{4\beta^2N_s^2} \sum_{kq} \mathcal{G}_0(\k+\q,ik_0+iq_0)\mathcal{G}_0(\q,iq_0)\textbf{S}_{k}\cdot \textbf{S}_{-k}
\end{align}$$$$

Then defining the polarizability function

$$\begin{align}
\pi(\k,ik_0) =& -\frac{1}{\beta N_s} \sum_q \mathcal{G}_0(\k+\q,ik_0+iq_0)\mathcal{G}_0(\q,iq_0) \\
=& -\frac{1}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + ik_0}
\end{align}$$

we can write the contribution to the effective action as 

$$$$\begin{align}
S_\text{eff}^{(2)} = \frac{J^2}{4\beta N_s} \sum_{k} \pi(\k,ik_0)\textbf{S}_{k}\cdot \textbf{S}_{-k}
\end{align}$$$$

The function \\(\pi\\) has Friedel oscillations. 


