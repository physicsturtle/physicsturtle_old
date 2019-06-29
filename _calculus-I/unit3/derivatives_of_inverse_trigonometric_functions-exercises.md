---
layout: lesson
title: Derivatives of Inverse Trigonometric Functions - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

\begin{questions}
\question[$*$] Differentiate the following function. $y = \arctan\left(\frac{3}{x}\right)$

\begin{solution}[100mm]
Apply the chain rule:
\begin{eqnarray*}
y' &=& \frac{1}{1+\left(\frac{3}{x}\right)^2}\cdot \frac{-3}{x^2} \\
&=& \frac{-3}{x^2(1+\frac{9}{x^2})} \\
&=& \frac{-3}{x^2+9}
\end{eqnarray*}

\end{solution}

\question[$**$] Differentiate the following function. $\displaystyle{y = x^2\arccos\left(\frac{2}{x}\right)}$

\begin{solution} [100mm]
First we find the derivative of $\arccos(2/x)$, then apply the product rule to the entire function.
\begin{eqnarray*}
\left[\arccos\left(\frac{2}{x}\right)\right]' &=& -\frac{1}{\sqrt{1-\left(\frac{2}{x}\right)^2}}\cdot-\frac{2}{x^2} \\
&=& \frac{2}{x^2\sqrt{1-\frac{4}{x^2}}}\\
&=& \frac{2}{x\sqrt{x^2-4}}
\end{eqnarray*}
Now we differentiate the entire function:
\begin{eqnarray*}
y' &=& [x^2\arccos(2/x)]' \\
&=& (2x)\left(\arccos\left(\frac{2}{x}\right)\right)+(x^2)\left(\frac{2}{x\sqrt{x^2-4}}\right)\\
&=& 2x\arccos\left(\frac{2}{x}\right)+\frac{2x}{\sqrt{x^2-4}}
\end{eqnarray*}

\end{solution}

\question[$**$] Differentiate the following function. $\displaystyle{y = \arcsin ( e^x \cdot \tan x})$

\begin{solution}[100 mm]
\[y' = \frac{e^x(\tan x + \sec^2 x)}{\sqrt{1-(e^x\tan x)^2}}\]
\end{solution}
