---
layout: page
title: Symmetries
course: quantum-mechanics-II
unit: unit1
---

Symmetries are very important in quantum mechanics. For this, we need to clear definitions. 

**Definition** A symmetry of a quantum system is a unitary operator. 

Let's look at the translation operator, defined by \\((\hat{T}_a\psi)(x) = \psi(x-a)\\)

First, let's show that this is a symmetry. To show that something is a symmetry, we need to find its adjoint and show that it is equal to its inverse. In order to do this, we can calculate
$$\begin{eqnarray}
\langle \psi |\left( \hat{T}_a |\phi\rangle\right) &=& \int\psi^*(x) (T_a\phi)(x) dx \\
&=& \int\psi^*(x)\phi(x-a) dx \\
&=& \int\psi^*(x+a)\phi(x) dx\\
&=& \int \psi(x+a)^*\phi(x)dx\\
&=& \int (\hat{T}_{-a}\psi)(x)\phi(x)dx\\
&=& \left(\langle\psi|\hat{T}_{-a}\right)|\phi\rangle
\end{eqnarray}$$

Thus the translation operator is unitary. Now we are interested in finding its associated hermitian operator, because to every symmetry corresponds a convserved quantity, which is expressed through a hermitian operator. We can taylor expand the translation operator as follows. 


In general, we expand a unitary operator as \\(\hat{T}_\epsilon = 1 + i\epsilon\hat{A}\\). This can be matched with a taylor series in a normal variable, \\((T_\epsilon \psi)(x) = \psi(x-\epsilon) = \psi(x) - \epsilon\psi'(x)\\). Then comparing this with \\(\hat{T}_\epsilon\psi)(x) = (1-i\epsilon\hat{A})(\psi)(x) = \psi(x) - i\epsilon(\hat{A}\psi)(x)\\), we find that \\(\hat{A}(\psi)(x) = -i\\psi'(x)\\). This means that \\(\hat{A} = -i\frac{d}{dx}\\), which is the momentum operator. 

