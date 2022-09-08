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

In doing this exercises, note that there are many instances where a $u$-substitution will be necessary in addition to integration by parts. Also, recall the basic formulas (which should be memorized)

$$\begin{eqnarray*}
\int x^n \d x &=& \frac{x^{n+1}}{n+1} ,\qquad (n\not=-1)\\
\int \sin x \d x &=& -\cos x \\
\int \cos x \d x &=& \sin x \\
\int \frac{\d x}{1+x^2} &=& \arctan x \\
\int e^x \d x &=& e^x \\
\int \frac{\d x}{x} &=& \log|x| 
\end{eqnarray*}$$

<ol> 
<li><div class="exercise"> Evaluate the integral
$$\int x^2\sin 3x \d x $$

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
To solve this problem, we note that the function which we want to differentiate is the $x^2$. The sine does not become more complicated if it's integrated, but the $x^2$ becomes simpler if differentiated. We will have to integrate by parts twice. Thus, 
\begin{align*}
\int x^2\sin 3x \d x =& -x^2\frac{\cos 3x}{3} + \frac{2}{3}\int x\cos 3x \d x \\
=& -\frac{x^2}{3}\cos 3x + \frac{2x}{9}\sin 3x - \frac{2}{9}\int \sin 3x \d x \\
=& -\frac{x^2}{3}\cos 3x + \frac{2x}{9}\sin 3x + \frac{2}{27}\cos 3x + C
\end{align*}

</div>
</div>
</div>
</li>

<li><div class="exercise"> Evaluate the integral
$$\int x^3 e^{-x} \d x $$

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
To solve this problem, we note that the function we want to differentiate is the $x^2$. The exponential does not become more complicated if it's integrated, but the $x^3$ becomes simpler if differentiated. We will have to integrate by parts three times. Thus, 
\begin{align*}
\int x^3 e^{-x} \d x =& -x^3 e^{-x} + \int 3x^2 e^{-x} \d x \\
=& -x^3 e^{-x} - 3x^2 e^{-x} + \int 6x e^{-x} \d x \\
=& -x^3 e^{-x} -3x^2 e^{-x} - 6x e^{-x} + \int 6 e^{-x} \d x \\
=& -(x^3 + 3x^2 + 6x + 6)e^{-x} + C
\end{align*}
</div>
</div>
</div>
</li>


