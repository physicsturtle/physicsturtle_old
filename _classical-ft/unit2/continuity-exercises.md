---
layout: exercise
title: Continuity - Exercises
dept: math
course: calculus-I
unit: unit2
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 2
---

### Exercises

\question[$**$] Find all values of $a$ such that $f$ is continuous for all $\mathbb{R}$:
\begin{displaymath}
f(x) = \left\{
\begin{array}{cc}
x+ 1 & x \leq a\\
x^2 & x > a
\end{array}
\right.
\end{displaymath}

\begin{solution}[60 mm]
For $f(x)$ to be continuous, $f(a)$ must be the same for both parts of the function at $x=a$
Computing the limit of $f$ as $x$ approaches $a$ (it is a very easy limit so we don't show its computation), and applying the condition of continuity, we get the equation:
\[ a+1=a^2\]
\[a^2-a-1=0\]
Using the quadratic formula to solve for $a$:
\[a = \frac{1\pm\sqrt{1+4}}{2}\]
\[a = \frac{1\pm \sqrt{5}}{2}\]
\end{solution}


\question[$***$] Find \textit{one pair} of values $a,b$ such that $f(x)$ is continuous at $x = 0$.
\begin{displaymath}
f(x) = \left \{
\begin{array}{lr}
(e^x - 1)\cos\left(\frac{1}{x}\right) & , x < 0 \\
\sin(x+a) + b &, x \geq 0
\end{array}
\right.
\end{displaymath}

\begin{solution}[200 mm]
The condition for continuity is 
\[f(a)= \lim_{x\to a^+}f(x) = \lim_{x\to a^-}f(x)\]

Left hand side limit:
\[\lim_{x\to0^-}f(x) = \lim_{x\to0^-}(e^x-1)\cos \left(\frac{1}{x}\right)\]
\[-1 \leq \cos\left(\frac{1}{x}\right) \leq 1\]
\[-(e^x-1) \leq (e^x-1)\cos \left(\frac{1}{x}\right) \leq (e^x-1)\]
\[\lim_{x\to0^-}-(e^x-1) \leq \lim_{x\to0^-}(e^x-1)\cos \left(\frac{1}{x}\right) \leq \lim_{x\to0^-}(e^x-1)\]
\[-(1-1) \leq \lim_{x\to0^-}(e^x-1)\cos \left(\frac{1}{x}\right) \leq 1-1\]
\[0 \leq \lim_{x\to0^-}(e^x-1)\cos \left(\frac{1}{x}\right) \leq 0\]
by the Squeeze Theorem, the left hand side limit, 
\[\lim_{x\to0^-}(e^x-1)\cos \left(\frac{1}{x}\right) = 0\]

Right hand side limit:
\[\lim_{x\to0^+}f(x) = \lim_{x\to0^+}\sin(x+a)+b \] The two lateral limits must be equal in order for $f(x)$ to be continuous, so we equate them.
\[\lim_{x\to0^+}\sin(x+a)+b=0\]
\[\sin(a)+b = 0\]
\[\sin(a)=-b\]

Overall $\sin(a)=-b$, for some $ a\in \mathbb{R}$ and $b\in [-1,1]$. There are infinitely many solutions to such an equation, and the most obvious solution is \[a=b=0\] An example of some others would be $a = n\pi$, $b = 0$.

\end{solution}

\question[$**$] For the function $f(x)$, determine the value of $a$ for which $f$ is continuous at $x = 0$.
\begin{displaymath}
f(x) = \left\{
\begin{array}{cc}
\frac{\sin^2(x)}{x} & x > 0 \\
a\cos x - 1 & x \leq 0
\end{array}
\right.
\end{displaymath}
You may use the fact that $\displaystyle{\lim_{x\to0} \frac{\sin(x)}{x}  = 1}$. 

\begin{solution}[100 mm]
We want to ensure that the limits of $f(x)$ as $x$ approaches zero from both sides are equal. First we compute the right hand side limit:
Since 
\[\lim_{x\to0} \frac{\sin(x)}{x} = 1 \]
We can write
\begin{eqnarray*}
\lim_{x\to0} \frac{\sin(x)\cdot\sin(x)}{x}&=&\lim_{x\to 0}\sin x \cdot \lim_{x\to 0}\frac{\sin x}{x}\\
&=& 0\cdot 1\\
&=& 0 
\end{eqnarray*}
In order for $f$ to be continuous, the left hand side limit must also be zero.
\[\lim_{x\to0} {a\cos(x)-1} = 0\]
Evaluating the limit yields
\[a-1=0\]
Solving for $a$:
\[a=1\]
\end{solution}
