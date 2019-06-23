---
layout: lesson
title: Solving ODEs with Fourier Transform
dept: math
course: ode-II
unit: unit5
deptDisplay: Math
courseDisplay: Ordinary Differential Equations II
unitDisplay: Unit 5
---

It is possible to solve ODEs with the Fourier transform by finding integral representation for their solution. Many of these integrals cannot be evaluated as elementary functions, but integral representations are useful for other things. For example, one can derive asymptotic formulas for certain special functions, which may be difficult with only a Taylor series representation. We will start by recalling the following useful formula:

$$\mathcal{F}(x^n y^{(m)})(k) = \frac{1}{(-i)^n}\frac{d^n}{dk^n}\left((-ik)^m\mathcal{F}(y)\right)$$

This formula allows us to calculate the Fourier transforms of many types of differential equations. It does of course require that we look for solutions which decay sufficiently rapidly at infinity. 

<div class="example">
<p><b>Example:</b> Solve the Airy differential equation $y''  = xy$ by using the Fourier transform. </p>
This example will illustrate the method nicely. Taking the Fourier transform of both sides yields
$$-k^2\hat{y} = \frac{1}{-i}\hat{y}'.$$
What we have done is transformed a second order ODE into a first order ODE! We can thus solve this first order ODE for $\hat{y}$, the Fourier transform of $y$. We rewrite the ODE as 
$$\frac{\hat{y}'}{\hat{y}} = ik^2,$$
which gives the following function for $\hat{y}$:
$$\hat{y} = e^{ik^3/3}.$$
Thus a solution to the original differential equation is 
$$y(x) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty e^{ik^3/3 + ikx} dk$$
</div>

