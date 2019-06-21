---
layout: lesson
title: Properties of the Fourier Transform
dept: math
course: ode-II
unit: unit5
deptDisplay: Math
courseDisplay: Ordinary Differential Equations II
unitDisplay: Unit 5
---

In the previous section, we introduced the Fourier tranform and how to interpret it. In this section, we introduce some properties of the Fourier transform that allow us to simplify calculations significantly. This will allow us to easily compute Fourier transforms of more complicated functions, as well as pave the way to solving differential equations. 


We recall the definition of the Fourier transform:

$$\mathcal{F}(f)(k) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty e^{-ikx} f(x) dx.$$



<div class="result">
<p> <b>Properties of the Fourier Transform</b> </p>
<p> Let $f(x)$ and $g(x)$ be functions, $\lambda$ any complex scalar, and $f^{(n)}(x) = \frac{d^n f}{dx^n}$ denote the $n$-th derivative of the function $f$. Then the following hold.
  </p>
<ol>
<li>Linearity
  $$\mathcal{F}(f+g) = \mathcal{F}(f) + \mathcal{F}(g)$$</li>  
<li>Scalar Multiplication 
  $$\mathcal{F}(\lambda f) = \lambda\mathcal{F}(f).$$ </li>
<li>Shifting of Argument
  $$\mathcal{F}(f(x-a)) = e^{iak}\mathcal{F}(f) </li>
<li>Fourier Transform of Derivatives:
  $$\mathcal{F}(f^{(n)}) = (-ik)^n\mathcal{F}(f)$$ </li>
<li>Fourier Transform of Powers of $x^n$ times $f$:
  $$\mathcal{F}(x^n f)(k) = \frac{1}{(-1)^n} \frac{d^n}{dk^n}\mathcal{F}(f)(k)$$ </li>
</ol>

</div>

These properties can be shown by direct computation. 

