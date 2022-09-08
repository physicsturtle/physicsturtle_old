---
layout: exercises
title: Substitution Rule - Exercises
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---

In this section, recall the basic formulas (which should be memorized):

$$\begin{eqnarray*}
\int x^n \d x &=& \frac{x^{n+1}}{n+1} ,\qquad (n\not=-1)\\
\int \sin x \d x &=& -\cos x \\
\int \cos x \d x &=& \sin x \\
\int \frac{\d x}{1+x^2} &=& \arctan x \\
\int e^x \d x &=& e^x \\
\int \frac{\d x}{x} &=& \log|x| 
\end{eqnarray*}$$

Armed with these formulas, you should be equipped to solve the following exercises. Also make sure that you keep your trigonometric identities in mind. Some of these integrals may seem quite complicated at first, but by using a trigonometric identity they are substantially simplified.

<ol>

<li><div class="exercise"> Compute the integral
$$\int 2\sin(3x) \d x$$

<div class="answerBox">
<button onclick="myFunction('answer0')" class="answerButton">Show Answer</button>
<div  id="answer0" class="answer" >
We make the substitution $u = 3x$, $\d u = 3\d x$, which gives us 

$$\int 2\sin(3x) \d x = 2\int \sin(u) \frac{\d u}{3} $$

and we can simply evaluate this after moving the $1/3$ to the front.

$$2\int \sin(u) \frac{\d u}{3} = \frac{2}{3}\int \sin u \d u = -\frac{2}{3}\cos u + C$$

Now substituting back in $u = 3x$, 

$$\int 2\sin(3x) \d x = -\frac{2}{3}\cos(3x) + C$$

</div>
</div>
</div>
</li>

<li><div class="exercise"> Evaluate the integral
$$\int \frac{x^2}{3}\cos(x^3) \d x$$

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
We recognize that we have the function $x^3$, and something which is almost its derivative, $x^2$. Thus we make the substitution $u = x^3$, $\d u = 3x^2\d x$. Doing this, we see that the $x^2$ in the numerator will cancel with the $x^2$ which is introduced in the denominator from the transformation of the differential. 

\begin{align}
\int \frac{x^2}{3}\cos(x^3) \d x=& \frac{1}{3}\int x^2 \cos(u) \frac{\d u}{3x^2} \\
=& \frac{1}{9}\int \cos u \d u \\
=& \frac{1}{9}\sin u + C\\
=& \frac{1}{9} \sin(x^3) + C
\end{align}

</div>
</div>
</div>
</li>

<li><div class="exercise"> Evaluate the integral
$$\int \cot\theta \d\theta$$

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
We rewrite the integral as 
$$\int \cot\theta \d\theta = \int \frac{\cos\theta}{\sin\theta} \d\theta$$
Making the substitution $u = \sin\theta$, and $\d u = \cos\theta \d\theta$, we have that 
$$\int \frac{\cos\theta}{\sin\theta} \d\theta = \int \frac{1}{u}{\d u}$$
This can be easily integrated to get 
$$\int \frac{1}{u}{\d u} = \log |u|.$$
Substituting back in, we find
$$\int \cot\theta \d\theta = \log|\sin\theta| + C.$$
</div>
</div>
</div>
</li>

<li><div class="exercise"> Compute the value of the integral. 
\[\int^8_4 \frac{x}{\sqrt{x^2-15}}\d x\]

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >
For the integral
\[\int_4^8 \frac{x}{\sqrt{x^2 - 15}}\d x\]
We first need to find the antiderivative 
\[\int \frac{x}{\sqrt {x^2 - 15}}\d x\]
Make the substitution $u = x^2 - 15$, and  $\d u = 2x\d x$ to obtain
\begin{eqnarray*}
\int \frac{x}{\sqrt {x^2 - 15}}\d x &=& \frac{1}{2}\int u^{-1/2}\d u  \\
&=& \sqrt u  \\
&=& \sqrt {x^2 - 15} \\
\end{eqnarray*}
Now evaluating the antiderivative at both end points:
\begin{eqnarray*}
\int_4^8 \frac{x}{\sqrt {x^2 - 15}}\d x  &=& \left. \left( \sqrt {x^2 - 15} \right) \right|_4^8 \\
&=& 7 - 1 \\
&=& 6\\
\end{eqnarray*}
The final answer becomes
\[\int_4^8 \frac{x}{\sqrt {x^2 - 15}}\d x = 6\]
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral
$$\int \frac{\cos\left(\log x\right)}{x} dx$$

