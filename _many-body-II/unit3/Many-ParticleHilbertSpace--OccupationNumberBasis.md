---
layout: lesson
title: Many-Particle Hilbert Space -- Occupation Number Basis
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
In many courses on advanced quantum mechanics, one is introduced to the many-particle Hilbert space, also known as the Fock space, by the following construction. First, the single-particle Hilbert space is considered. Then, antisymmetrized tensor products between Hilbert spaces are defined: \\(\mathcal{H}^{\wedge n} = \mathcal{H}\wedge \cdots \wedge\mathcal{H}\\). Lastly, the direct sum is taken between these different number particle sectors: 

$$$$\begin{align}
\mathcal{F} = \bigoplus_{n=0}^N \mathcal{H}^{\wedge n}.
\end{align}$$$$

This constitutes the fermionic Fock space. This construction makes clear how to construct a basis for the Fock space out of different \\(n\\)-particle bases. This is to be contrasted with the approach we take here, which will apply a completely different basis. Here, we take into account the fact that each single-particle state can only be occupied or unoccupied. If there are \\(N\\) possible single-particle states, then we can instead write the Fock space as 

$$$$\begin{align}
\mathcal{F} = (\chat^2)^{\otimes N}.
\end{align}$$$$

The advantage of this construction is that antisymmetrized states are no longer necessary. Furthermore, it allows us to construct the Fock space out of a simple and well-understood Hilbert space: \\(\chat^2\\). This construction also goes by the name of ``occupation number basis". 

We will, of course, want to generalize fermionic coherent states to a Hilbert space with many creation/annihilation operators \\(\chat_{\k\sigma}\\); now each 2-dimensional Hilbert space is labelled by a \\(\k\\) and \\(\sigma\\). Let's keep the indices more abstract, and now consider operators \\(\hat{\psi}_i\\) and \\(\hat{\psi}_i^\dagger\\), where \\(i\\) is an index denoting a site in some lattice. The anticommutation relation between operators on (possibly) different sites is

$$$$\begin{align}
\{\hat{\psi}_i,\hat{\psi}^\dagger_j\} = \delta_{ij}.
\end{align}$$$$

We introduce a pair of Grassmann numbers \\(\psi_i\\), and \\(\bar{\psi}_i\\) for each \\(\hat{\psi}_i\\) and \\(\hat{\psi}^\dagger_i\\) pair of operators. These obey

$$$$\begin{align}\{\psi_i,\bar{\psi}_j\} = 0 = \{\psi_i,\psi_j\} = \{\bar{\psi}_i,\bar{\psi}_j\}.\end{align}$$$$

Now that we have defined Grassmann numberes for 

 Coherent states: e.g. for 2 fermion operators

$$$$\begin{align}\ket{\psi_1,\psi_2} = (1-\psi_1\hat{\psi}_1^\dagger)(1-\psi_2\hat{\psi}_2^\dagger)\ket{0}\end{align}$$$$

Note: 1 - 2 order doesn't matter, but note \\(\psi\hat{\psi}^\dagger\\) order. Integral table follows from

$$$$\begin{align}\int 1 \d\psi_1 = 0,\qquad \int \psi_1 \d\psi_1 = 1\end{align}$$$$

We now extend our formulas for the resolution of identity and trace to this new Hilbert space. Suppose we had 


