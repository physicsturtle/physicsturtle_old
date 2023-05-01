---
layout: lesson
title: Kondo Hamiltonian
dept: physics
course: many-body-II
unit: unit13
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 13
---
The Kondo Hamiltonian is given by

$$$$\begin{align}
\Hhat = \sum_{\k} \epsilon_{\k} \chat^\dagger_{\k\sigma} \chat_{\k\sigma} + J\chat^\dagger_{0\alpha}\boldsymbol{\sigma}_{\alpha\beta} \chat_{0\beta} \cdot\hat{\textbf{S}}
\end{align}$$$$

If we change the conduction electron operators into momentum space, we find that 

$$$$\begin{align} 
\Hhat = \sum_{\k} \epsilon(\k)  \chat_{\k\sigma}^\dagger \chat_{\k\sigma}+ \frac{J}{N}\sum_{\k,\k'\alpha,\beta} \chat^\dagger_{\k\alpha}\boldsymbol{\sigma}_{\alpha\beta} \chat_{\k'\beta}\cdot \hat{\textbf{S}}\end{align}$$$$

where \\(\textbf{S} = \frac{1}{2}\boldsymbol{\sigma}\\) are a vector of \\(S = 1/2\\) spin operators, satisfying the following Lie algebra

$$$$\begin{align}[\hat{S}^a,\hat{S}^b] = i\epsilon^{abc}\hat{S}^c,\end{align}$$$$

where \\(\hat{S}^a\\) are operators acting on the \\(a\\)th component acting on the impurity spin, which could be in an up or down state. The first term is the kinetic energy of an electron moving in the presence of the ionic potential, and the second term is the scattering potential. We can expand this second term, \\(\Hhat_\text{int}\\) out by expanding out the dot product, then summing over \\(\alpha\\) and \\(\beta\\). Note that \\(\alpha\\) and \\(\beta\\) are the indices of the elements in a given Pauli matrix, so they each run from 1 to 2. 

$$\begin{align}
\Hhat_\text{int} =& \frac{J}{N}\sum_{\k,\k'\alpha,\beta} \chat^\dagger_{\k\alpha}\boldsymbol{\sigma}_{\alpha\beta} \chat_{\k'\beta}\cdot \hat{\textbf{S}} \label{eq:kondo_interaction}\\
=& \frac{J}{N}\sum_{\k,\k',\alpha,\beta}\left(\chat^\dagger_{\k\alpha}\sigma^x_{\alpha\beta}\chat_{\k'\beta}\hat{S}^x + \chat^\dagger_{\k\alpha}\sigma^y_{\alpha\beta}\chat_{\k'\beta}\hat{S}^y + \chat^\dagger_{\k\alpha}\sigma^z_{\alpha\beta}\chat_{\k'\beta}\hat{S}^z \right)\\
=& \frac{J}{N}\sum_{\k,\k',\alpha,\beta}\left(\chat^\dagger_{\k\alpha}\sigma^x_{\alpha\beta}\chat_{\k'\beta}\hat{S}^x + \chat^\dagger_{\k\alpha}\sigma^y_{\alpha\beta}\chat_{\k'\beta}\hat{S}^y + \chat^\dagger_{\k\alpha}\sigma^z_{\alpha\beta}\chat_{\k'\beta}\hat{S}^z \right)\\
=& \frac{J}{N}\sum_{\k,\k'}\left((\chat^\dagger_{\k\uparrow}\chat_{\k'\downarrow} + \chat^\dagger_{\k\downarrow}\chat_{\k'\uparrow})\hat{S}^x + i(\chat^\dagger_{\k\downarrow}\chat_{\k'\uparrow} - \chat^\dagger_{\k\uparrow}\chat_{\k'\downarrow}) \hat{S}^y + (\chat^\dagger_{\k\uparrow}\chat_{\k'\uparrow} - \chat^\dagger_{\k\downarrow}\chat_{\k'\downarrow})\hat{S}^z\right) \\
=& \frac{J}{N}\sum_{\k,\k'}\left(\chat^\dagger_{\k\uparrow}\chat_{\k'\downarrow}(\hat{S}^x - i\hat{S}^y) + \chat^\dagger_{\k\downarrow}\chat_{\k'\uparrow}(\hat{S}^x + i\hat{S}^y) + (\chat^\dagger_{\k\uparrow}\chat_{\k'\uparrow} - \chat^\dagger_{\k\downarrow}\chat_{\k'\downarrow})\hat{S}^z\right)\\
=& \frac{J}{N}\sum_{\k,\k'}\left(\chat^\dagger_{\k\uparrow}\chat_{\k'\downarrow}\hat{S}^- + \chat^\dagger_{\k\downarrow}\chat_{\k'\uparrow}\hat{S}^+ + (\chat^\dagger_{\k\uparrow}\chat_{\k'\uparrow} - \chat^\dagger_{\k\downarrow}\chat_{\k'\downarrow})\hat{S}^z\right)\\
\end{align}$$

Now we have the interaction Hamiltonian written in a more physically transparent form. We note that electron spin can flip during scattering processes with impurity spin flipping to conserve total spin. This is apparently simple, yet quantum mechanical aspects of the Kondo interaction leads to all its complexities and richness. More specifically, the fact that spin operators (in different directions) don't commute is the root of why there will be a renormalization in the coupling constant. If we were not able to have the spin flip behaviour, we would have a simple potential scattering model (electric monopoles) which doesn't exhibit any interesting RG behaviour. In position space, we can express the interaction term with the fermionic field operators \\(\hat{\psi}^\dagger_\alpha(\r)\\):

$$$$\begin{align}
\Hhat_\text{int} = J\sum_{\alpha\beta}\psi^\dagger_\alpha(0)\boldsymbol{\sigma}_{\alpha\beta}\psi_\beta(0)\cdot\textbf{S}\end{align}$$$$

which describes \\(\delta\\) function scattering. Note that this is equivalent to \eqref{eq:kondo_interaction}; one simply needs to Fourier transform the field operators to show this. Note that actually we need to cut off interaction at large \\(\k\\) and \\(\k'\\), because \\(\delta\\) function scattering potential is not well-defined in \\(d=2\\) or \\(d=3\\). I.e. use finite range model

Or, one can use a tight binding model, 

$$$$\begin{align}
\Hhat = -t\sum_{\left<i,j\right>,\sigma}\chat^\dagger_{i\sigma}\chat_{j\sigma} + J\sum_{\alpha\beta}\chat^\dagger_{0\alpha}\boldsymbol{\sigma}_{\alpha\beta}\chat_{0\beta}\cdot\textbf{S}.
\end{align}$$$$

In the continuum (\\(\k\\) space) model, \\(J\\) has dimensions of energy times volume. Relevant dimensionless parameter is \\(J\nu\\), where \\(\nu\\) is the density of states at the Fermi energy per unit energy, per unit volume, per spin component, in the noninteracting theory. For \\(\epsilon = \frac{\hbar^2 k^2}{2m}\\), the density of states at the Fermi energy is (in 3 dimensions)

$$$$\begin{align}
\nu = \int\delta\left(\frac{\hbar^2 k^2}{2m} - \epsilon_F\right)\frac{d^3\k}{(2\pi)^3} = \frac{mk_F}{2\pi^2} = \frac{k_F^3}{4\pi^2 \epsilon_F}.
\end{align}$$$$

In general, 

$$$$\begin{align}\nu\sim \frac{1}{\epsilon_F - a^3}\end{align}$$$$

Where \\(a\\) is the lattice spacing or electron-electron separation. \\(J\\) in tight binding model is normalized differently - has dimensions of energy


