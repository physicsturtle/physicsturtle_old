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
\int x^n dx &=& \frac{x^{n+1}}{n+1} ,\qquad (n\not=-1)\\
\int \sin x dx &=& -\cos x \\
\int \cos x dx &=& \sin x \\
\int \frac{dx}{1+x^2} &=& \arctan x \\
\int e^x dx &=& e^x \\
\int \frac{dx}{x} &=& \log|x| 
\end{eqnarray*}$$

Armed with these formulas, you should be equipped to solve the following exercises. Also make sure that you keep your trigonometric identities in mind. Some of these integrals may seem quite complicated at first, but by using a trigonometric identity they are substantially simplified.

<ol>
<li><div class="exercise">
Compute the value of the integral. 
$$\int^8_4 \frac{x}{\sqrt{x^2-15}}dx$$

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
For the integral
$$\int_4^8 \frac{x}{\sqrt{x^2 - 15}}dx$$
We first need to find the antiderivative 
$$\int \frac{x}{\sqrt {x^2 - 15}}dx$$
Make the substitution $u = x^2 - 15$, and  $du = 2xdx$ to obtain
\begin{eqnarray*}
\int \frac{x}{\sqrt {x^2 - 15}}dx &=& \frac{1}{2}\int u^{-1/2}du  \\
&=& \sqrt u  \\
&=& \sqrt {x^2 - 15} \\
\end{eqnarray*}
Now evaluating the antiderivative at both end points:
\begin{eqnarray*}
\int_4^8 \frac{x}{\sqrt {x^2 - 15}}dx  &=& \left. \left( \sqrt {x^2 - 15} \right) \right|_4^8 \\
&=& 7 - 1 \\
&=& 6\\
\end{eqnarray*}
The final answer becomes
$$\int_4^8 \frac{x}{\sqrt {x^2 - 15}}dx = 6$$
</div>
</div>
</div>
</li>


<li><div class="exercise">If $x = 6\cos \theta$, $y = 2\sin \theta$, compute the value of the integral. 
$$\int^6_3 xy dx$$

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
For the integral $$\int_3^6 xy dx$$
since $x = 6\cos \theta$ and $y = 2\sin \theta$, we can compute $dx =  - 6\sin \theta d\theta$. Since the bounds are from $x = 3$ to $x = 6$, the equivalent $\theta$ that accomplish this are $\theta = \pi/3$ to $\theta = 0$.
\begin{eqnarray*}
\int_{\pi /3}^0 (6\cos \theta )(2\sin \theta )(-6\sin \theta )d\theta &=&  - 72\int_{\pi /3}^0 \sin^2\theta \cos \theta d\theta \\
&=& 72\left. \frac{\sin^3\theta}{3} \right|_0^{\pi /3} \\
&=& 24\left(\frac{\sqrt{3}}{2}\right)^3 \\
&=& 9\sqrt{3}
\end{eqnarray*}
$$\int_3^6 xydx  = 9\sqrt{3}$$
</div>
</div>
</div>
</li>



<li><div class="exercise">Evaluate the integral. 
$$\int\frac{e^{2x}}{1+e^{4x}}dx$$

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >
For the integral
$$\int \frac{e^{2x}}{1 + e^{4x}}dx $$
We make the substitution $u = e^{2x}$, and $du = 2e^{2x}dx$. The integral then becomes
\begin{eqnarray*}
\int \frac{e^{2x}}{1 + e^{4x}}dx  &=& \frac{1}{2}\int \frac{1}{1 + u^2} du \\
&=& \frac{1}{2}\arctan u + C \\
&=& \frac{1}{2}\arctan (e^{2x}) + C
\end{eqnarray*}
The final answer is then
$$ \int \frac{e^{2x}}{1 + e^{4x}}dx  = \frac{1}{2}\arctan (e^{2x}) + C$$
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. 
$$\int \frac{2x-7}{x^2+1} dx$$

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer" >
We split the integral up into the sum of two fractions, both of which are easy to evaluate:
\begin{eqnarray*}
\int \frac{2x - 7}{x^2 + 1}dx &=& \int \frac{2x}{x^2 + 1} - \frac{7}{x^2 + 1}dx \\
&=& \log (x^2 + 1) - 7\arctan x + C
\end{eqnarray*}
The final answer is then
$$\int \frac{2x - 7}{x^2 + 1}dx = \log (x^2 + 1) - 7\arctan x + C $$
</div>
</div>
</div>
</li>




<li><div class="exercise"> Compute the value of the integral. 
$$\int^9_4 \frac{1-\sqrt{x}}{1+\sqrt{x}}  dx$$

