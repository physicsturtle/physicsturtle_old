---
layout: exercises
title: Differential Equations - Exercises
dept: math
unit: unit3
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 3
courseDisplay: Calculus II
---

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >

\question[$**$] Find an implicit solution to the following differential equation 
\[\frac{dy}{dx} = \frac{y\cos x}{1+2y^2}\]

\begin{solution}[80mm]
First we separate variables:
\[\frac{1+2y^2}{y} dy = \cos x dx\]
Then we can integrate both sides with respect to the appropriate variable:
\begin{eqnarray*}
\int \frac{1+2y^2}{y} dy &=& \int \cos x dx\\
\int \left( \frac{1}{y} + 2y\right) dy &=& \sin x + C\\
\log|y| + y^2 &=& \sin x + C
\end{eqnarray*}
Thus the final answer is 
\[\log|y| + y^2 =\sin x + C\]
where we only have on constant of integration because one can be absorbed into another.
\end{solution}

\question[$**$] Solve the following initial value problem explicitly in terms of $y$:
\[\frac{dy}{dx} = x^2y^2 + xy^2 + yx^2 + xy,\quad y(0) = 5\]

\begin{solution}[200mm]
First we have to factor the RHS:
\[\frac{dy}{dx} = (x^2+x)(y^2+y)\]
Now we can separate variables:
\[\frac{dy}{y^2+y} = (x^2+x)dx\]
Since the variables are separated, we can integrate both sides with respect to the appropriate variable.
\begin{eqnarray*}
\int \frac{dy}{y^2+y} &=& \int  (x^2+x)dx\\
\int \left(\frac{1}{y} - \frac{1}{y+1}\right) dy&=& \frac{x^3}{3} + x + C\\
\log|y| - \log|y+1| &=& \frac{x^3}{3} + x + C\\
\log\left|\frac{y}{y+1}\right| &=&\frac{x^3}{3} + x + C\\
\left|\frac{y}{y+1}\right| &=&\tilde Ce^{\frac{x^3}{3} + x}\\
\end{eqnarray*}
Now we plug in the initial condition to obtain that $\tilde C = 5/6$. Thus since both sides are positive we have
\[\frac{y}{y+1} = \frac{5}{6} e^{\frac{x^3}{3} + x}\]
Now solving for $y$, we have the final solution
\[ y = \frac{(5/6)e^{\frac{x^3}{3} + x}}{1-(5/6)e^{\frac{x^3}{3} + x}}\]
\end{solution}


\question[$**$] Solve the differential equation: \[y'(\cos y)(x-1) = 2x\sin y\]

\begin{solution}[95mm]
Expressing in the Leibniz notation:
\[ \frac{dy}{dx}\cdot(x - 1)\cos y = 2x\sin y\]
Rearranging:
\[  \cot ydy = \frac{2x}{x - 1}dx\]
Integrating both sides:
\begin{eqnarray*}
\int \cot ydy  &=& \int \frac{2x}{x - 1}dx \\
\log \left| \sin y \right| &=& 2\int \frac{x}{x - 1}dx  \\
&=& 2\int \frac{x - 1 + 1}{x - 1}dx\\
&=& 2x + 2\log \left| {x - 1} \right|  + C\\
\end{eqnarray*}
Solving for $y = y(x)$:
\begin{eqnarray*}
\left| \sin y \right| &=& e^C(x - 1)^2e^{2x}\\
\sin y &=& C(x - 1)^2e^{2x} \\
y(x) &=& \arcsin \left( C(x - 1)^2e^{2x} \right)\\
\end{eqnarray*}
Where $C\in \mathbb{R}$ is an arbitrary constant.
\end{solution}


\question[$**$] Solve the differential equation. \[y' = y\log y \cot x\]

\begin{solution}[95mm]
Expressing in the Leibniz notation:
\[y\log y\cot x = \frac{dy}{dx}\]
Rearranging:
\[\frac{dy}{y\log y} = \cot xdx\]
Integrating both sides:
\[\int \frac{dy}{y\log y} = \int \cot xdx\]
\begin{eqnarray*}
\log \log |y| &=& \log \left| \sin x \right| + C\\
\log |y| &=& C\sin x \\
|y| &=& Ce^{\sin x}, \hspace{5mm} C>0\\
y &=&Ce^{\sin x}
\end{eqnarray*}
Where $C \in \mathbb{R}$ is an arbitrary constant. 
\end{solution}

\question[$**$] Solve the differential equation. \[xdy + (1+y^2)\arctan y dx = 0\]

\begin{solution}[120mm]
Rearranging: 
\[ xdy =  - (1 + y^2)\arctan ydx \]
\[\frac{dy}{(1 + y^2)\arctan y} =- \frac{dx}{x}\]
Integrating:
\[ \int \frac{dy}{(1 + y^2)\arctan y} = -\int \frac{dx}{x}\]
\[ \log \left| \arctan y \right| = -\log |x| + C\]
Solving for $y = y(x)$:
\[|\arctan y| = \frac{C}{x}\]
\[y = \tan \left(\frac{C}{x}\right)\]
Where $C \in \mathbb{R}$ is an arbitrary constant.
\end{solution}
