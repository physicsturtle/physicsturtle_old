---
layout: lesson
title: Linear Approximations and Differentials
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---



\question[$*$] Compute the differential of the function $y = \sqrt{3+x^2}$.

\begin{solution}[40mm]
\[dy = \frac{x}{\sqrt{3+x^2}}dx\]
\end{solution}

\question[$*$] Use a linear approximation to estimate the value of $29^{-1/3}$.

\begin{solution}
Consider \[f(x) = \frac{1}{\sqrt[3]{x}}\]
Then we can compute the linear approximation to $f(x)$ at $ x = 27$ to then find a value that approximates $29^{-1/3}$.
\begin{eqnarray*}
L(x) &=& f(27) + f'(27)(x-27)\\
&=& \frac{1}{3} - \frac{1}{3\cdot 27^{4/3}}(x-27)\\
&=& \frac{1}{3} - \frac{1}{243}(x-27)
\end{eqnarray*}
Evaluating at $x = 29$, we have 
\[L(29) = \frac{1}{3} - \frac{2}{243} = \frac{81 - 2}{243} = \frac{79}{243}\]
\end{solution}



















