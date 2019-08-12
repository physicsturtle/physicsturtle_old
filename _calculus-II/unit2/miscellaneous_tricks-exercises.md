---
layout: exercises
title: Miscellaneous Tricks - Exercises
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >


\question Compute the integral  by using the complex exponential. 
\[\int e^{2x}\sin(3x)dx\]
\begin{hint} \[\int e^{2x}\sin 3xdx  = \im \left( \int e^{2x}e^{i3x} dx \right) =\im \left( \int e^{(2 + 3i)x}dx \right)\] \end{hint}

\begin{solution}
\begin{eqnarray*}
\int e^{2x}\sin 3xdx &=& \im  \left( \int e^{2x}e^{i3x} dx \right) \\
&=& \im \left( \int e^{(2 + 3i)x}dx \right)\\
&=&\im\left( \frac{1}{2 + 3i}e^{(2 + 3i)x} \right)\\
&=&\im \left[ e^{2x}\frac{1}{2 + 3i}\left( \cos 3x + i\sin 3x \right)\right]\\
&=&\im \left[ e^{2x}\frac{1}{13}\left( \cos 3x + i\sin 3x \right)(2 - 3i)\right]\\
&=& \im \left[e^{2x}\frac{1}{13}\left( 2\cos 3x + 3\sin 3x + i(2\sin 3x - 3\cos 3x) \right)\right]\\
&=& \frac{e^{2x}}{13}(2\sin 3x - 3\cos 3x)
\end{eqnarray*}\\
Thus 
\[\int e^{2x}\sin 3xdx   =  \frac{e^{2x}}{13}(2\sin 3x - 3\cos 3x) + C\]
\end{solution}

\question[$***$] Connection with Math 101. Compute the integral  by using the complex exponential. \[\int\sin(\log(x))dx\]
\begin{hint} \[x^i = e^{i\log x} = \cos (\log x) + i\sin (\log x)\] \end{hint}

\begin{solution}
\begin{eqnarray*}
\int \sin (\log (x))dx  &=& \im \left( \int \cos (\log x) + i\sin (\log x)dx \right) \\
&=& \im \left( \int e^{i\log x}dx \right) \\
&=& \im \int x^i dx \\
&=& \im\left(\frac{x^{i + 1}}{i + 1}\right)\\
&=& \im\left( \frac{x}{i + 1}\left( \cos (\log x) + i\sin (\log x)\right)\right)\\
&=&\im \left( \frac{x}{2}\left( {\cos (\log x) + i\sin (\log x)} \right)(1 - i) \right)\\
&=&\im\left[ \frac{x}{2}\left( {\cos (\log x) + \sin (\log x) + i(\sin (\log x) - \cos (\log x))} \right)\right]\\
&=& \frac{x}{2}(\sin (\log x) - \cos (\log x))\\
\end{eqnarray*}
Thus
\[\int {\sin (\log (x))dx}  = \frac{x}{2}(\sin (\log x) - \cos (\log x)) + C\]
\end{solution}
