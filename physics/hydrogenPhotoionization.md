---
layout: page
title: Hydrogen Photoionization
course: test
unit: unit1
permalink: /test/
---

Photoionization is the problem where an electron in a bound state of an atom is released to an unbound state via some bath of radiation in which it sits. 

Eventually, this leads to integrals of the form 

$$\left<\psi_f\right|\textbf{r}\left|\psi_i\right>$$

with \\(\psi_i\\) and \\(\psi_f\\) denoting the initial and final states respectively. The initial states are the bound hydrogen states; we will use hydrogenic ones for generality. 

$$\psi_i = \sqrt{\left(\frac{2Z}{n_1a}\right)^3\frac{(n_1-l_1-1)!}{2n((n_1+l_1)!)^3}}\exp\left(-\frac{Zr}{n_1 a}\right)\left(\frac{2rZ}{n_1a}\right)^{l_1}L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right)Y^{m_1}_{l_1}(\theta,\varphi)$$

The unbound wave-function is the coulomb wave-function. (show a derivation for this in another section)

$$\psi_f = \frac{(-1)^{l_2}2\sqrt{Z}}{\sqrt{1-e^{-2\pi n'}}}\left(\prod_{s=1}^{l_2}\sqrt{s^2+(n')^2}\right)\frac{Y^{m_2}_{l_2}(\theta,\varphi)}{2\pi(2kr)^{l_2+1}}\oint e^{2ikr\xi}\left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} d\xi $$

The next step is to calculate the inner product. This will be a very lengthy integral, so let's do each part separately. Since we can write \\(\textbf{r} = r\left(\sin\theta\cos\varphi \hat{\textbf{x}} + \sin\theta\sin\varphi \hat{\textbf{y}} + \cos\theta\hat{\textbf{z}}\right)\\), this factor of \\(r\\) can be separated out. This leaves us with three separate components:

The constant:

$$A = \sqrt{\left(\frac{2Z}{n_1a}\right)^3\frac{(n_1-l_1-1)!}{2n((n_1+l_1)!)^3}}\frac{(-1)^{l_2}2\sqrt{Z}}{2\pi\sqrt{1-e^{-2\pi n'}}}\left(\prod_{s=1}^{l_2}\sqrt{s^2+(n')^2}\right)$$

The radial integral:

$$R = \int_0^\infty \exp\left(-\frac{Zr}{n_1 a}\right)\left(\frac{2rZ}{n_1a}\right)^{l_1}L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right) \frac{r}{(2kr)^{l_1+1}} \oint e^{2ikr\xi}\left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} d\xi r^2 dr$$

The angular integrals:

$$\int_0^{2\pi}\int_0^\pi Y^{m_1}_{l_1}(\theta,\varphi)^* \left(\sin\theta\cos\varphi \hat{\textbf{x}} + \sin\theta\sin\varphi \hat{\textbf{y}} + \cos\theta\hat{\textbf{z}}\right) Y^{m_2}_{l_2}(\theta,\varphi) d\theta d\varphi$$

### The Radial Integral

We now evaluate the radial integral. 

$$\begin{eqnarray}
R &=& \int_0^\infty \exp\left(-\frac{Zr}{n_1 a}\right)\left(\frac{2rZ}{n_1a}\right)^{l_1}L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right) \frac{r}{(2kr)^{l_1+1}} \oint e^{2ikr\xi}\left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} d\xi r^2 dr \\
&=& \left(\frac{2Z}{n_1a}\right)^{l_1}\frac{1}{(2k)^{l_1+1}}\int_0^\infty \oint\exp\left(-\frac{Zr}{n_1 a} + 2ikr\xi\right)L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right) \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} d\xi r^2 dr \\
&=& \left(\frac{2Z}{n_1a}\right)^{l_1}\frac{1}{(2k)^{l_1+1}} \oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} \int_0^\infty \exp\left( 2ikr\xi -\frac{Zr}{n_1 a}\right)L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right)  r^2 dr d\xi \\
\end{eqnarray}
$$

At this point, we have simplified some terms and swapped the order of integration. Now let's change the integration variable:

$$\frac{2Zr}{n_1a} = u$$

Thus the integral becomes

$$\begin{eqnarray}
R &=& \left(\frac{2Z}{n_1a}\right)^{l_1-3}\frac{1}{(2k)^{l_1+1}} \oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} \int_0^\infty \exp\left(\underbrace{\left(\frac{ik\xi n_1 a}{Z} - \frac{1}{2}\right)}_{\beta}u\right)L^{2l_1+1}_{n_1-l_1+1}(u)  u^2 du d\xi \\
&=& \left(\frac{2Z}{n_1a}\right)^{l_1-3}\frac{1}{(2k)^{l_1+1}} \oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} \int_0^\infty e^{\beta u}L^{2l_1+1}_{n_1-l_1+1}(u)  u^2 du d\xi \\
\end{eqnarray}
$$

The integral in \\(u\\) can be evaluated to 

$$\int_0^\infty u^q e^{\beta u} L^\alpha_n(u) du = \sum_{k=1}^n\frac{(-1)^k}{k!(n-k)!}\frac{\Gamma(n+\alpha+1)}{\Gamma(k+\alpha+1)}\frac{(q+k)!}{\beta^{q+k+1}}$$

(add proof here, optional)




