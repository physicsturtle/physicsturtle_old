---
layout: lesson
title: Interacting Fermions in 1 Dimension
dept: physics
course: many-body-II
unit: unit16
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 16
---
Now, we will study interacting fermions in 1 dimension. Although this may seem not useful in realistic physical scenarios, this is not true. Experimental applications include the study of carbon nanotubes, metallic nanowires, gated semiconductor nano-wires, nanowire self assembled on metallic surfaces, organic conductors, and quasi 1D magnetic insulators (by Jordan Wigner transformation). 

We start with the simplest case: a single band of spinless fermions with short-ranged (screened) Coulomb interactions. This is useful because the renormalization group is much simpler in 1D than in 2D or 3D. The results are also more interesting because the behaviour is more exotic; a non-Fermi liquid phase results. Note that we will start with a lattice model. This is because condensed matter physicists are typically more comfortable with lattice models. We will also perform the thermodynamic limit in some detail, which we perform because it is easier to do the field theory in this limit.

%We will follow treatment in Shankar Chapter 4 quite closely - please read!

We will apply RG and focus on universal low energy properties. These properties are largely independent of the microscopic model, but for concreteness we will consider a tight-binding model with a 1D nearest neighbour Hubbard interaction between nearest neighbours. This is in contrast to the study of the Kondo model, where the interaction is ``zero dimensional". We have now graduated to \\(d = 1\\). 

$$$$\begin{align}
H = \sum_j\left[-t(\chat^\dagger_j\chat_{j+1} + \hc) + U\hat{n}_j\hat{n}_{j+1}\right]
\end{align}$$$$

where \\(\hat{n}_j = \chat^\dagger_j \chat_j\\). Note that \\(\chat_j\\) is unitless, and both \\(t,U\\) have units of energy. The nearest neighbour interaction \\(U\\) is the shortest-ranged possible for spinless fermions because on-site interactions are prohibited by the Pauli principle. 

