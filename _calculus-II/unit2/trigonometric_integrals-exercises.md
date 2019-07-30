---
layout: exercises
title: Trigonometric Integrals - Exercises
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---


<ol>
<li><div class="exercise"> Evaluate the integral. \[\int \sin^3x\cos^2x dx\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
Let $\cos x = u$, $du =  - \sin xdx$\\
\begin{eqnarray*}
\int \sin^3x\cos^2xdx &=&  - \int (1 - u^2)u^2du \\
&=& \int u^4 - u^2du \\
&=& \frac{u^5}{5} - \frac{u^3}{3} + C \\
&=& \frac{\cos^5x}{5} - \frac{\cos^3x}{3} + C\\
\end{eqnarray*}
\[\int \sin^3x\cos^2xdx = \frac{\cos^5x}{5} - \frac{\cos^3x}{3} + C\]
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral. \[\int \tan^4 x \sec^4 x dx\]

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
Let $u = \tan x$, $du = \sec ^2xdx$
\begin{eqnarray*}
\int u^4(u^2 + 1)du &=& \int u^6 + u^4du \\
&=& \frac{u^7}{7} + \frac{u^5}{5} + C \\
&=& \frac{\tan^7x}{7} + \frac{\tan^5x}{5} + C\\
\end{eqnarray*}
\[\int \tan^4x\sec^4xdx  = \frac{\tan^7x}{7} + \frac{\tan^5x}{5} + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. \[\int \sin^4 x dx\]

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >
\begin{eqnarray*}
\int \sin^4xdx  &=& \int \sin^2x(1 - \cos^2x )dx\\
&=& \int \sin^2x - \sin^2x\cos^2xdx\\
&=& \int \sin^2x dx - \int \sin^2x\cos^2xdx \\
&=& \int \frac{1 - \cos 2x}{2}dx - \int \frac{\sin^2 2x}{4}dx \\
&=& \frac{1}{2}x - \frac{\sin 2x}{4}  - \int \frac{1 - \cos 4x}{8}dx  \\
&=& \frac{1}{2}x - \frac{\sin 2x}{4} - \frac{1}{8}x + \frac{\sin 4x}{32} + C\\
&=& \frac{3x}{8} - \frac{\sin 2x}{4} + \frac{\sin 4x}{32} + C\\
\end{eqnarray*}
\[\int \sin^4xdx  = \frac{3x}{8} - \frac{\sin 2x}{4} + \frac{\sin 4x}{32} + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. \[\int x(\cos^3(x^2) - \sin^3(x^2)) dx\]

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer" >
Let  $x^2 = u$, $du = 2xdx$. Then
\begin{eqnarray*}
\int x(\cos^3(x^2) - \sin^3(x^2)) dx &=& \frac{1}{2}\int \cos^3u  - \sin ^3udu\\
&=& \frac{1}{2}\int \cos^3udu - \frac{1}{2}\int \sin^3udu  \\
&=& \frac{1}{2}\int (1 - \sin^2u)\cos udu  - \frac{1}{2}\int (1 - \cos^2u)\sin udu \\
&=& \frac{1}{2}\int \cos u - \sin^2u\cos udu - \frac{1}{2}\int \sin u - \cos^2u\sin udu \\
&=& \frac{1}{2}\sin u - \frac{1}{6}\sin^3u + \frac{1}{2}\cos u - \frac{1}{6}\cos^3u \\
&=& \frac{1}{12}\left( 6(\sin u + \cos u) - 2(\sin^3u + \cos^3u) \right)\\
&=& \frac{1}{12}\left( 6(\sin u + \cos u) - 2(\sin u + \cos u)(\sin^2u + \cos^2u - \sin u\cos u) \right)\\
&=& \frac{\sin u + \cos u}{12}\left( {6 - (2 - \sin 2u)} \right) + C \\
&=& \frac{1}{12}(\sin (x^2) + \cos (x^2))(4 + \sin (2x^2)) + C\\
\end{eqnarray*}
Thus the final answer is
\[\int x(\cos^3(x^2) - \sin^3(x^2))dx  = \frac{1}{12}(\sin (x^2) + \cos (x^2))(4 + \sin (2x^2)) + C\]
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral. \[\int \sin^3(3x) \cos^5(3x) dx\]

<div class="answerBox">
<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer" >
Let $3x = u$, and $3dx = du$. 
\begin{eqnarray*}
\int \sin^3(3x) \cos^5(3x) dx &=& \frac{1}{3}\int \sin^3(u)\cos^5(u)du \\
&=& \frac{1}{3}\int (1 - \cos^2u)\sin u\cos^5(u)du 
\end{eqnarray*}
Let $ \cos u = z$, and $dz = -\sin u du$. 
\begin{eqnarray*}
\frac{1}{3}\int (1 - \cos^2u)\sin u\cos^5(u)du  &=& \frac{1}{3}\int (z^2 - 1)z^5dz  \\
&=& \frac{1}{3}\int z^7 - z^5dz \\
&=& \frac{1}{3}\left( \frac{z^8}{8} - \frac{z^6}{6} \right)\\\
&=& \frac{1}{3}\left( \frac{\cos^8(3x)}{8} - \frac{\cos^6(3x)}{6} \right) + C
\end{eqnarray*}
Thus the final answer is 
\[\int \sin^3(3x) \cos^5(3x) dx = \frac{1}{3}\left( \frac{\cos^8(3x)}{8} - \frac{\cos^6(3x)}{6} \right) + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. \[\int\tan^5 x dx\]

<div class="answerBox">
<button onclick="myFunction('answer6')" class="answerButton">Show Answer</button>
<div  id="answer6" class="answer" >
\begin{eqnarray*}
\int \tan^5xdx  &=& \int (\sec^2x - 1)\tan^3xdx  \\
&=& \int \sec^2x\tan^3x - \tan^3xdx\\
&=& \frac{\tan^4x}{4} - \int(\sec^2x - 1)\tan xdx  \\
&=& \frac{\tan^4x}{4} - \int \sec^2x\tan x - \tan xdx \\
&=& \frac{\tan^4x}{4} - \frac{\tan^2x}{2} + \log \left| \sec x \right| + C
\end{eqnarray*}
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. \[\int \tan^3(2x)\sec^3(2x) dx\]

<div class="answerBox">
<button onclick="myFunction('answer7')" class="answerButton">Show Answer</button>
<div  id="answer7" class="answer" >First, let $2x = u$ and $2dx = du$. 
\begin{eqnarray*}
\int \tan^3(2x)\sec^3(2x)dx  &=& \frac{1}{2}\int \tan^3u\sec^3udu   \\
&=& \frac{1}{2}\int (\sec^2u - 1)\sec^3u\tan udu\\
\end{eqnarray*}
Now let $ \sec u = z$ and $dz = \sec u\tan udu$.
\begin{eqnarray*}
\frac{1}{2}\int (\sec^2u - 1)\sec^3u\tan udu  &=& \frac{1}{2}\int (z^2- 1)z^2 dz \\
&=& \frac{1}{2}\int z^4 - z^2 dz\\
&=& \frac{1}{2}\left( \frac{z^5}{5} - \frac{z^3}{3} \right) + C \\
&=& \frac{1}{2}\left( \frac{\sec^5(2x)}{5} - \frac{\sec^3(2x)}{3} \right) + C
\end{eqnarray*}
</div>
</div>
</div>
</li>


</ol>