<li><div class="exercise">[$**$] Evaluate the integral
\[\int^\pi_0 e^{\cos t}\sin(2t) \d t\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
First we will find the antiderivative. Let $u = \cos t$, and $\d u = -\sin t \d t$.
\begin{eqnarray*}
\int e^{\cos t}\sin(2t) \d t &=& \int e^{\cos t} 2\sin t \cos t \d t \\
&=& -2\int e^u u \d u\\
&=& -2 (u-1)e^u + C\\
&=& 2(1-\cos t)e^{\cos t} + C
\end{eqnarray*}
Now evaluating at the bounds of integration, we have 
\[\int^\pi_0 e^{\cos t}\sin(2t) \d t = 2(1-\cos \pi) e^{\cos \pi} - 0 = \frac{4}{e}\]
</div>
</div>
</div>
</li>


<li><div class="exercise">[$**$] Evaluate the integral
\[\int\cos\left(\sqrt{x}\right) \d x\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
First make the substitution $u = \sqrt{x}$, and $2u \d u = \d x$:
\[\int\cos\left(\sqrt{x}\right) \d x = \int\cos(u) 2u \d u\]
Now integrating by parts, we have
\[ \int\cos(u) 2u \d u = 2\left(u\sin u - \int\sin u \d u\right)\]
Thus the final answer in terms of $u$ is
\[2u\sin u + 2\cos u +C\]
Then putting back in terms of $x$,
\[\int\cos\left(\sqrt{x}\right) \d x = 2\sqrt{x}\sin\left(\sqrt{x}\right) + 2\cos\left(\sqrt{x}\right) + C\]
</div>
</div>
</div>
</li>


<li><div class="exercise">[$**$]Evaluate the integral
\[\int \cos\left(\log x\right) \d x\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
First, let $\log x = u$. Then $\d u = \d x/x = e^{-u} \d x$. Thus $\d x = e^u \d u$. We can then transform the integral as
\[\int \cos\left(\log x\right) \d x = \int \cos u e^u \d u\]
We then integrate by parts twice, both times integrating the exponential, and differentiating the trigonometric function. Note that we would get the same result had we instead differentiated the exponential, and integrated the trigonometric function. 
\[\int e^u \cos u \d u = e^u\cos u + e^u \sin u - \int e^u\cos u \d u\]
Rearranging, we have
\[2\int e^u \cos u \d u = e^u(\cos u + \sin u)\]
Then solving for the integral, we have
\[\int e^u\cos u \d u = \frac{e^u}{2}(\cos u + \sin u)\]
Now plugging back in the original variables, we have
\[\int \cos\left(\log x\right) \d x = \frac{x}{2}(\cos(\log x) + \sin(\log x)) + C\]

</div>
</div>
</div>
</li>


<li><div class="exercise">[$***$] Evaluate the integral
\[\int x\arctan x \d x \]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
First we need to compute
\[\int\arctan x \d x\]
The way to do this is to integrate by parts, letting $u' = 1$, and $v = \arctan x$. Then we have
\[\int\arctan x \d x = x\arctan x - \int\frac{x}{x^2+1}\d x\]
This then evaluates to 
\[\int\arctan x \d x = x\arctan x - \frac{1}{2}\log(1+x^2)\]
Now we return to the original integral. We will have to integrate by parts. Let $x = u'$, and $\arctan x = v$. Then we have
\begin{eqnarray*}
\int x\arctan x \d x &=& \frac{x^2}{2}\arctan x - \frac{1}{2}\int \frac{x^2}{1+x^2}\d x \\
&=& \frac{x^2}{2}\arctan x - \frac{1}{2}\int\frac{x^2+1}{1+x^2} - \frac{1}{1+x^2} \d x\\
&=& \frac{x^2}{2}\arctan x - \frac{x}{2} + \frac{\arctan x}{2} + C
\end{eqnarray*}
Thus we have
\[\int x\arctan x \d x =\frac{x^2}{2}\arctan x - \frac{x}{2} + \frac{\arctan x}{2} + C \]
</div>
</div>
</div>
</li>


<li><div class="exercise">[$**$] Find the value of the integral. \[\int^e_1 \log x \d x\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
\begin{align*}
\int_1^e \log x\d x  =& \left. \left( x\log x - x \right) \right|_1^e \\
=& e\log e - e - (1\log 1 - 1) \\
=& e - e + 1 \\
=& 1\\
\end{align*}
\[\int_1^e \log x\d x  = 1\]

</div>
</div>
</div>
</li>


<li><div class="exercise">[$**$] Evaluate the integral. \[\int (\sin x)(\sin 3x) \d x\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
We will have to integrate this by parts twice:
\begin{eqnarray*}
\int (\sin x)(\sin 3x)\d x &=&  - \cos x\sin 3x + 3\int \cos x\cos 3x\d x \\
&=&  - \cos x\sin 3x + 3\left( \sin x\cos 3x + 3\int \sin x\sin 3x\d x \right)\\
&=&  - \cos x\sin 3x + 3\sin x\cos 3x + 9\int {\sin x\sin 3x\d x} \\
\end{eqnarray*}
Rearranging:
\[ - 8\int \sin x\sin 3x\d x =  - \cos x\sin 3x + 3\sin x\cos 3x\]
\[\int {\sin x\sin 3x\d x}  = \frac{1}{8}\cos x\sin 3x - \frac{3}{8}\sin x\cos 3x + C\]
</div>
</div>
</div>
</li>


<li><div class="exercise">[$***$] Evaluate the integral. \[\int x\arcsin x \d x\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
We will need to integrate by parts. Let $u = x$, and $v' = \arcsin x$. First we need to find $v(x)$. For this integral, integrate by parts, with the two functions being $1$ and $\arcsin x$. 
\begin{eqnarray*}
v(x) = \int \arcsin x\d x  = x\arcsin x + \sqrt{1 - x^2} \\
\end{eqnarray*}
\begin{eqnarray*}
\int x\arcsin x\d x  &=& x\left( x\arcsin x + \sqrt{1 - x^2} \right) - \int\left( x\arcsin x + \sqrt{1 -x^2} \right)\d x\\
&=& x^2\arcsin x + x\sqrt{1 - x^2}  - \int x\arcsin x\d x - \int {\sqrt{1 - x^2} \d x} \\
\end{eqnarray*}
Rearranging, 
\[2\int x\arcsin x\d x = x^2\arcsin x + x\sqrt{1 - x^2}  - \int {\sqrt{1 - x^2} \d x} \]
Now we need to find the antiderivative of $\sqrt{1-x^2}$. To do this, let $x = \sin z$, and $\d x = \cos z \d z$. 
\begin{eqnarray*}
\int \sqrt{1 - x^2} \d x  &=& \int \cos z^2\d z \\
&=& \frac{1}{2}\int 1 + \cos 2z\d z \\
&=& \frac{z}{2} +\frac{\sin 2z}{4} \\
&=& \frac{z}{2} + \frac{\sin z\cos z}{2}\\
&=& \frac{\arcsin x}{2} + \frac{x\sqrt{1-x^2}}{2}\\
\end{eqnarray*}
\begin{eqnarray*}
2\int {x\arcsin x\d x}  = x^2\arcsin x + x\sqrt{1 - x^2}  -\left(  \frac{\arcsin x}{2} + \frac{x\sqrt{1-x^2}}{2}\right)\\
2\int {x\arcsin x\d x}  = x^2\arcsin x + \frac{x\sqrt{1 - x^2}}{2} - \frac{\arcsin x}{2} + C\\
\end{eqnarray*}
Thus the final answer is 
\[\int {x\arcsin x\d x}  = \frac{x^2\arcsin x}{2} + \frac{x\sqrt{1 - x^2}}{4} - \frac{\arcsin x}{4} + C\]
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral.
$$\int e^{-3x}\sin (2x) \d x$$

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
In this one, we will need to integrate by parts twice. Let's integrate the exponential and differentiate the sine.
 
$$\int e^{-3x}\sin (2x) \d x = -\frac{1}{3}e^{-3x}\sin 2x + \frac{2}{3}\int e^{-3x}\cos 2x \d x $$

Applying integration by parts again by differentiating the cosine and integrating the exponential, 

\begin{align*}
\int e^{-3x}\sin (2x) \d x =& -\frac{1}{3}e^{-3x}\sin 2x + \frac{2}{3}\left(-\frac{1}{3}e^{-3x}\cos 2x - \frac{2}{3}\int e^{-3x}\sin 2x \d x\right)  \\
=& -\frac{1}{3}e^{-3x}\sin 2x - \frac{2}{9}e^{-3x}\cos 2x - \frac{4}{9}\int e^{-3x}\sin 2x dx
\end{align*}

Moving both integrals to the same side, 

\begin{align*}
\left(1 + \frac{4}{9}\right)\int e^{-3x}\sin 2x \d x =& -\frac{1}{3}e^{-3x}\sin 2x - \frac{2}{9}e^{-3x}\cos 2x\\
\frac{13}{9}\int e^{-3x}\sin 2x \d x =& -\frac{1}{9}e^{-3x}(3\sin 2x + 2\cos 2x)
\end{align*}

Lastly, isolating the integral, we get 
$$\int e^{-3x}\sin 2x \d x = -\frac{1}{13}e^{-3x}(3\sin 2x + 2\cos 2x) + C$$
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral. 
$$\int e^{3x}x^2\sin x \d x$$

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" > 
Let $e^{3x}\sin x = u'(x)$. We will have to use integration by parts multiple times, first to get rid of the $x^2$ term, then to integrate the remaining exponential and sine.

Let $U'(x)  =  u(x).$

\begin{eqnarray*}
\int x^2 u' \d x &=& x^2 u - 2\int xu \d x  \\
&=& x^2u - 2\left( xU - \int U \d x \right)\\
\end{eqnarray*}

First, we need to find $u(x)$, with $u'(x)$ defined as above. 

\begin{eqnarray*}
u(x) &=& \int u'(x) \d x \\
&=& \int e^{3x}\sin x \d x \\
&=& \frac{e^{3x}}{3}\sin x - \frac{1}{3}\int e^{3x}\cos x \d x\\
&=& \frac{e^{3x}}{3}\sin x - \frac{1}{3}\left( \frac{e^{3x}}{3} + \frac{1}{3}\int e^{3x}\sin x \d x \right)\\
\end{eqnarray*}

Rearranging, 

$$\frac{10}{9}\int e^{3x}\sin x \d x = \frac{e^{3x}}{9}\left( 3\sin x - \cos x\right)$$

which tells us that, after a simple rearrangement,

$$\int e^{3x}\sin x \d x  = \frac{e^{3x}}{10}\left( 3\sin x - \cos x \right).$$

In order to find $U(x)$, having already found $u(x)$, we need to perform the same procedure as in the previous integration. This is left to the reader, as it has already been shown once. 

\begin{eqnarray*}
U(x) &=& \int u(x) \d x \\
&=& \frac{e^{3x}}{50}\left( 4\sin x - 3\cos x \right)\\
\end{eqnarray*}
Lastly, we need the antiderivative of $U(x)$. That is computed in the same way as the two previous:

$$\int U(x)dx = \frac{e^{3x}}{500}(9\sin x - 13\cos x) $$

Plugging back into the original expression yields:

\begin{align*}
x^2u - 2\left( xU - \int U\d x \right) =& x^2\left( \frac{e^{3x}}{10}\left( 3\sin x - \cos x \right) \right) - 2x\left( \frac{e^{3x}}{50}\left( 4\sin x - 3\cos x \right) \right) + \\
&+2\left( \frac{e^{3x}}{500}(9\sin x - 13\cos x)\right)\\
=& \frac{e^{3x}}{250}\left( {25x^2(3\sin x - \cos x) - 10x(4\sin x - 3\cos x) + 9\sin x - 13\cos x} \right) + C
\end{align*}

$$\int e^{3x}x^2\sin x \d x = \frac{e^{3x}}{250}\left( 25x^2(3\sin x - \cos x) - 10x(4\sin x - 3\cos x) + 9\sin x - 13\cos x \right) + C$$

</div>
</div>
</div>
</li>


</ol>
