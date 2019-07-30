---
layout: exercises
title: Integration by Parts - Exercises
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---



<ol> 
<li><div class="exercise"> Evaluate the integral
\[\int^\pi_0 e^{\cos t}\sin(2t) dt\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
First we will find the antiderivative. Let $u = \cos t$, and $du = -\sin t dt$.
\begin{eqnarray*}
\int e^{\cos t}\sin(2t) dt &=& \int e^{\cos t} 2\sin t \cos t dt \\
&=& -2\int e^u u du\\
&=& -2 (u-1)e^u + C\\
&=& 2(1-\cos t)e^{\cos t} + C
\end{eqnarray*}
Now evaluating at the bounds of integration, we have 
\[\int^\pi_0 e^{\cos t}\sin(2t) dt = 2(1-\cos \pi) e^{\cos \pi} - 0 = \frac{4}{e}\]
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral
\[\int\cos\left(\sqrt{x}\right) dx\]

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" > 
First make the substitution $u = \sqrt{x}$, and $2u du = dx$:
\[\int\cos\left(\sqrt{x}\right) dx = \int\cos(u) 2u du\]
Now integrating by parts, we have
\[ \int\cos(u) 2u du = 2\left(u\sin u - \int\sin u du\right)\]
Thus the final answer in terms of $u$ is
\[2u\sin u + 2\cos u +C\]
Then putting back in terms of $x$,
\[\int\cos\left(\sqrt{x}\right) dx = 2\sqrt{x}\sin\left(\sqrt{x}\right) + 2\cos\left(\sqrt{x}\right) + C\]
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral
\[\int x\arctan x dx \]

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" > 
First we need to compute
\[\int\arctan x dx\]
The way to do this is to integrate by parts, letting $u' = 1$, and $v = \arctan x$. Then we have
\[\int\arctan x dx = x\arctan x - \int\frac{x}{x^2+1}dx\]
This then evaluates to 
\[\int\arctan x dx = x\arctan x - \frac{1}{2}\log(1+x^2)\]
Now we return to the original integral. We will have to integrate by parts. Let $x = u'$, and $\arctan x = v$. Then we have
\begin{eqnarray*}
\int x\arctan x dx &=& \frac{x^2}{2}\arctan x - \frac{1}{2}\int \frac{x^2}{1+x^2}dx \\
&=& \frac{x^2}{2}\arctan x - \frac{1}{2}\int\frac{x^2+1}{1+x^2} - \frac{1}{1+x^2} dx\\
&=& \frac{x^2}{2}\arctan x - \frac{x}{2} + \frac{\arctan x}{2} + C
\end{eqnarray*}
Thus we have
\[\int x\arctan x dx =\frac{x^2}{2}\arctan x - \frac{x}{2} + \frac{\arctan x}{2} + C \]
</div>
</div>
</div>
</li>



<li><div class="exercise">Evaluate the integral
\[\int \cos\left(\log x\right) dx\]

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer" > 
First, let $\log x = u$. Then $du = dx/x = e^{-u} dx$. Thus $dx = e^u du$. We can then transform the integral as
\[\int \cos\left(\log x\right) dx = \int \cos u e^u du\]
We then integrate by parts twice, both times integrating the exponential, and differentiating the trigonometric function. Note that we would get the same result had we instead differentiated the exponential, and integrated the trigonometric function. 
\[\int e^u \cos u du = e^u\cos u + e^u \sin u - \int e^u\cos u du\]
Rearranging, we have
\[2\int e^u \cos u du = e^u(\cos u + \sin u)\]
Then solving for the integral, we have
\[\int e^u\cos u du = \frac{e^u}{2}(\cos u + \sin u)\]
Now plugging back in the original variables, we have
\[\int \cos\left(\log x\right) dx = \frac{x}{2}(\cos\log x + \sin\log x) + C\]

</div>
</div>
</div>
</li>



<li><div class="exercise">Evaluate the integral. \[\int (\sin x)(\sin 3x) dx\]

<div class="answerBox">
<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer" > 
We will have to integrate this by parts twice:
\begin{eqnarray*}
\int (\sin x)(\sin 3x)dx &=&  - \cos x\sin 3x + 3\int \cos x\cos 3xdx \\
&=&  - \cos x\sin 3x + 3\left( \sin x\cos 3x + 3\int \sin x\sin 3xdx \right)\\
&=&  - \cos x\sin 3x + 3\sin x\cos 3x + 9\int {\sin x\sin 3xdx} \\
\end{eqnarray*}
Rearranging:
\[ - 8\int \sin x\sin 3xdx =  - \cos x\sin 3x + 3\sin x\cos 3x\]
\[\int {\sin x\sin 3xdx}  = \frac{1}{8}\cos x\sin 3x - \frac{3}{8}\sin x\cos 3x + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise"> Find the value of the integral. \[\int^e_1 \log x dx\]

<div class="answerBox">
<button onclick="myFunction('answer6)" class="answerButton">Show Answer</button>
<div  id="answer6" class="answer" > 
\begin{eqnarray*}
\int_1^e \log xdx  &=& \left. \left( x\log x - x \right) \right|_1^e \\
&=& e\log e - e - (1\log 1 - 1) \\
&=& e - e + 1 \\
&=& 1\\
\end{eqnarray*}
\[\int_1^e \log xdx  = 1\]
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. \[\int x\arcsin x dx\]

<div class="answerBox">
<button onclick="myFunction('answer7')" class="answerButton">Show Answer</button>
<div  id="answer7" class="answer" > 
We will need to integrate by parts. Let $u = x$, and $v' = \arcsin x$. First we need to find $v(x)$. For this integral, integrate by parts, with the two functions being $1$ and $\arcsin x$. 
\begin{eqnarray*}
v(x) = \int \arcsin xdx  = x\arcsin x + \sqrt{1 - x^2} \\
\end{eqnarray*}
\begin{eqnarray*}
\int x\arcsin xdx  &=& x\left( x\arcsin x + \sqrt{1 - x^2} \right) - \int\left( x\arcsin x + \sqrt{1 -x^2} \right)dx\\
&=& x^2\arcsin x + x\sqrt{1 - x^2}  - \int x\arcsin xdx - \int {\sqrt{1 - x^2} dx} \\
\end{eqnarray*}
Rearranging, 
\[2\int x\arcsin xdx = x^2\arcsin x + x\sqrt{1 - x^2}  - \int {\sqrt{1 - x^2} dx} \]
Now we need to find the antiderivative of $\sqrt{1-x^2}$. To do this, let $x = \sin z$, and $dx = \cos z dz$. 
\begin{eqnarray*}
\int \sqrt{1 - x^2} dx  &=& \int \cos z^2dz \\
&=& \frac{1}{2}\int 1 + \cos 2zdz \\
&=& \frac{z}{2} +\frac{\sin 2z}{4} \\
&=& \frac{z}{2} + \frac{\sin z\cos z}{2}\\
&=& \frac{\arcsin x}{2} + \frac{x\sqrt{1-x^2}}{2}\\
\end{eqnarray*}
\begin{eqnarray*}
2\int {x\arcsin xdx}  = x^2\arcsin x + x\sqrt{1 - x^2}  -\left(  \frac{\arcsin x}{2} + \frac{x\sqrt{1-x^2}}{2}\right)\\
2\int {x\arcsin xdx}  = x^2\arcsin x + \frac{x\sqrt{1 - x^2}}{2} - \frac{\arcsin x}{2} + C\\
\end{eqnarray*}
Thus the final answer is 
\[\int {x\arcsin xdx}  = \frac{x^2\arcsin x}{2} + \frac{x\sqrt{1 - x^2}}{4} - \frac{\arcsin x}{4} + C\]
</div>
</div>
</div>
</li>


</ol>
