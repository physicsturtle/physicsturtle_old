---
layout: exercises
title: Kinematics Problems - Exercises
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---

\question[$**$] A body moves along a horizontal line according to the law $s = f(t) = t^3 - 9t^2 + 24t$. 
\begin{enumerate}[(a)]
\item When is $s$ increasing and when decreasing?
\item When is $v$ increasing and when decreasing?
\item When is the \textit{speed} of the body increasing and when decreasing?
\item Compute the total distance travelled in the first 5 seconds of motion.
\end{enumerate}

\begin{solution}
\begin{enumerate}[(a)]
\item Compute the derivative 
\[f'(t) = 3t^2-18t+24 = 3(t^2-6t+8)\] then find the zeroes. 
\[ t^2-6t+8 = (t-4)(t-2) = 0 \Rightarrow t = 2,4\] Solve the inequality $t^2-6t+8 > 0$  to find when $f$ is increasing. The solution then yields
\begin{itemize}
\item $s$ is increasing for $t\in(0,2)\cup(4,\infty)$
\item $s$ is decreasing for $t\in(2,4)$
\end{itemize}
\item $a(t) = 6t -18$, so then $v$ is decreasing for $t\in (0,3)$, and $v$ is increasing for $t\in(3,\infty)$.
\item The speed of a particle is the magnitude of its velocity:
\[|v| = 3|t^2-6t+8|\] 
Differentiating, we find 
\[\frac{d|v|}{dt} =\frac{v}{|v|}\cdot a = \sgn(v) a\]
where $\sgn(v)$ denotes the \textit{sign} of $v$ ($+1$ if $v$ is positive, $-1$ if $v$ is negative). Solve the inequalities for $\frac{d|v|}{dt}$ being positive and negative.
\begin{itemize}
\item To find where the speed is increasing, we have the inequality $(t^2-6t+8)(t-3) > 0$, which has solution $t\in(2,3)\cup(4,\infty)$.
\item To find where the speed is decreasing, we have the inequality $(t^2-6t+8)(t-3) < 0$, which has solution $t\in(0,2)\cup(3,4)$.
\end{itemize}
\item The total distance travelled in the first 5 seconds will be 
\begin{eqnarray*}
D &=& |f(2) - f(0)| + |f(4) - f(2)| + |f(5) - f(4)| \\
&=& |20 - 0| + |16 - 20| + |20 - 16| \\
&=& 28
\end{eqnarray*}
\end{enumerate}
\end{solution}
