---
layout: lesson
dept: physics
title: The Euler-Lagrange Equation
course: cm-III
unit: unit1
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 1
---

In this lesson, we will derive the Euler-Lagrange equation for the simplest problem in the calculus of variations. The problem is to minimize the integral

$$S[y] = \int_a^b \mathcal{L}(x,y,y') dx $$

over functions $y$. To do this, we assume that we have found a function $y_/*$ which minimizes the integral. Then, we consider a general function $y = y_\* + \epsilon\eta$, where $\eta$ is a any function satisfying $\eta(a) = \eta(b) = 0$. Thus, $\epsilon\eta$ is a small perturbing funciton. We note that for $\epsilon = 0$, $y$ becomes the minimizer of the integral. This means that 

$$\frac{d}{d\epsilon} S[y]\bigg|_{\epsilon = 0} = 0.$$

Armed with this condition, we compute the derivative of $S$ with respect to $\epsilon$. 

$$\begin{eqnarray*}
\frac{d}{d\epsilon}S[y] &=& \frac{d}{d\epsilon} \int_a^b \mathcal{L}(x,y,y') dx\\
&=& \int_a^b\left(\frac{\partial\mathcal{L}}{\partial y}\frac{dy}{d\epsilon} + \frac{\partial\mathcal{L}}{\partial y'} \frac{dy'}{d\epsilon}\right) dx \\
&=& \int_a^b\left(\frac{\partial\mathcal{L}}{\partial y}\eta + \frac{\partial\mathcal{L}}{\partial y'} \eta' \right) dx \\
&=&  \int_a^b\left(\frac{\partial\mathcal{L}}{\partial y}\eta \right) dx +  \int_a^b\left(\frac{\partial\mathcal{L}}{\partial y'} \eta' \right) dx \\
&=&  \int_a^b\left(\frac{\partial\mathcal{L}}{\partial y}\eta \right) dx +  \left(\frac{\partial\mathcal{L}}{\partial y'} \eta\right)\bigg|_a^b - \int_a^b \frac{d}{dx}\left(\frac{\partial\mathcal{L}}{\partial y'} \right)\eta dx \\
&=&  \int_a^b\left[\frac{\partial\mathcal{L}}{\partial y}- \frac{d}{dx}\left(\frac{\partial\mathcal{L}}{\partial y'} \right)\right]\eta dx 
\\
&=& 0
\end{eqnarray*}$$

Since this quantity is 0 for all $\eta$, we conclude that the object multiplying it is zero, or, 

$$\frac{\partial\mathcal{L}}{\partial y}- \frac{d}{dx}\left(\frac{\partial\mathcal{L}}{\partial y'}\right)  = 0$$

This is known as the Euler-Lagrange equation. 