<div class="answerBox">
<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer" >
$$\int_4^9 \frac{1 - \sqrt{x}}{1 + \sqrt{x}}dx $$
We first find an antiderivative.
\begin{eqnarray*}
\int \frac{1 - \sqrt{x}}{1 + \sqrt{x}}dx &=& \int \frac{1 + \sqrt{x} - 2\sqrt{x}}{1 + \sqrt{x}}dx \\
& =& \int 1 - \frac{2\sqrt{x}}{1 + \sqrt {x}} dx \\
\end{eqnarray*}
\begin{equation} \label{int3.1} \int \frac{1 - \sqrt {x} }{1 + \sqrt {x} }dx  = x - 2\int \frac{\sqrt {x}}{1 + \sqrt {x}} dx \end{equation}
Consider the remaining integral
$$\int \frac{\sqrt{x}}{1 + \sqrt{x} }dx. $$
Make the substitution $u = 1 + \sqrt{x}$, which gives $ du = \frac{{dx}}{2\sqrt{x}}$, or, rearranging, $dx = 2(u - 1)du$. We then have the integral
\begin{eqnarray*}
\int \frac{\sqrt{x}}{1 + \sqrt{x}}dx &=& \int \frac{2(u - 1)^2}{u}du \\
&=& 2 \int \frac{u^2 - 2u + 1}{u} du \\
&=& 2\int u - 2 + \frac{1}{u}du \\
&=& 2\left( \frac{u^2}{2} - 2u + \log u \right)  \\
&=& (1 + \sqrt{x} )^2 - 4(1 + \sqrt{x} ) + 2\log (1 + \sqrt{x} )
\end{eqnarray*}
Then, plugging this result into equation \eqref{int3.1}:
\begin{eqnarray*}
\int \frac{1 - \sqrt{x}}{1 + \sqrt{x}}dx  &=& x - 2\left[ (1 + \sqrt{x})^2- 4(1 + \sqrt{x}) + 2\log (1 + \sqrt{x} )\right] \\
&=& - x + 6 + 4\sqrt{x}  - 4\log (1 + \sqrt{x})
\end{eqnarray*}
Now that we have the antiderivative, we can evaluate it at the two endpoints:
\begin{eqnarray*}
\int_4^9 \frac{1 - \sqrt{x}}{1 + \sqrt{x}}dx  &=& \left. \left(- x + 6 + 4\sqrt{x}  - 4\log (1 + \sqrt{x}) \right) \right|_4^9 \\
&=& 4\log (3/4) - 1
\end{eqnarray*}
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral. 
$$\int\frac{e^x - 1}{e^x + 1} dx$$

<div class="answerBox">
<button onclick="myFunction('answer6')" class="answerButton">Show Answer</button>
<div  id="answer6" class="answer" >
\begin{eqnarray*}
\int \frac{e^x - 1}{e^x + 1}dx &=&  - \int \frac{1 - e^x}{e^x + 1}dx \\
&=&  - \int \frac{1 + e^x}{e^x + 1} - \frac{2e^x}{e^x + 1}dx \\
&=&  - \int 1 -\frac{2e^x}{e^x + 1} dx\\
&=&  - x + 2\int \frac{e^x}{e^x + 1} dx \\
&=&  - x + 2\log (e^x + 1) + C \\
&=& 2\log (e^x + 1) - x + C\\
\end{eqnarray*}
Thus
$$\int \frac{e^x - 1}{e^x + 1} dx = 2\log (e^x + 1) - x + C$$
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. 
$$\int\frac{1}{1-\sin(x/2)}dx$$

<div class="answerBox">
<button onclick="myFunction('answer7')" class="answerButton">Show Answer</button>
<div  id="answer7" class="answer" >
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




<li><div class="exercise">Evaluate the integral. 
$$\int\frac{\cos 2x}{\sin^2(2x) + 8}dx$$

<div class="answerBox">
<button onclick="myFunction('answer8')" class="answerButton">Show Answer</button>
<div  id="answer8" class="answer" >
For the integral
$$ \int \frac{\cos 2x}{\sin^2(2x) + 8} dx $$
We make the substitution $u = \sin 2x$, so the differential is $du = 2\cos2x\,dx$. 
\begin{eqnarray*}
\int \frac{\cos 2x}{\sin^2 2x + 8} dx &=& \frac{1}{2}\int \frac{1}{u^2+ 8}du  \\
&=& \frac{1}{16}\int \frac{1}{\left( \frac{u}{2\sqrt{2}} \right)^2 + 1} du 
\end{eqnarray*}
Now with this integral, make the substitution $w = \frac{u}{2\sqrt{2}}$, and $du = 2\sqrt 2 dw$, to easily evaluate the integral:
\begin{eqnarray*}
\frac{1}{16}\int \frac{1}{\left( \frac{u}{2\sqrt{2} }\right)^2 + 1} du &=& \frac{\sqrt{2}}{8}\int \frac{1}{1 + w^2}dw \\
&=& \frac{\sqrt{2}}{8}\arctan w + C \\
&=& \frac{\sqrt{2}}{8}\arctan \left(\frac{\sin 2x}{2\sqrt{2}} \right) + C
\end{eqnarray*}
</div>
</div>
</div>
</li>




