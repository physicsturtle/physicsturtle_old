---
layout: page
title: Introduction
course: test
unit: unit1
permalink: /test/born-approximation/
---

In this section, we will discuss another approximation for scattering problems, known as the Born approximation. Consider the time independent Schrödinger equation
$$-\frac{\hbar^2}{2m}\nabla^2\psi + V\psi = E\psi$$
Rearranging this, we get 
$$\nabla^2\psi(\textbf{x}) + k^2\psi(\textbf{x}) = f(\textbf{x}),$$
where $k^2 = 2mE/\hbar^2$ and $f(\textbf{x}) = 2mV\psi/\hbar^2$. We know that the Green's function $G = -\frac{e^{-ikr}}{4\pi r}$ for the Helmholtz equation satisfies 

$$(\nabla^{\prime 2} + k^2)G(\textbf{x}',\textbf{x}) = \delta(\textbf{x} - \textbf{x}').$$

If we multiply the above equation with $\psi$ and then integrate over all space, we get 

$$\int_{\mathbb{R}^3}\psi(\textbf{x}')(\nabla^{\prime 2} + k^2)G(\textbf{x}',\textbf{x}) d^3\textbf{x} = \int_{\mathbb{R}^3} \psi(\textbf{x}')\delta(\textbf{x}'-\textbf{x})$$

If we apply Green's second identity of the left hand side and simplify the right hand side, we get 

$$\int_{\mathbb{R}^3} G(\textbf{x}',\textbf{x})(\nabla^{\prime 2} + k^2)\psi(\textbf{x}')d^3\textbf{x} = \psi(\textbf{x})$$

If we plug in the Green's function as well as the function $f(\textbf{x})$, then we get 

$$\psi(\textbf{x}) = -\int_{\mathbb{R}^3} \frac{e^{-ik|\textbf{x}'-\textbf{x}|}}{4\pi|\textbf{x}'-\textbf{x}|}\frac{2mV(\textbf{x}')\psi(\textbf{x}')}{\hbar^2} d^3\textbf{x}'$$



