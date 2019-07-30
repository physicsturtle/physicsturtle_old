---
layout: exercises
title: Derivatives of Polynomials - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

### Exercises

\question[$*$] Differentiate the following function. $y = 2x^{1/2} + 6x^{1/3} - 2x^{3/2}$\\

\begin{solution}[30 mm]
Applying the power rule, \[y' = \frac{1}{\sqrt{ x}} + \frac{2}{x^{2/3}} - 3 \sqrt{x}\]
\end{solution}

\question[$*$] Differentiate the following function. $ \displaystyle{k(x) = \pi^2x + e^{x + e} - \frac{1}{\pi}}$\\

\begin{solution}[30 mm]
\[y' = \pi^2 + e^ee^x\]
\end{solution}

\question[$*$] Differentiate the following function. $\displaystyle{f(x) = \frac{x^3 - 5x^2 + 2x - 9}{x^2}}$\\

\begin{solution}[40 mm]
Simplifying, $\displaystyle{f(x) = x - 5 + \frac{2}{x} - \frac{9}{x^2}}$\\
Applying the power rule yields, \[y' = 1 - \frac{2}{x^2} + \frac{18}{x^3}\]
\end{solution}

\question[$**$] Show that on the graph of any quadratic polynomial the chord joining the points for which $x = a$ and $x = b$ is parallel to the tangent line at the midpoint $x = (a+b)/2$.

\begin{solution}[100mm]
To show that this is true for any quadratic function, first we create a general quadratic\\ polynomial function $f(x)=Ax^2+Bx+C$. \\
And then we take note that the "chord joining the points for which $x=a$ and $x=b$" has the slope equal to $\frac{\Delta y}{\Delta x} = \frac{f(b)-f(a)}{b-a}$.\\
Next, we know that the slope of a function at $x = \frac{a+b}{2}$ is simply $f'(\frac{a+b}{2})$ and $f'(x) = 2Ax+B$.\\
Equating the two:
\begin{eqnarray*}
\frac{\Delta y}{\Delta x} = \frac{f(b)-f(a)}{b-a} &=& f'(\frac{a+b}{2})\\
\frac{(Ab^2+Bb+C)-(Aa^2+Ba+C)}{b-a} &=& 2A(\frac{a+b}{2})+B\\
\frac{A(b^2-a^2)+B(b-a)}{b-a} &=& A(a+b)+B\\
\frac{A(b+a)(b-a)+B(b-a)}{b-a} &=& A(a+b)+B\\
A(a+b)+B &=& A(a+b)+B\\
\end{eqnarray*}
Thus, we can see that this is true for any general quadratic when $a \neq b$.\\
\end{solution}