<div class="answerBox">
<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer" >
Make the substitution $u = \log x$ so that we get 
$$\int \frac{\cos\left(\log x\right)}{x} dx = \int \cos u du = \sin u + C$$
Substituting back in our original expression, we find that 
$$\int \frac{\cos\left(\log x\right)}{x} dx = \sin \log x + C$$
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral. $$\int 2e^x \sin (e^x) dx$$

<div class="answerBox">
<button onclick="myFunction('answer6')" class="answerButton">Show Answer</button>
<div  id="answer6" class="answer" >
Make the substitution $u = e^x$ to find
$$\int 2\sin u du = -2\cos u +C$$
Substituting back in terms of $x$, we find 
$$\int 2e^x \sin (e^x) dx = -2\cos(e^x)$$
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral. 
\[\int\frac{e^{2x}}{1+e^{4x}}\d x\]

<div class="answerBox">
<button onclick="myFunction('answer7')" class="answerButton">Show Answer</button>
<div  id="answer7" class="answer" >
For the integral
\[\int \frac{e^{2x}}{1 + e^{4x}}\d x \]
We make the substitution $u = e^{2x}$, and $\d u = 2e^{2x}\d x$. The integral then becomes
\begin{eqnarray*}
\int \frac{e^{2x}}{1 + e^{4x}}\d x  &=& \frac{1}{2}\int \frac{1}{1 + u^2} \d u \\
&=& \frac{1}{2}\arctan u + C \\
&=& \frac{1}{2}\arctan (e^{2x}) + C
\end{eqnarray*}
The final answer is then
\[ \int \frac{e^{2x}}{1 + e^{4x}}\d x  = \frac{1}{2}\arctan (e^{2x}) + C\]
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral. 
\[\int \frac{2x-7}{x^2+1} \d x\]

<div class="answerBox">
<button onclick="myFunction('answer8')" class="answerButton">Show Answer</button>
<div  id="answer8" class="answer" >
We split the integral up into the sum of two fractions, both of which are easy to evaluate:
\begin{eqnarray*}
\int \frac{2x - 7}{x^2 + 1}\d x &=& \int \frac{2x}{x^2 + 1} - \frac{7}{x^2 + 1}\d x \\
&=& \log (x^2 + 1) - 7\arctan x + C
\end{eqnarray*}
The final answer is then
\[\int \frac{2x - 7}{x^2 + 1}\d x = \log (x^2 + 1) - 7\arctan x + C \]
</div>
</div>
</div>
</li>


<li><div class="exercise"> Compute the value of the integral. 
\[\int^9_4 \frac{1-\sqrt{x}}{1+\sqrt{x}}  \d x\]

<div class="answerBox">
<button onclick="myFunction('answer9')" class="answerButton">Show Answer</button>
<div  id="answer9" class="answer" >
\[\int_4^9 \frac{1 - \sqrt{x}}{1 + \sqrt{x}}\d x \]
We first find an antiderivative.
\begin{eqnarray*}
\int \frac{1 - \sqrt{x}}{1 + \sqrt{x}}\d x &=& \int \frac{1 + \sqrt{x} - 2\sqrt{x}}{1 + \sqrt{x}}\d x \\
& =& \int 1 - \frac{2\sqrt{x}}{1 + \sqrt {x}} \d x \\
\end{eqnarray*}
\begin{equation} \label{int3.1} \int \frac{1 - \sqrt {x} }{1 + \sqrt {x} }\d x  = x - 2\int \frac{\sqrt {x}}{1 + \sqrt {x}} \d x \end{equation}
Consider the remaining integral
\[\int \frac{\sqrt{x}}{1 + \sqrt{x} }\d x. \]
Make the substitution $u = 1 + \sqrt{x}$, which gives $ \d u = \frac{{\d x}}{2\sqrt{x}}$, or, rearranging, $\d x = 2(u - 1)\d u$. We then have the integral
\begin{eqnarray*}
\int \frac{\sqrt{x}}{1 + \sqrt{x}}\d x &=& \int \frac{2(u - 1)^2}{u}\d u \\
&=& 2 \int \frac{u^2 - 2u + 1}{u} \d u \\
&=& 2\int u - 2 + \frac{1}{u}\d u \\
&=& 2\left( \frac{u^2}{2} - 2u + \log u \right)  \\
&=& (1 + \sqrt{x} )^2 - 4(1 + \sqrt{x} ) + 2\log (1 + \sqrt{x} )
\end{eqnarray*}
Then, plugging this result into equation \eqref{int3.1}:
\begin{eqnarray*}
\int \frac{1 - \sqrt{x}}{1 + \sqrt{x}}\d x  &=& x - 2\left[ (1 + \sqrt{x})^2- 4(1 + \sqrt{x}) + 2\log (1 + \sqrt{x} )\right] \\
&=& - x + 6 + 4\sqrt{x}  - 4\log (1 + \sqrt{x})
\end{eqnarray*}
Now that we have the antiderivative, we can evaluate it at the two endpoints:
\begin{eqnarray*}
 \int_4^9 \frac{1 - \sqrt{x}}{1 + \sqrt{x}}\d x  &=& \left. \left(- x + 6 + 4\sqrt{x}  - 4\log (1 + \sqrt{x}) \right) \right|_4^9 \\
 &=& 4\log (3/4) - 1
 \end{eqnarray*}
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral. 
\[\int\frac{e^x - 1}{e^x + 1} \d x\]

