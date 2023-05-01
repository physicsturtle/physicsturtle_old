---
layout: lesson
title: The Fermi-Hubbard Model: Electron-Electron Interactions
dept: physics
course: many-body-II
unit: unit9
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 9
---
In this section, we will develop the perturbation series for electron-electron interactions. We will do this in the context of the Hubbard model. It is also possible to do this exercise for the jellium model, but this will be left as a student project. The Hamiltonian we consider is 

$$H = -t\sum_{\left<i,j\right>,\sigma} \chat^\dagger_{i\sigma} \chat_{j\sigma} + U\sum_i \nhat_{i\uparrow} \nhat_{i\downarrow} $$

which means that the effective action is given by 

$$S = \int_0^\beta \left(\sum_{\k\sigma} \bar{c}_{\k\tau \sigma}(\partial_\tau + \xi_{\k}) c_{\k\tau \sigma} + U\sum_i \bar{c}_{i\uparrow} \bar{c}_{i\downarrow} c_{i\downarrow} c_{i\uparrow} \right)\d\tau$$

where \\(\xi_{\k} = \epsilon_{\k} - \mu\\). We define the interacting part of the action as 

$$S_\text{int} = U\int_0^\beta \sum_i \bar{c}_{i\tau\uparrow} \bar{c}_{i\tau\downarrow} c_{i\tau\downarrow} c_{i\tau\uparrow} \d\tau $$

We consider the interacting Green function

$$\mathcal{G}(k,ik_0) = \left<\bar{c}_{k\sigma} c_{k\sigma} \right>$$

where we note that the incoming and outgoing momenta and Matsubara frequency of the electron must be the same. To evaluate this, we rewrite it in terms of correlation functions with respect to the free Hamiltonian: 

$$\mathcal{G}(\k,ik_0) = \frac{\left< e^{-S_\text{int}} \bar{c}_{k\sigma} c_{k\sigma} \right>_0}{\left<e^{-S_\text{int}}\right>_0}$$

By the linked cluster theorem, this quantity is given by the sum of all connected diagrams. To start to see how this works, we rewrite this as 

$$\mathcal{G}(\k,ik_0) = \sum_{n=0}^\infty \frac{(-1)^n}{n!}\left<S^n_\text{int} \bar{c}_{k\sigma} c_{k\sigma} \right>_{0,\text{conn}}$$

Now, we start to write out powers of the interaction. To do this, it is useful to rewrite the interaction as 

$$\begin{align}
S_\text{int} =& U\int_0^\beta \sum_i \bar{c}_{i\uparrow} \bar{c}_{i\downarrow} c_{i\downarrow} c_{i\uparrow} \d\tau \\
=& \frac{U}{(\beta N_s)^2} \int_0^\beta \sum_i \sum_{kk'pp'} \bar{c}_{k'\uparrow} \bar{c}_{k\downarrow} c_{p'\downarrow} c_{p\uparrow} e^{i(\p+\p'-\k-\k')\cdot\textbf{R}_i} e^{-i(p_0+p_0'-k_0-k_0')\tau} \d\tau \\
=& \frac{U}{\beta N_s} \sum_{kk'pp'} \bar{c}_{k\uparrow} \bar{c}_{k'\downarrow} c_{p'\downarrow} c_{p\uparrow} \delta_{\p+\p',\k+\k'} \delta_{p_0+p_0',k_0+k_0'} \\
=& \frac{U}{\beta N_s} \sum_{k'pp'} \bar{c}_{p+p'-k',\uparrow} \bar{c}_{k'\downarrow} c_{p'\downarrow} c_{p\uparrow}
\end{align}$$

We then define \\(p'-k' = q\\), and then sum over \\(q\\): 

$$\begin{align}
S_\text{int} =& \frac{U}{\beta N_s} \sum_{qpp'} \bar{c}_{p+q,\uparrow} \bar{c}_{p'-q,\downarrow} c_{p'\downarrow} c_{p\uparrow}
\end{align}$$

and then relabel the variables a little bit to get 

$$\begin{align}
S_\text{int} =& \frac{U}{\beta N_s} \sum_{kpq} \bar{c}_{k+q,\uparrow} \bar{c}_{p-q,\downarrow} c_{p\downarrow} c_{k\uparrow}
\end{align}$$

\underline{Zeroth Order \\(O(1)\\)}

$$\mathcal{G}(\k,ik_0) = \left<\bar{c}_{k\sigma} c_{k\sigma}\right>_0$$

\underline{First Order \\(O(U):\\)}

$$\begin{align}
\mathcal{G}(\k,ik_0) =& -\frac{U}{\beta N_s}\sum_{k_1p_1q_1} \left<\bar{c}_{k_1+q_1,\uparrow} \bar{c}_{p_1-q_1,\downarrow} c_{p_1\downarrow} c_{k_1\uparrow} \bar{c}_{k\sigma} c_{k\sigma} \right>_0 \\
=& -\frac{U}{\beta N_s}\sum_{k_1p_1q_1} \left(\left<\wick{ \c1{\bar{c}}_{k_1+q_1,\uparrow} \c2{\bar{c}}_{p_1-q_1,\downarrow} \c2{c}_{p_1\downarrow} \c1{c}_{k_1\uparrow} \bar{c}_{k\sigma} c_{k\sigma} }\right>_0 +  \left<\bar{c}_{k_1+q_1,\uparrow} \bar{c}_{p_1-q_1,\downarrow} c_{p_1\downarrow} c_{k_1\uparrow} \bar{c}_{k\sigma} c_{k\sigma} \right>_0\right) \\
\end{align}$$


<ol>
\question
\end{questions}


\section{Fermi Hubbard Model}
The Hubbard model for fermions is a model of interacting electrons on a lattice. It consists of two terms. The first is a kinetic energy term, describing the hopping of electrons between nearest neighbour sites on the lattice. The second term is a repulsive Coulomb potential for two electrons on the same lattice site. The extremely short-ranted nature of the Coulomb interaction is quite reasonable in a solid, where Coulomb interactions are already heavily screened, for example in Thomas-Fermi screening. The nearest-neighbour electron hopping is reasonable for materials well-described by the tight-binding model. The Hamiltonian for the model is therefore given by 

$$$$\begin{align}
\Hhat = -t\sum_{\left<i,j\right>,\sigma}(\chat^\dagger_{i\sigma}\chat_{j\sigma} + \hc) + U\sum_i \chat^\dagger_{i\uparrow}\chat^\dagger_{i\downarrow}\chat_{i\downarrow}\chat_{i\uparrow}.
\end{align}$$$$