<li><div class="exercise">Compute the value of the integral. 
$$\int^{\pi}_0 \frac{\sin x}{\cos^2x - 6\cos x + 13}dx$$

<div class="answerBox">
<button onclick="myFunction('answer9')" class="answerButton">Show Answer</button>
<div  id="answer9" class="answer" >
$$\int_0^\pi \frac{\sin x}{\cos^2x - 6\cos x + 13} dx$$
First we find an antiderivative by making a $u$ substitution. For the integral
$$ \int \frac{\sin x}{\cos^2x - 6\cos x + 13}dx $$
Make the substitution $u = \cos x$, and $du =  - \sin xdx$. This yields the integral
\begin{eqnarray*}
\int \frac{\sin x}{\cos^2x - 6\cos x + 13}dx &=&  - \int \frac{1}{u^2 - 6u + 13}du\\
&=&  - \int \frac{1}{(u - 3)^2 + 4}du \\
&=&  - \frac{1}{4}\int \frac{1}{\left( \frac{u - 3}{2} \right)^2 + 1}du 
\end{eqnarray*}
Now with this integral, we make the substitution $\frac{u - 3}{2}  = w$ and $2dw =  du$. The we have the integral
\begin{eqnarray*}
- \frac{1}{4}\int \frac{1}{\left( \frac{u - 3}{2} \right)^2 + 1} du&=&  - \frac{1}{2}\int \frac{1}{1 + w^2}dw \\
&=&  - \frac{1}{2}\arctan w 
\end{eqnarray*}
Now substitution in the original variables:
$$- \frac{1}{2}\arctan \left( \frac{\cos x - 3}{2} \right) $$
Now we evaluate at the endpoints:
$$\left. \left(- \frac{1}{2}\arctan \left(\frac{\cos x - 3}{2} \right) \right) \right|_0^\pi  $$
This yields the final answer:
$$\frac{1}{2}\left(\arctan 2 - \frac{\pi}{4} \right)$$
</div>
</div>
</div>
</li>



<li><div class="exercise">Evaluate the integral
$$\int \frac{\cos\left(\log x\right)}{x} dx$$

<div class="answerBox">
<button onclick="myFunction('answer10')" class="answerButton">Show Answer</button>
<div  id="answer10" class="answer" >
Make the substitution $u = \log x$ so that we get 
$$\int \frac{\cos\left(\log x\right)}{x} dx = \int \cos u du = \sin u + C$$
Substituting back in our original expression, we find that 
$$\int \frac{\cos\left(\log x\right)}{x} dx = \sin \log x + C$$
</div>
</div>
</div>
</li>



<li><div class="exercise">Evaluate the integral. $$\int 2e^x \sin (e^x) dx$$

<div class="answerBox">
<button onclick="myFunction('answer11')" class="answerButton">Show Answer</button>
<div  id="answer11" class="answer" >
Make the substitution $u = e^x$ to find
$$\int 2\sin u du = -2\cos u +C$$
Substituting back in terms of $x$, we find 
$$\int 2e^x \sin (e^x) dx = -2\cos(e^x)$$
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral. $$\int \sqrt{1-\cos x} dx$$

<div class="answerBox">
<button onclick="myFunction('answer12')" class="answerButton">Show Answer</button>
<div  id="answer12" class="answer" >
Use the double angle identity
$$1 - \cos 2x = 2\sin ^2x \Rightarrow 1 - \cos x = 2\sin ^2\left( \frac{x}{2} \right)$$
\begin{eqnarray*}
\int \sqrt{1 - \cos x} dx &=& \int \sqrt{2\sin^2\left( \frac{x}{2} \right)} dx\\ 
&=& \sqrt2 \int \sin \left( \frac{x}{2} \right) dx \\
&=&  - 2\sqrt2 \cos \left( \frac{x}{2} \right) + C\\
\end{eqnarray*}
$$\int \sqrt{1 - \cos x} dx  =  - 2\sqrt2 \cos \left( \frac{x}{2} \right) + C$$
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral
$$\int\frac{\sqrt{1+\sqrt{x}}}{\sqrt{x}}dx$$