<div class="answerBox">
<button onclick="myFunction('answer10')" class="answerButton">Show Answer</button>
<div  id="answer10" class="answer" >
\begin{eqnarray*}
\int \frac{e^x - 1}{e^x + 1}\d x &=&  - \int \frac{1 - e^x}{e^x + 1}\d x \\
&=&  - \int \frac{1 + e^x}{e^x + 1} - \frac{2e^x}{e^x + 1}\d x \\
&=&  - \int 1 -\frac{2e^x}{e^x + 1} \d x\\
&=&  - x + 2\int \frac{e^x}{e^x + 1} \d x \\
&=&  - x + 2\log (e^x + 1) + C \\
&=& 2\log (e^x + 1) - x + C\\
\end{eqnarray*}
Thus
\[\int \frac{e^x - 1}{e^x + 1} \d x = 2\log (e^x + 1) - x + C\]
</div>
</div>
</div>
</li>

<li><div class="exercise"> Evaluate the integral. 
$$\int\frac{1}{1-\sin(x/2)}dx$$

<div class="answerBox">
<button onclick="myFunction('answer11')" class="answerButton">Show Answer</button>
<div  id="answer11" class="answer" >
We will need to multiply by the conjugate to solve this problem:
\begin{eqnarray*}
\int \frac{1}{1-\sin (x/2)}dx &=& \int \frac{1 + \sin (x/2)}{1 - \sin^2(x/2)}dx \\
&=& \int \frac{1 + \sin (x/2)}{\cos^2(x/2)}dx \\
&=& \int \sec^2\left(\frac{x}{2}\right) + \tan\left(\frac{x}{2}\right)\sec\left(\frac{x}{2}\right)dx \\
&=& 2\left(\tan\left(\frac{x}{2}\right)  + \sec\left(\frac{x}{2}\right)\right) + C
\end{eqnarray*}
The final answer is then
$$\int \frac{1}{1 - \sin (x/2)}dx = 2\left(\tan\left(\frac{x}{2}\right) + \sec\left(\frac{x}{2}\right)\right) + C$$
</div>
</div>
</div>
</li>

<li><div class="exercise"> Evaluate the integral. 
\[\int\frac{\cos 2x}{\sin^2(2x) + 8}\d x\]

<div class="answerBox">
<button onclick="myFunction('answer12')" class="answerButton">Show Answer</button>
<div  id="answer12" class="answer" >
For the integral
\[ \int \frac{\cos 2x}{\sin^2(2x) + 8} \d x \]
We make the substitution $u = \sin 2x$, so the differential is $\d u = 2\cos2x\,\d x$. 
\begin{eqnarray*}
\int \frac{\cos 2x}{\sin^2 2x + 8} \d x &=& \frac{1}{2}\int \frac{1}{u^2+ 8}\d u  \\
&=& \frac{1}{16}\int \frac{1}{\left( \frac{u}{2\sqrt{2}} \right)^2 + 1} \d u 
\end{eqnarray*}
Now with this integral, make the substitution $w = \frac{u}{2\sqrt{2}}$, and $\d u = 2\sqrt 2 \d w$, to easily evaluate the integral:
\begin{eqnarray*}
\frac{1}{16}\int \frac{1}{\left( \frac{u}{2\sqrt{2} }\right)^2 + 1} \d u &=& \frac{\sqrt{2}}{8}\int \frac{1}{1 + w^2}\d w \\
&=& \frac{\sqrt{2}}{8}\arctan w + C \\
&=& \frac{\sqrt{2}}{8}\arctan \left(\frac{\sin 2x}{2\sqrt{2}} \right) + C
\end{eqnarray*}
</div>
</div>
</div>
</li>


<li><div class="exercise"> Compute the value of the integral. 
\[\int^{\pi}_0 \frac{\sin x}{\cos^2x - 6\cos x + 13}\d x\]

