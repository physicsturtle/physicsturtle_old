---
layout: page
title: Coulomb Wavefunction
course: test
unit: unit1
permalink: /test2/
---

Coulomb Wavefunctions are solutions to the hydrogenic system for positive energies. That is, unbound states of the hydrogenic system. Calculating these functions requires some heavy analysis, namely tools from contour integration. The differential equation that this leads to is (in atomic units)

$$-\frac{1}{2}\nabla^2\psi + \frac{Z}{r}\psi = E\psi$$

After separating variables, this leads to 

$$-\frac{1}{2}\frac{d^2}{dr^2}\psi + \frac{Z}{r}\psi + \frac{l(l+1)}{2r^2}\psi = E\psi.$$

The solutions to the Schrödinger equation have already been calculated for this, but for negative energies. It is possible to use these solutions as a template and from them build the solutions for positive energies. It will require us to do a new normalization, but it is better than trying to solve the differential equation from scratch again. 

The main difference between the solutions for positive energy and the solutions for negative energy is that the solutions for positive energy require an imaginary principal quantum number. Before, we had the formula (in atomic units)

$$E = -\frac{Z}{2n^2}$$

Now, for positive energies, we think of this as a continuous spectrum of possible states, and define 

$$E = \frac{k^2}{2}$$

which means that \\(n = i\sqrt{Z}k\\). 

The solution to the hydrogenic equation is as follows: 

$$\psi_{nlm} = \sqrt{\left(\frac{2Z}{n_1a}\right)^3\frac{(n_1-l_1-1)!}{2n((n_1+l_1)!)^3}}\exp\left(-\frac{Zr}{n_1 a}\right)\left(\frac{2rZ}{n_1a}\right)^{l_1}L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right)Y^{m_1}_{l_1}(\theta,\varphi).$$

We ditch the normalization factor, and focus only on the variable part. In order to adapt this solution, we need to extend the definition of the Laguerre polynomials to the case of complex indices. The Laguerre polynomials are defined as

$$ L_q(x) = e^x\left(\frac{d}{dx}\right)^q\left(e^{-x} x^q\right) $$

The \\(n\\)-fold differentiation of a product has various formulas for expressing it in a closed form. Recall the Cauchy integral formula:

\begin{equation}
f(z) = \frac{1}{2\pi i}\oint \frac{f(s)}{s-z} ds
\end{equation}

where the integral is taken counterclcockwise over a simple closed curve, \\(f\\) is holomorphic in an open set which fully contains the curve, and \\(z\\) is a point inside the closed curve. Then we can differentiate the formula \\(n\\) times with respect to \\(z\\).

$$ f^{(n)}(z) = \frac{\Gamma(n+1)}{2\pi i}\oint \frac{f(s)}{(s-z)^{n+1}} ds $$

Thus we can express the \\(q\\)th Laguerre polynomial as 

$$L_q(x) = \frac{e^x \Gamma(q+1)}{2\pi i}\oint \frac{e^{-z} z^q}{(z-x)^{q+1}} dz $$

It is important that we keep track of the curve over which we integrate. In the above integral, this contour is still the one enclosing the point \\(x\\).  Then we make the substitution \\(y = z-x\\), so the contour becomes the counterclockwise one enclosing the origin.

$$ L_q(x) = \frac{\Gamma(q+1)}{2\pi i}\oint \frac{e^{-y}(x+y)^q}{y^{q+1}} dy $$

The associated Laguerre polynomials are define in terms of the Laguerre polynomials like so:

$$ L^p_{q-p}(x) = (-1)^p\left(\frac{d}{dx}\right)^p L_q(x) $$

We can plug in the Laguerre polynomials into the formula for the associated Laguerre polynomials. Differentiating the formula \\(p\\) times now gives us

$$ L^p_{q-p}(x) = (-1)^p \frac{(\Gamma(q+1))^2}{2\pi i \Gamma(q-p+1)}\oint \frac{e^{-y}(x+y)^{q-p}}{y^{q+1}} dy  $$






