---
layout: lesson
title: Charge Density Wave Order
dept: physics
course: many-body-II
unit: unit10
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 10
---
In this section, we will apply the path integral formalism that we have developed to study the possibility of charge density waves in the Fermi Hubbard model. Physically, this order corresponds to the possibility that there are more charges (electrons) built up at certain sites on the lattice in some ordered fashion. What we will find is that the Hubbard model does not exhibit charge density wave order. 

We begin by writing the path integral formulation for the Hubbard model on a \\(d\\)-dimensional square lattice. To remind the reader, the Hubbard model in operator language is given by 

$$$$\begin{align}
\Hhat = -t\sum_{\left<i,j\right>,\sigma}(\chat^\dagger_{i\sigma}\chat_{j\sigma} + \hc) + U\sum_i \chat^\dagger_{i\uparrow}\chat^\dagger_{i\downarrow}\chat_{i\downarrow}\chat_{i\uparrow} - \mu\sum_{i\sigma}\chat^\dagger_{i\sigma}\chat_{i\sigma}.
\end{align}$$$$

The corresponding effective action for the path integral is then given by

$$$$\begin{align}
S = \int_0^\beta\left[ \sum_{i,\sigma} \bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} -t\sum_{\left<i,j\right>,\sigma}(\bar{c}_{i\tau\sigma}c_{j\tau\sigma} + \bar{c}_{j\tau\sigma}c_{i\tau\sigma}) + U\sum_i \bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow} - \mu\sum_{i\sigma}\bar{c}_{i\tau\sigma}c_{i\tau\sigma}\right] \d\tau
\end{align}$$$$

We split up this action into two parts: a non-interacting part \\(S_0\\) and an interacting part \\(S_\text{int}\\):

$$\begin{align}
S_0 =& \int_0^\beta\left[ \sum_{i,\sigma} \bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} -t\sum_{\left<i,j\right>,\sigma}(\bar{c}_{i\tau\sigma}c_{j\tau\sigma} + \bar{c}_{j\tau\sigma}c_{i\tau\sigma}) - \mu\sum_{i\sigma}\bar{c}_{i\tau\sigma}c_{i\tau\sigma}\right] \d\tau \\
S_\text{int} =& \int_0^\beta U\sum_i \bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow} \d\tau.
\end{align}$$

The partition function for the system is then simply written as 

$$$$\begin{align}
Z = \int e^{-S_0 - S_\text{int}}\D\bar{c}\D c.
\end{align}$$$$

We focus now on the interaction term, and perform a Hubbard-Stratonovich transformation. There are different ways to set up the transformation, but, since we are looking for charge density waves, we will pick the \textit{density channel}. To pick the density channel, we look for a Hubbard-Stratonovich field \\(\phi\\) which couples to the number operator. Recalling the identity

$$$$\begin{align}
\int e^{-a\phi^2 - b\phi} \d \phi \propto e^{b^2/4a}
\end{align}$$$$

we set 

$$$$\begin{align}
\frac{b^2}{4a} = -U\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow}.
\end{align}$$$$

and, since we want the Hubbard-Stratonovich field, to couple to the number operator, we let \\(b = -i(\bar{c}_{i\tau\uparrow}c_{i\tau\uparrow} + \bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}) = -i\sum_\sigma \bar{c}_{i\tau\sigma}c_{i\tau\sigma}\\). Then, if \\(a = 1/2U\\), we get that indeed the above equation is satisfied. We note that we could have set \\(a=1\\) and absorbed everything else into \\(b\\), but this is not conventional. It is not possible to let \\(a\\) be negative because then the integral would not converge. Equipped with the transformation, we will make use of the easily-verifiable identity 

$$$$\begin{align}
\int \exp\left(-\frac{1}{2U}\phi_{i\tau}^2 + i\phi_{i\tau}(\bar{c}_{i\tau\uparrow}c_{i\tau\uparrow} + \bar{c}_{i\tau\downarrow}c_{i\tau\downarrow})\right)\d\phi_{i\tau} = \exp\left(-U\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow}\right).
\end{align}$$$$

