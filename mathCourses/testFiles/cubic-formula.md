---
layout: page
title: The Cubic Formula
course: test
unit: unit1
permalink: /test/cubic-formula
---

Here, we present a simple solution to the cubic equation. No knowledge of abstract algebra is assumed, but rather only high-school algebra. 

Solving polynomial equations is a very old problem, and it was proven that polynomials of degree five or higher have no formula for their solution. It is well understood how to solve the equation 

$$ax^2+bx+c = 0$$ 

through the quadratic formula

$$x = \frac{-b\pm\sqrt{b^2-4ac}}{2a}.$$

It is possible to derive a formula that solves 

$$ax^3 + bx^2 + cx + d = 0,$$

but this time it is much more involved than completing the square. Here, we will derive the formula that solves general cubic equation. Without loss of generality, we can write the general cubic as 

$$ \begin{equation} \label{eq:generalCubic}
x^3 + Ax^2 + Bx + C = 0
\end{equation} $$

because, assuming that the leading coefficient is nonzero, we can divide through by it to obtain Equation $\eqref{eq:generalCubic}$. The trick to solving this is first getting rid of the $x^2$ term. If we make a shift so that the inflection point moves to zero, then it will help us solve the equation. 

First, defining $f(x) = x^3 + Ax^2 + Bx + C$, we calculate $f^{\prime\prime}(x) = 6x + 2A = 0$, so that the inflection point is found to be at $x = -A/3$. Thus making the change of variables $x = X - A/3$, we can rewrite the equation:

$$X^3 + \left(B - \frac{A^2}{3}\right)X + \left(\frac{2A^2}{27} - \frac{BA}{3} + C\right) = 0$$

Now, we define new coefficients so that we can rewrite it simply as 

$$X^3 + bX + c = 0.$$

Now, taking a detour we consider the equation 

$$\xi^3 = 3\alpha\xi + 2\beta.$$

If $\xi = s + t$, for some values of $s$ and $t$, then we transform the equation into 

$$s^3 + 3s^2t + 3st^2 + t^3 = 3\alpha(s+t) + 2\beta$$

If we can find $s$ and $t$ such that $s^3 + t^3 = 2\beta$ and $3s^2t + 3st^2 = 3\alpha(t+s)$, or, equivalently $st = \alpha$, then our job is done. If we solve this system of two equations 

$$\begin{cases}
s^3 + t^3 = 2\beta \\
st = \alpha
\end{cases}$$

then we get that 

$$t^3 = \beta\pm\sqrt{\beta^2 - \alpha^3}, \qquad s^3 = \beta \mp \sqrt{\beta^2 - \alpha^3}$$

which gives us a solution

$$\xi = \sqrt[3]{\beta + \sqrt{\beta^2 - \alpha^3}} + \sqrt[3]{\beta - \sqrt{\beta^2 - \alpha^3}}$$

Since this is a cubic equation and we have found one root, if we factor out this expression then we will be left with a quadratic, which we already know how to solve. It is up to the reader to show that performing a polynomial long division of $\xi^3 - 3\alpha\xi -2\beta$ by $(\xi - \xi_1)$, we get 

$$\frac{\xi^3 - 3\alpha\xi -2\beta}{\xi -\xi_1} = \xi^2 + \xi_1 \xi - 3\alpha + \xi_1^2$$

where the remainder term has been set to zero because we already know that $\xi_1$ is a root. The resulting is easy to solve in terms of $\alpha$ and $\beta$ by using the quadratic formula:

$$\xi_2 = \frac{-\xi_1 + \sqrt{3}\sqrt{4\alpha-\xi_1^2}}{2},\quad \xi_3 =  \frac{-\xi_1 - \sqrt{3}\sqrt{4\alpha - \xi_1^2}}{2}$$



