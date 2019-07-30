---
layout: exercises
title: Center of Mass - Exercises
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


\question[$**$] Find the centroid of the region bounded by the curves $y = 4x-x^2$, $y = x$. 

\begin{solution}[200mm]
The curves intersect at $x = 3$, and in this interval $(0,3)$, the curve $y = 4x - x^2$ is going to be above the curve $y = x$. Thus the area of the region is
\[A = \int_0^3 (4x - x^2 - x) dx = \frac{9}{2}\]
Now we can calculate the $x$ and $y$ coordinates of the centroid.
\begin{eqnarray*}
\overline x &=& \frac{1}{A} \int_0^3 x(f(x) - g(x))dx\\
&=& \frac{1}{A}\int_0^3 x(4x - x^2 - x)dx \\
&=& \frac{1}{A} \int_0^3 x(3x - x^2)dx \\
&=& \frac{1}{A} \int_0^3 3x^2 - x^3dx\\
&=& \frac{27}{4} \cdot \frac{2}{9} \\
&=& \frac{3}{2}\\
\end{eqnarray*}
Now the $y$ coordinate:
\begin{eqnarray*}
\overline y  &=& \frac{1}{2A}\int_0^3 (f(x))^2 - (g(x))^2dx \\
&=& \frac{1}{2A}\int_0^3 (4x - x^2)^2 - x^2dx\\
&=& \frac{108}{5} \cdot \frac{2}{9} \cdot \frac{1}{2} \\
&=& \frac{12}{5}\\
\end{eqnarray*}
Thus the centroid is
\[(\overline x ,\overline y ) = \left( \frac{3}{2},\frac{12}{5} \right)\]
\end{solution}


\question[$**$] Find the centroid of the region bounded by $9x^2+16y^2 = 144$ in the first quadrant.

\begin{solution}[210mm]
First, solving for $y$, we have
\[y = \frac{1}{4}\sqrt{144 - 9x^2}\]
Then the area in the firrst quadrant will be given by 
\[A = \int_0^4 \frac{1}{4}\sqrt{144 - 9x^2} dx = 3\pi\]
Note that the above integral can be easily computed by defining $z = 3x$, then using the area of a circle formula. Now we apply the formulas for the $x$ and $y$ coordinates of the centre of mass.
\begin{eqnarray*}
\overline x  &=& \frac{1}{A}\int_0^4 xf(x)dx\\
&=& \int_0^4 x\frac{1}{4}\sqrt{144 - 9x^2} dx \\
&=& \frac{16}{3\pi}
\end{eqnarray*}
Now for the $y$ component, 
\begin{eqnarray*}
\overline y  &=& \frac{1}{2A}\int_0^4 (f(x))^2dx \\
&=& \frac{1}{2A}\int_0^4 \frac{144 - 9x^2}{16}dx \\
&=& \frac{4}{\pi}\\
\end{eqnarray*}
Now the final answer is
\[(\overline x ,\overline y ) = \left( \frac{16}{3\pi},\frac{4}{\pi} \right)\]
\end{solution}

