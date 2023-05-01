---
layout: lesson
title: Review of Coherent States
dept: physics
course: many-body-II
unit: unit2
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 2
---
In single-particle quantum mechanics, a coherent state is a particular state of a quantum harmonic oscillator which has the dynamics most closely resembling the oscillatory behaviour of a classical harmonic oscillator. We will later come to constructing the ``coherent state path integral". Although the intuition associated with this path integral does not have much to do with coherent states of the quantum harmonic oscillator, it is nonetheless helpful to review the ordinary coherent states purely for the relevant mathematical manipulations.

We recall that the Hamiltonian for the quantum harmonic oscillator is given by 

$$\Hhat = \hbar\omega\left(\ahat^\dagger\ahat + \frac{1}{2}\right)$$

and that the relation between the position and momentum operators and the creation/annihilation operators are simply 

$$\ahat = \frac{1}{\sqrt{2\hbar m\omega}}(i\phat + m\omega\xhat) ,\quad \ahat^\dagger = \frac{1}{\sqrt{2\hbar m\omega}}(-i\phat + m\omega\xhat)$$

A coherent state is an eigenstate of the annihilation operator, with an eigenvalue \\(\alpha\\), so

$$\ahat\ket{\alpha} = \alpha\ket{\alpha}$$

The wave function and its time evolution, which we want to solve for, are given by 

$$\bra{x}\ket{\alpha} = \psi_\alpha(x),\quad \bra{x}e^{-i\Hhat t/\hbar} \ket{\alpha} = \psi_\alpha(x,t)$$

The goal will be to show that the expectation values of the position and momentum operators in this state will yield the same time evolution as the actual position and momentum of a classical harmonic oscillator. 



Both bosonic and fermionic path integrals are based on inserting complete sets of states, 

$$$$\begin{align}
I = \sum_{n=0}^\infty \ket{n}\bra{n}
\end{align}$$$$

many times, that is 

$$\begin{align}
e^{iHt} =& (e^{iH\Delta t})^N \\
=& e^{iH\Delta t}\sum_{n_1}\ket{n_1}\bra{n_1}e^{iH\Delta t}\sum_{n_2}\ket{n_2}\bra{n_2}\dots e^{i\Hhat\Delta t} \sum_{n_{N-1}}\ket{n_{N-1}}\bra{n_{N-1}} e^{-iH\Delta t} 
\end{align}$$

We need to find a convenient representation for this. Consider a single harmonic oscillator, whose creation operator is \\(a^\dagger\\). Then, the \\(n\\)th eigenstate of the oscillator is given by

$$$$\begin{align}
\ket{n} = \frac{(a^\dagger)^n}{\sqrt{n!}}\ket{0},
\end{align}$$$$

where the \\(1/\sqrt{n!}\\) is the normalization factor. 


