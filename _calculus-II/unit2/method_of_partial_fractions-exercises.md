---
layout: exercises
title: Method of Partial Fractions - Exercises
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---



<ol>
<li><div class="exercise"> Evaluate the integral. \[\int \frac{dx}{x^2+7x+6}\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
\begin{eqnarray*}
\int \frac{dx}{x^2 + 7x + 6} &=& \int \frac{dx}{(x + 6)(x + 1)}\\
&=& \frac{1}{5}\int \frac{1}{x + 1} - \frac{1}{x + 6}dx \\
&=& \frac{1}{5}\log \left| \frac{x + 1}{x + 6} \right| + C
\end{eqnarray*}
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral. \[\int \frac{x+1}{x^3 + x^2 - 6x} dx\]

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
\begin{eqnarray*}
\int \frac{x + 1}{x^3 + x^2 - 6x}dx  &=& \int \frac{x + 1}{x(x + 3)(x - 2)}dx  \\
&=& \int  - \frac{1}{6x} + \frac{3}{10(x - 2)} - \frac{2}{15(x + 3)}dx\\
& =&  - \frac{1}{6}\log \left| x \right| + \frac{3}{10}\log \left| {x - 2} \right| - \frac{2}{15}\log \left| {x + 3} \right| + C
\end{eqnarray*}
</div>
</div>
</div>
</li>




<li><div class="exercise">Evaluate the integral 
\[\int\frac{e^x}{(e^x - 2)(e^{2x} + 1)} dx\]

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >
Let $e^x = u$. Then $du = e^x dx$. The integral is then transformed to
\[\int\frac{e^x}{(e^x - 2)(e^{2x} + 1)} dx = \int \frac{du}{(u-2)(u^2 +1)}\]
We apply a partial fraction decomposition to this. Just looking at the integrand, 
\[\frac{1}{(u-2)(u^2+1)} = \frac{1}{5(x-2)}- \frac{x}{5(x^2+1)}-\frac{2}{5(x^2+1)}\]
Now integrating term by term, we have
\[\int \frac{du}{(u-2)(u^2 +1)} = \frac{1}{5}\log|u-2| - \frac{1}{10}\log(u^2+1) - \frac{2}{5}\arctan u + C\] 
Now transforming back to the original variable $x$, 
\[\int\frac{e^x}{(e^x - 2)(e^{2x} + 1)} dx = \frac{1}{5}\log|e^x - 2| - \frac{1}{10}\log(e^{2x} + 1) - \frac{2}{5}\arctan e^x + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise">Evaluate the integral
\[\int_0^1\frac{1}{1+\sqrt[3]{x}}dx\]

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer" >
Let $x = u^3$. Then $dx = 3u^2 du$, and the integral becomes
\[\int_0^1\frac{1}{1+\sqrt[3]{x}}dx = \int_0^1 \frac{3u^2}{1+u} du\]
Just looking at the integrand, it can be expanded by partial fractions to obtain
\[\frac{3u^2}{1+u} = 3\left(u-1+\frac{1}{u+1}\right)\]
Now plugging this back into the integral, 
\[\int_0^1\frac{1}{1+\sqrt[3]{x}}dx =3 \int_0^1 \left(u-1+\frac{1}{u+1}\right)du\]
This is easily evaluated as 
\[\int_0^1\frac{1}{1+\sqrt[3]{x}}dx = 3\left.\left(\frac{u^2}{2} - u + \log|u+1|\right)\right|^1_0\]
Finally we have
\[\int_0^1\frac{1}{1+\sqrt[3]{x}}dx = 3\log 2 - \frac{3}{2}\]
</div>
</div>
</div>
</li>




<li><div class="exercise">\label{secant} Evaluate the integral without referring to the attached table. \[\int \sec x dx\]

<div class="answerBox">
<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer" >
We first manipulate the integrand to make it possible to use partial fractions.
\begin{eqnarray*}
\int \sec \theta d\theta &=& \int \frac{1}{\cos \theta}d\theta \\
&=& \int \frac{\cos \theta }{\cos^2\theta}d\theta \\
&=& \int \frac{\cos \theta}{1-\sin^2\theta }d\theta 
\end{eqnarray*}
Let $\sin \theta  = u$, and $du = \cos \theta d\theta$. This transforms the integral in to
\begin{eqnarray*}
\int \frac{\cos \theta}{1-\sin^2\theta }d\theta  &=&\int \frac{du}{1 - u^2} \\
&=& \frac{1}{2}\int \frac{1}{1 + u} + \frac{1}{1 - u} du \\
&=& \frac{1}{2}\log \left| \frac{1 + u}{1 - u} \right| = \frac{1}{2}\log \left| \frac{1 + \sin \theta }{1 - \sin \theta } \right| \\ 
&=& \frac{1}{2}\log \left| \frac{1 + \sin \theta }{1 - \sin \theta }\left( \frac{1 + \sin \theta }{1 + \sin \theta } \right) \right| \\
&=& \frac{1}{2}\log \left| \frac{(1 + \sin \theta )^2}{\cos^2\theta } \right|\\
& =& \log \left| \frac{1+\sin \theta }{\cos \theta } \right|\\
&=& \log \left| {\sec \theta  + \tan \theta } \right| \\
\end{eqnarray*}
Thus
\[\int {\sec \theta d\theta }  = \log \left| {\sec \theta  + \tan \theta } \right| \]
</div>
</div>
</div>
</li>




<li><div class="exercise">Evaluate the integral. The attached table may be useful. \[\int\frac{dx}{x\sqrt{9+4x^2}}\]

<div class="answerBox">
<button onclick="myFunction('answer6')" class="answerButton">Show Answer</button>
<div  id="answer6" class="answer" >
To evaluate this integral we recognize it as the form of a trigonometric substitution. Let $x = \frac{3}{2}\tan z$, and $dx = \frac{3}{2}\sec^2z dz$. Note that we will have to evaluate the integral of $\csc$ along the way for this problem. You may use the attached table, but we will show the steps to evaluate the $\csc$ integral regardless.
\begin{eqnarray*}
\int \frac{\sec^2z}{\tan z\sqrt{9 + 9\tan^2z}}dz  &=& \frac{1}{3}\int\frac{\sec z}{\tan z}dz \\
&=& \frac{1}{3}\int \frac{1}{\sin z}dz \\
&=& \frac{1}{3}\int \frac{\sin z}{\sin^2z}dz  = \frac{1}{3}\int \frac{\sin z}{1 - \cos^2z}dz 
\end{eqnarray*}
Now we have to set this up for a partial fraction decomposition:
Let $\cos z = u$, and $du =  - \sin zdz$
\begin{eqnarray*}
- \frac{1}{3}\int \frac{1}{1 - u^2} du &=&  - \frac{1}{6}\int \frac{1}{1+u} + \frac{1}{1-u}du \\
&=& \frac{-1}{6}\log \left| \frac{1 + u}{1 - u} \right| \\
&=& \frac{1}{6}\log \left| \frac{1 - u}{1 + u} \right| \\
&=& \frac{1}{6}\log \left| \frac{1 - \cos z}{1 + \cos z} \right| \\
&=& \frac{1}{6}\log \left| \frac{1 - \cos z}{1 + \cos z}\left( \frac{1 - \cos z}{1 - \cos z} \right) \right|\\
&=& \frac{1}{6}\log \left| \frac{(1 - \cos z)^2}{\sin^2z} \right|\\
&=& \frac{1}{3}\log \left| \frac{1 - \cos z}{\sin z} \right|\\
&=& \frac{1}{3}\log \left| \csc z - \cot z \right| + C \\
&=& \frac{1}{3}\log \left| \frac{\sqrt{9 + 4x^2}  - 3}{x} \right| + C\\
\end{eqnarray*}
Thus our final answer is
\[\int \frac{dx}{x\sqrt{9 + 4x^2}}  = \frac{1}{3}\log \left| \frac{\sqrt{9 + 4x^2}  - 3}{x} \right| + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise">Evaluate the integral. \[\int \frac{x^4 - x^3 - x + 1}{x^3 - x^2} dx\]

<div class="answerBox">
<button onclick="myFunction('answer7')" class="answerButton">Show Answer</button>
<div  id="answer7" class="answer" >
\begin{eqnarray*}
\int \frac{x^4 - x^3 - x + 1}{x^3 - x^2} dx &=& \int x - \frac{x - 1}{x^3 - x^2}dx  \\
&=& \frac{1}{2}x^2 - \int \frac{x - 1}{x^2(x - 1)}dx \\
&=& \frac{1}{2} x^2 - \int \frac{1}{x^2}dx  \\
&=& \frac{1}{2}x^2 + \frac{1}{x} + C
\end{eqnarray*}
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. The attached table may be useful.
\[\int^{\pi/2}_0 \frac{\cos\theta}{\sqrt{1+\sin^2\theta}} d\theta\]

<div class="answerBox">
<button onclick="myFunction('answer8')" class="answerButton">Show Answer</button>
<div  id="answer8" class="answer" >
Let $\sin\theta = u$, and $du = \cos\theta d\theta$. Then we have the integral
\[\int^{\pi/2}_0 \frac{\cos\theta}{\sqrt{1+\sin^2\theta}} d\theta = \int_0^1 \frac{du}{\sqrt{1+u^2}}\]
Let $u = \tan\varphi$, $du = \sec^2\varphi d\varphi$. Then the integral is now
\[\int_0^1 \frac{du}{\sqrt{1+u^2}} = \int_0^{\pi/4} \sec \varphi d\varphi\]
By the secant example, we have
\[\int_0^{\pi/4} \sec \varphi d\varphi = \left.\left(\log|\sec\varphi + \tan\varphi|\right)\right|^{\pi/4}_0\]
</div>
</div>
</div>
</li>



</ol>
