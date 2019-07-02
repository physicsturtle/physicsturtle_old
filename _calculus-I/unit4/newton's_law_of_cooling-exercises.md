---
layout: lesson
title: Newton's Law of Cooling - Exercises
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---
\question[$**$] A glass of water is left out for a long time at room temperature of $20 \degree$C. Someone puts it in the freezer which is held at a constant temperature of $-5 \degree$C. At 2pm, it is $10 \degree$ C, and at 3pm its just about to begin freezing. When was it put into the freezer?

\begin{solution}
We apply Newton's Law of Cooling: 
\[\frac{dT}{dt} = k(T_0-T)\]
To solve the differential equation, let 
\[z(t) = T_0-T \Rightarrow z'(t) = -T'(t)\]
This means we can plug $z$ into the Newton's law of cooling to obtain the simplified version
\[z'(t) = -kz(t) \]
This equation has known solution 
\[ z(t) = Ce^{-kt}\]
With out definition of $z$ above, we can plug $T$ back in to obtain 
\[T(t) = T_0 -Ce^{-kt}\]
Plugging in the value of the ambient temperature, $T_0 = -5\degree\si{C}$, 
\[T(t) = -5 - Ce^{-kt}\]
Define $t = 0$ at 2pm. Then $T(0) = 10$, and $T(1) = 0$. Plugging $T(0) = 10$, we can solve 
\[-5 - C = 10\] 
solving for $C$:
\[C = -15\]
Now we have \[T(t) = -5+15e^{-kt}\]
Plugging in the other condition, $T(1) = 0$, we get 
\[-5 + 15e^{-k} = 0 \]
which allows us to solve for \[ k = \log(3)\]
So \[T(t) = -5+15(3^{-t})\]
We plug in $T = 20$ to find the time at which the water was put into the freezer. 
\[20 = -5+15(3^{-t}) \]
We can then solve for $t$:
\[ t = -\frac{\log5}{\log3}\]
By the laws of logarithms, we can rewrite
\[t = -\log_3(5)\]
So the water was put into the freezer $\log_3(5)$ hours \textit{before} 2pm.
\end{solution}