<div class="answerBox">
<button onclick="myFunction('answer13')" class="answerButton">Show Answer</button>
<div  id="answer13" class="answer" >
\[\int_0^\pi \frac{\sin x}{\cos^2x - 6\cos x + 13} \d x\]
First we find an antiderivative by making a $u$ substitution. For the integral
\[ \int \frac{\sin x}{\cos^2x - 6\cos x + 13}\d x \]
Make the substitution $u = \cos x$, and $\d u =  - \sin x\d x$. This yields the integral
\begin{eqnarray*}
\int \frac{\sin x}{\cos^2x - 6\cos x + 13}\d x &=&  - \int \frac{1}{u^2 - 6u + 13}\d u\\
&=&  - \int \frac{1}{(u - 3)^2 + 4}\d u \\
&=&  - \frac{1}{4}\int \frac{1}{\left( \frac{u - 3}{2} \right)^2 + 1}\d u 
\end{eqnarray*}
Now with this integral, we make the substitution $\frac{u - 3}{2}  = w$ and $2\d w =  \d u$. The we have the integral
\begin{eqnarray*}
- \frac{1}{4}\int \frac{1}{\left( \frac{u - 3}{2} \right)^2 + 1} \d u&=&  - \frac{1}{2}\int \frac{1}{1 + w^2}\d w \\
&=&  - \frac{1}{2}\arctan w 
\end{eqnarray*}
Now substitution in the original variables:
\[- \frac{1}{2}\arctan \left( \frac{\cos x - 3}{2} \right) \]
Now we evaluate at the endpoints:
\[\left. \left(- \frac{1}{2}\arctan \left(\frac{\cos x - 3}{2} \right) \right) \right|_0^\pi  \]
This yields the final answer:
\[\frac{1}{2}\left(\arctan 2 - \frac{\pi}{4} \right)\]
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral. \[\int \frac{1}{x+x^{1/3}} \d x\]