<div class="answerBox">
<button onclick="myFunction('answer13')" class="answerButton">Show Answer</button>
<div  id="answer13" class="answer" >
Let $u = 1+ \sqrt{x}$, and $2du = \frac{1}{\sqrt{x}} dx$. Then the integral becomes
$$\int\frac{\sqrt{1+\sqrt{x}}}{\sqrt{x}}dx = 2\int\sqrt{u} du$$
This integral is easily evaluated
$$ 2\int\sqrt{u} du = \frac{4}{3}u^{3/2} + C $$
Now changing to the original variables, 
$$\int\frac{\sqrt{1+\sqrt{x}}}{\sqrt{x}}dx = \frac{4}{3}(1+\sqrt{x})^{3/2} + C$$
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. $$\int \csc(2x) dx$$

<div class="answerBox">
<button onclick="myFunction('answer14')" class="answerButton">Show Answer</button>
<div  id="answer14" class="answer" >
\begin{eqnarray*}
\int \csc (2x)dx  &=& \int \frac{1}{\sin (2x)}dx \\
&=& \int \frac{1}{2\sin (x)\cos (x)}dx  \\
&=& \int \frac{\cos (x)}{2\sin (x)\cos^2(x)}dx  \\
&=& \frac{1}{2} \int \frac{\sec^2(x)}{\tan (x)} dx\\
&=&\frac{1}{2}\log \left| \tan x \right| + C\\
\end{eqnarray*}
The final answer is then
$$\int \csc (2x)dx  = \frac{1}{2}\log \left| \tan x \right| + C$$
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. $$\int \frac{1}{x+x^{1/3}} dx$$

<div class="answerBox">
<button onclick="myFunction('answer15')" class="answerButton">Show Answer</button>
<div  id="answer15" class="answer" >
Let $x = z^3$, and $dx = 3z^2dz$. Making these substitutions yields
\begin{eqnarray*}
\int \frac{1}{z^3 + z}3z^2dz &=& 3\int \frac{z}{z^2 + 1}dz \\
&=& \frac{3}{2}\log (z^2 + 1)  + C  \\
&=& \frac{3}{2}\log (x^{2/3} + 1) + C\\
\end{eqnarray*}
Thus the final answer is
$$ \int \frac{1}{x + x^{1/3}}dx  = \frac{3}{2}\log (x^{2/3} + 1) + C$$
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. $$\int x^3 \sqrt{a^2-x^2} dx$$

<div class="answerBox">
<button onclick="myFunction('answer16')" class="answerButton">Show Answer</button>
<div  id="answer16" class="answer" >
Let $u = a^2 - x^2$ and $du =  - 2xdx$.
\begin{eqnarray*}
\int x^3\sqrt{a^2 - x^2} dx  &=&  - \frac{1}{2}\int x^2\sqrt{u} du \\
&=& \frac{1}{2}\int (u -a^2)\sqrt{u} du \\
&=& \frac{1}{2}\int u^{3/2} - a^2\sqrt{u} du  \\
&=& \frac{1}{2}\left( \frac{2}{5}u^{5/2} - \frac{2}{3}a^2u^{3/2} \right) + C\\
&=& \frac{1}{5}(a^2 - x^2)^{5/2} - \frac{a^2}{3}(a^2 - x^2)^{3/2} + C
\end{eqnarray*}
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral $$\int \frac{2x+3}{9x^2-12x + 8} dx$$

<div class="answerBox">
<button onclick="myFunction('answer17')" class="answerButton">Show Answer</button>
<div  id="answer17" class="answer" >
\begin{eqnarray*}
\int \frac{2x + 3}{9x^2 - 12x + 8}dx  &=& \frac{1}{9}\int \frac{18x + 27}{9x^2 - 12x + 8}  dx\\
&=& \frac{1}{9}\int \left( \frac{18x - 12}{9x^2 - 12x + 8} + \frac{39}{(3x - 2)^2 + 4}\right)dx \\
\end{eqnarray*}
Let $ 3x - 2 = 2z$, and $3dx = 2dz$. 
\begin{eqnarray*}
\frac{1}{9}\int \left(\frac{18x - 12}{9x^2 - 12x + 8} + \frac{39}{(3x - 2)^2 + 4}\right)dx  &=& \frac{1}{9}\log \left| 9x^2 - 12x + 8 \right| + \frac{1}{18}\int \frac{13}{z^2 + 1}dz \\
&=& \frac{1}{9}\log \left| 9x^2 - 12x + 8 \right| + \frac{13}{18}\arctan (z) + C\\
&=& \frac{1}{9}\log \left| 9x^2 - 12x + 8 \right| + \frac{13}{18}\arctan \left( \frac{3x - 2}{2} \right) + C
\end{eqnarray*}
</div>
</div>
</div>
</li>

</ol>