This means that we can write the term

$$$$\begin{align}
\exp\left(-\int_0^\beta\sum_i U\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow}\right) = \int \exp\left(-\int_0^\beta\sum_i\left[ \frac{1}{2U}\phi_{i\tau}^2 - i\phi_{i\tau}(\bar{c}_{i\tau\uparrow}c_{i\tau\uparrow} + \bar{c}_{i\tau\downarrow}c_{i\tau\downarrow})\right] \d\tau\right)\D\phi.
\end{align}$$$$

This allows us to rewrite the interaction term of the effective action as 

$$$$\begin{align}
S_\text{int} = \int_0^\beta\sum_i\left[ \frac{1}{2U}\phi_{i\tau}^2 - i\sum_\sigma \phi_{i\tau}\bar{c}_{i\tau\sigma} c_{i\tau\sigma}\right]\d\tau
\end{align}$$$$

as long as we remember to include the path integral measure for the \\(\phi\\) field in the partition function. For the next step, we will Fourier transform all of our fields in spacetime. We will apply the Fourier conventions 

$$$$\begin{align}
c_{i\tau\sigma} = \frac{1}{\sqrt{N\beta}}\sum_k e^{-ik_0\tau + i\textbf{R}_i\cdot\k} c_{k\sigma},\qquad \bar{c}_{i\tau\sigma} = \frac{1}{\sqrt{N\beta}}\sum_k e^{ik_0\tau - i\textbf{R}_i\cdot\k} \bar{c}_{k\sigma}, \qquad \phi_{i\tau} = \frac{1}{\beta N}\sum_k e^{-ik_0\tau + i\textbf{R}_i\cdot\k}\phi_k 
\end{align}$$$$

where we emphasize that \\(k\\) is a vector containing both a Matsubara frequency as well as a crystal momentum in each of these cases. For the \\(c,\bar{c}\\) fields, the sum over Matsubara frequencies is over fermionic frequencies, whereas for the \\(\phi\\) field, it is over bosonic frequencies. Now, we Fourier transform the action. The two terms of the action become

$$$$\begin{align}
S_0 = \sum_{k\sigma}\bar{c}_{k\sigma}(-ik_0 + \xi_{\k})c_{k\sigma},\qquad S_\text{int} = \frac{1}{2U \beta N}\sum_{k}\phi_k \phi_{-k} - \frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\bar{c}_{k+p,\sigma}c_{p\sigma}
\end{align}$$$$

Finally, we plug these two expressions back in to the path integral: 

$$$$\begin{align}
Z = \int e^{-S_0} \exp\left(-\frac{1}{2U\beta N}\sum_k\phi_k\phi_{-k} \right)\exp\left(\frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\bar{c}_{k+p,\sigma}c_{p\sigma}\right)\D\bar{c}\D c\D\phi
\end{align}$$$$

We rearrange the order of the terms and place brackets to rewrite everything in terms of an effective action \\(S_\text{eff}[\phi]\\), which we will evaluate perturbatively in powers of \\(\phi\\). 

$$\begin{align}
Z =& \int \exp\left(-\frac{1}{2U\beta N}\sum_k\phi_k\phi_{-k} \right)\left[\int e^{-S_0} \exp\left(\frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\bar{c}_{k+p,\sigma}c_{p\sigma}\right)\D\bar{c}\D c\right]\D\phi \\
=& \int \exp\left(-\frac{1}{2U\beta N}\sum_k\phi_k\phi_{-k} \right)Z_0\left<\exp\left(\frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\bar{c}_{k+p,\sigma}c_{p\sigma}\right)\right>_0\D\phi \\
=& Z_0\int e^{-S_\text{eff}[\phi]}\D\phi
\end{align}$$

