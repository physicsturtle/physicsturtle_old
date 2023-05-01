---
layout: lesson
title: Fermi Hubbard Model
dept: physics
course: many-body-II
unit: unit10
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 10
---
The Hubbard model for fermions is a model of interacting electrons on a lattice. It consists of two terms. The first is a kinetic energy term, describing the hopping of electrons between nearest neighbour sites on the lattice. The second term is a repulsive Coulomb potential for two electrons on the same lattice site. The extremely short-ranted nature of the Coulomb interaction is quite reasonable in a solid, where Coulomb interactions are already heavily screened, for example in Thomas-Fermi screening. The nearest-neighbour electron hopping is reasonable for materials well-described by the tight-binding model. The Hamiltonian for the model is therefore given by 

$$$$\begin{align}
\Hhat = -t\sum_{\left<i,j\right>,\sigma}(\chat^\dagger_{i\sigma}\chat_{j\sigma} + \hc) + U\sum_i \chat^\dagger_{i\uparrow}\chat^\dagger_{i\downarrow}\chat_{i\downarrow}\chat_{i\uparrow}.
\end{align}$$$$