<div class="answerBox">
<button onclick="myFunction('answer14')" class="answerButton">Show Answer</button>
<div  id="answer14" class="answer" >
Let $x = z^3$, and $\d x = 3z^2\d z$. Making these substitutions yields
\begin{eqnarray*}
\int \frac{1}{z^3 + z}3z^2\d z &=& 3\int \frac{z}{z^2 + 1}\d z \\
&=& \frac{3}{2}\log (z^2 + 1)  + C  \\
&=& \frac{3}{2}\log (x^{2/3} + 1) + C\\
\end{eqnarray*}
Thus the final answer is
\[ \int \frac{1}{x + x^{1/3}}\d x  = \frac{3}{2}\log (x^{2/3} + 1) + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. \[\int x^3 \sqrt{a^2-x^2} \d x\]

<div class="answerBox">
<button onclick="myFunction('answer15')" class="answerButton">Show Answer</button>
<div  id="answer15" class="answer" >
Let $u = a^2 - x^2$ and $\d u =  - 2x\d x$.
\begin{eqnarray*}
\int x^3\sqrt{a^2 - x^2} \d x  &=&  - \frac{1}{2}\int x^2\sqrt{u} \d u \\
&=& \frac{1}{2}\int (u -a^2)\sqrt{u} \d u \\
 &=& \frac{1}{2}\int u^{3/2} - a^2\sqrt{u} \d u  \\
 &=& \frac{1}{2}\left( \frac{2}{5}u^{5/2} - \frac{2}{3}a^2u^{3/2} \right) + C\\
 &=& \frac{1}{5}(a^2 - x^2)^{5/2} - \frac{a^2}{3}(a^2 - x^2)^{3/2} + C
\end{eqnarray*}
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral. \[\int \sqrt{1-\cos x} \d x\]

<div class="answerBox">
<button onclick="myFunction('answer16')" class="answerButton">Show Answer</button>
<div  id="answer16" class="answer" >
Use the double angle identity
$$1 - \cos 2x = 2\sin ^2x \Rightarrow 1 - \cos x = 2\sin ^2\left( \frac{x}{2} \right)$$
\begin{eqnarray*}
\int \sqrt{1 - \cos x} \d x &=& \int \sqrt{2\sin^2\left( \frac{x}{2} \right)} \d x\\ 
&=& \sqrt2 \int \sin \left( \frac{x}{2} \right) \d x \\
&=&  - 2\sqrt2 \cos \left( \frac{x}{2} \right) + C\\
\end{eqnarray*}
$$\int \sqrt{1 - \cos x} \d x  =  - 2\sqrt2 \cos \left( \frac{x}{2} \right) + C$$
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral
\[\int\frac{\sqrt{1+\sqrt{x}}}{\sqrt{x}}\d x\]

<div class="answerBox">
<button onclick="myFunction('answer17')" class="answerButton">Show Answer</button>
<div  id="answer17" class="answer" >
Let $u = 1+ \sqrt{x}$, and $2\d u = \frac{1}{\sqrt{x}} \d x$. Then the integral becomes
\[\int\frac{\sqrt{1+\sqrt{x}}}{\sqrt{x}}\d x = 2\int\sqrt{u} \d u\]
This integral is easily evaluated
\[ 2\int\sqrt{u} \d u = \frac{4}{3}u^{3/2} + C \]
Now changing to the original variables, 
\[\int\frac{\sqrt{1+\sqrt{x}}}{\sqrt{x}}\d x = \frac{4}{3}(1+\sqrt{x})^{3/2} + C\]
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral. \[\int \frac{2x-3}{x^2+6x+13} \d x\]

<div class="answerBox">
<button onclick="myFunction('answer18')" class="answerButton">Show Answer</button>
<div  id="answer18" class="answer" >
We will split this integral up so that part of it can be evaluated as a logarithm:
\begin{eqnarray*}
\int \frac{2x - 3}{x^2 + 6x + 13}\d x  &=& \int \frac{2x + 6 - 9}{x^2 + 6x + 13}\d x \\
&=& \int \frac{2x + 6}{x^2 + 6x + 13}\d x - \int \frac{9}{x^2 + 6x + 9 + 4}\d x \\
&=& \log \left| x^2 + 6x + 13 \right| - 9\int \frac{1}{(x + 3)^2 + 4}\d x \\
\end{eqnarray*}
To evaluate the second integral, \[9\int \frac{1}{(x + 3)^2+ 4}\d x\]
we need to make the substitution $x + 3 = 2\tan z$, and $\d x = 2\sec^2z\d z$. Thus
\[9\int \frac{1}{(x + 3)^2+ 4}\d x =\frac{9}{2}\int 1\d z = \frac{9z}{2} = \frac{9}{2}\arctan \left( \frac{x + 3}{2}\right)\]
The final answer is then 
\[\int \frac{2x-3}{x^2+6x+13} \d x = \log \left| {x^2 + 6x + 13} \right| - \frac{9}{2}\arctan \left( \frac{x + 3}{2} \right) + C\]
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral. \[\int \csc(2x) \d x\]

<div class="answerBox">
<button onclick="myFunction('answer19')" class="answerButton">Show Answer</button>
<div  id="answer19" class="answer" >
\begin{eqnarray*}
\int \csc (2x)\d x  &=& \int \frac{1}{\sin (2x)}\d x \\
 &=& \int \frac{1}{2\sin (x)\cos (x)}\d x  \\
 &=& \int \frac{\cos (x)}{2\sin (x)\cos^2(x)}\d x  \\
 &=& \frac{1}{2} \int \frac{\sec^2(x)}{\tan (x)} \d x\\
&=&\frac{1}{2}\log \left| \tan x \right| + C\\
\end{eqnarray*}
The final answer is then
\[\int \csc (2x)\d x  = \frac{1}{2}\log \left| \tan x \right| + C\]
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral \[\int \frac{2x+3}{9x^2-12x + 8} \d x\]

<div class="answerBox">
<button onclick="myFunction('answer20')" class="answerButton">Show Answer</button>
<div  id="answer20" class="answer" >
\begin{eqnarray*}
\int \frac{2x + 3}{9x^2 - 12x + 8}\d x  &=& \frac{1}{9}\int \frac{18x + 27}{9x^2 - 12x + 8}  \d x\\
&=& \frac{1}{9}\int \left( \frac{18x - 12}{9x^2 - 12x + 8} + \frac{39}{(3x - 2)^2 + 4}\right)\d x \\
\end{eqnarray*}
Let $ 3x - 2 = 2z$, and $3\d x = 2\d z$. 
\begin{eqnarray*}
\frac{1}{9}\int \left(\frac{18x - 12}{9x^2 - 12x + 8} + \frac{39}{(3x - 2)^2 + 4}\right)\d x  &=& \frac{1}{9}\log \left| 9x^2 - 12x + 8 \right| + \frac{1}{18}\int \frac{13}{z^2 + 1}\d z \\
 &=& \frac{1}{9}\log \left| 9x^2 - 12x + 8 \right| + \frac{13}{18}\arctan (z) + C\\
 &=& \frac{1}{9}\log \left| 9x^2 - 12x + 8 \right| + \frac{13}{18}\arctan \left( \frac{3x - 2}{2} \right) + C
\end{eqnarray*}
</div>
</div>
</div>
</li>


</ol>
