---
layout: lesson
title: Grassman Numbers
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
In this section, we will introduce the mathematics of so-called Grassmann numbers, which allow us to define the eigenvalues and eigenstates of fermionic creation and annihilation operators. A single fermionic oscillator is the Hilbert space upon which the fermionic creation/annihilation operators, \\(\hat{\psi}\\), \\(\hat{\psi}^\dagger\\), act. Watch carefully in this section for the distinction between \\(\hat{\psi}\\) and \\(\bar{\psi}\\). As always, \\(\hat{\psi}\\) denotes a fermionic annihilation operator, and now \\(\psi\\) denotes a Grassmann number, which we will introduce now.

\begin{definition_wrapper}
\begin{definition}
The Grassmann numbers \\(\psi\\) and \\(\bar{\psi}\\) are numbers obeying the following anticommutation relations: 
$$$$\begin{align}
\{\psi,\bar{\psi}\} = \{\psi,\psi\} = \{\bar{\psi},\bar{\psi}\} = 0.
\end{align}$$$$

They also obey the following anticommutation and commutation relations with fermionic operators, bosonic operators, and complex numbers. 
\end{definition}
\end{definition_wrapper}


These anticommutation relations imply that \\(\psi^2 = \bar{\psi}^2 = 0\\). Additionally, this implies that the series

$$$$\begin{align}
\sum_{n=0}^\infty \ket{n}\bra{n}
\end{align}$$$$

terminates at \\(n=1\\). This makes sense because, for fermions, we cannot have an occupation number other than 0 or 1. Note that this is different than the creation and annihilation \textit{operators} which obey \\(\{\hat{\psi},\hat{\psi}^\dagger\} = 1\\). A fermionic coherent state is not labelled by a complex number \\(z\\) as in the bosonic case, but instead by Grassmann numbers \\(\psi\\) and \\(\bar{\psi}\\).

\begin{remark_wrapper}
\begin{remark}
Grassmann numbers, although defined here in a very imprecise way, do have a rigorous mathematical foundation. Rigorously, a Grassmann number is an element of the exterior algebra over the complex numbers \\(\chat\\). We recall that the exterior algebra over a vector space \\(V\\) (in our case the vector space \\(V\\) is simply \\(\chat\\) over the field \\(\chat\\)) is .... FINISH THIS LATER
\end{remark}
\end{remark_wrapper}

The Grassmann numbers are defined to anticommute with fermionic operators, \\(\{\psi,\hat{\psi}\} = \{\psi,\hat{\psi}^\dagger\} = 0\\), etc. and to commute with bosonic operators. They also commute with the ground state (ground state or vacuum?) \\(\psi\ket{0} = \ket{0}\psi\\). 

We also define integrals over Grassmann numbers as 

$$$$\begin{align}
\int 1\d\psi := 0,\qquad \int \psi  \d\psi := 1 =  -\int \d\psi \psi.
\end{align}$$$$

Note that this convention is sometimes reversed in other sources. This doesn't actually matter for any computations of physical observables, as long as one is consistent! This is a complete integral table since \\(\psi^n = 0\\) for \\(n\geq 2\\), and every function \\(f\\) of \\(\psi\\) is defined by Taylor expanding \\(f(\psi) = f(0) + f'(0)\psi\\). 

Differentiation proceeds identically, as

$$$$\begin{align}
\frac{\d}{\d\psi} 1 = 0,\qquad \frac{\d}{\d\psi} \psi = 1.
\end{align}$$$$