where we define

$$$$\begin{align}
S_\text{eff}[\phi] = \frac{1}{2U\beta N}\sum_k\phi_k\phi_{-k} \underbrace{-\log \left<\exp\left(\frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\bar{c}_{k+p,\sigma}c_{p\sigma}\right)\right>_0}_{\Delta S_\text{eff}}
\end{align}$$$$

$$$$\begin{align}
Z_0 = \int e^{-S_0}\D\bar{c}\D c,\qquad \left<A\right>_0 = \frac{1}{Z_0}\int  e^{-S_0}A\D\bar{c}\D c.
\end{align}$$$$

To evaluate the partition function, we will calculate \\(\Delta S_\text{eff}\\) perturbatively. We do this by employing the cumulant expansion, and we will expand to second order in the field \\(\phi\\). The cumulant expansion is then given by 

$$\log \left<e^A\right> = \left<A\right>_c + \frac{1}{2!}\left<A^2\right>_c + \frac{1}{3!}\left<A^3\right>_c + \cdots,$$

where the first three cumulants are

$$\left<A\right>_c = \left<A\right>,\quad \left<A^2\right>_c = \left<A^2\right> - \left<A\right>^2,\quad \left<A^3\right>_c = ...$$

We therefore let

$$\Delta S^{(1)}_\text{eff} = -\left<\frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\bar{c}_{k+p,\sigma}c_{p\sigma}\right>_0$$

and 

$$\Delta S^{(2)}_\text{eff} = -\frac{1}{2}\left[\left<\left(\frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\bar{c}_{k+p,\sigma}c_{p\sigma}\right)^2\right>_0 - \left<\frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\bar{c}_{k+p,\sigma}c_{p\sigma}\right>_0^2\right].$$

First, let's evaluate \\(\Delta S^{(1)}_\text{eff}\\):

$$\begin{align}
\Delta S^{(1)}_\text{eff} =& -\frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\left<\bar{c}_{k+p,\sigma}c_{p\sigma}\right>_0 \\
=& -\frac{i}{\beta N}\sum_{k,p,\sigma}\phi_k\delta_{k,0}\mathcal{G}_0(p) \\
=& -\frac{2i}{\beta N}\sum_{p}\phi(k=0)\mathcal{G}_0(p) \\
=& -\frac{2i\phi(k=0)}{\beta N}\sum_{ip_0,\p}\frac{1}{ip_0 - \xi_{\k}} \\
=& -\frac{2i\phi(k=0)}{N}\sum_{\p} n_F(\xi_{\k}) 
\end{align}$$

We recognize \\(\sum_{\p} n_F(\xi_{\k})\\) as the total number of points occupied in \\(\k\\) space. Thus, the total number of electrons in the system is 2 times that due to spin. We can therefore rewrite 

$$$$\begin{align}
\Delta S^{(1)}_\text{eff} = -i\phi(k=0)\rho 
\end{align}$$$$

where \\(\rho = \frac{2}{N}\sum_{\p} n(\xi_{\p})\\) is the density (including spin) of electrons in the solid. Unfortunately, we were hoping that the first order term would be zero, so that all even order terms are the only important ones. To fix this, we will add and subtract

$$\begin{align}
S_\text{int} =& \frac{1}{2U\beta N}\sum_k \phi_k \phi_{-k} - \frac{i}{\beta N}\sum_{k,p}\phi_k(\sum_\sigma \bar{c}_{k+p,\sigma}c_{p\sigma} - \rho + \rho). \\
=& \int_0^\beta \left[\frac{1}{2U}\sum_i \phi_i^2 - i\sum_{k,p}\phi_i(\sum_\sigma \bar{c}_{i\sigma}c_{i\sigma} - \rho + \rho) \right]\d\tau.
\end{align}$$

If we go back and integrate out the Hubbard-Stratonovich field, then we arrive back at the interaction 

$$S_\text{int} = $$




