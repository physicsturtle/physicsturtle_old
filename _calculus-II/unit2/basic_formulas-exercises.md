---
layout: exercises
title: Basic Formulas - Exercises
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---

<ol> 
<li> <div class="exercise"> By using differentiation of trigonometric functions (other than sine and cosine), determine the antiderivatives of $f(x) = \sec^2 x$, $f(x) = \csc^2 x$, $f(x) = \sec x \tan x$, and $f(x) = \csc x \cot x$. 

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
    
We recognize these as the derivatives of $\tan x$, $-\cot x$, $\sec x$, and $-\csc x$. Thus, 

$$\begin{align*}
\int \sec^2 x dx =& \tan x \\
\int \csc^2 x dx =& -\cot x\\
\int \sec x \tan x dx =& \sec x\\
\int \csc x \cot x dx =& -\csc x
\end{align*}$$

</div>
</div>
</div>
</li>

<li><div class="exercise"> By using differentiation of certain inverse trigonometric functions, determine the antiderivative of 
$$f(x) = \frac{1}{\sqrt{1-x^2}}.$$

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >

We recognize this as the derivative of $\arcsin x$, that is, 

$$\frac{d}{dx}\arcsin x = \frac{1}{\sqrt{1-x^2}}.$$
This tells us that

$$\int\frac{1}{\sqrt{1-x^2}}dx = \arcsin x.$$

</div>
</div>
</div>
</li>

<li><div class="exercise"> By using differentiation of an exponential function, determine the antiderivative of $f(x) = a^x$, where $a$ is a positive constant. 

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >

Let's consider differentiating $a^x$. Doing this, we get

$$\frac{d}{dx}a^x = a^x \log a$$

If we divide both sides by $\log a$, then

$$\frac{d}{dx}\left(\frac{a^x}{\log a}\right) = a^x$$

which is in the form we want to get rid of the derivative sign, and add the integral sign to the other side! Thus, 

$$\int a^x dx = \frac{a^x}{\log a}$$

</div>
</div>
</div>
</li>

<li><div class="exercise"> Compute the value of the integral. 
\[\int_0^1 x \left( 1 - \sqrt{x} \right)^2 dx\]

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer" >

$$\begin{eqnarray*}
\int_0^1 x(1 - \sqrt{x})^2dx  &=& \int_0^1 x(1 - 2\sqrt{x}  + x)dx \\
&=& \int_0^1 x - 2x^{3/2} + x^2 dx \\
 &=& \left. \left( \frac{x^2}{2} - \frac{4x^{5/2}}{5} + \frac{x^3}{3} \right) \right|_0^1 \\
 &=& \frac{1}{30}\\
 \end{eqnarray*}$$
 
$$\int_0^1 x(1 - \sqrt{x})^2 dx = \frac{1}{30}$$

</div>
</div>
</div>
</li>

<li><div class="exercise"> If $x(t) = e^t\cos t$ and $y(t) = e^t\sin t$, compute the value of the integral. 
\[\int^3_2 \sqrt{\left(\frac{dx}{dt}\right)^2 + \left( \frac{dy}{dt} \right)^2} dt\]

<div class="answerBox">
<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer" >

First we compute the derivatives $x'$ and $y'$:

$$\begin{eqnarray*}
x'(t) = e^t(\cos t - \sin t)\\
y'(t) = e^t(\sin t + \cos t)
\end{eqnarray*}$$

Now plugging these results into the integral:

$$\begin{eqnarray*}
\int_2^3 \sqrt{\left( \frac{dx}{dt} \right)^2 + \left( \frac{dy}{dt} \right)^2} dt  &=& \int_2^3 \sqrt{\left( e^t(\cos t - \sin t)\right)^2 + \left( e^t(\sin t + \cos t) \right)^2} dt\\
 &=& \int_2^3 \sqrt{e^{2t}(\cos^2t - 2\cos t\sin t + \sin^2t + \sin^2t + 2\cos t\sin t + \cos^2t)} dt \\
&=& \int_2^3 \sqrt {2e^{2t}} dt\\
&=& \int_2^3 e^t \sqrt{2} dt \\
&=& \sqrt 2 \left. e^t \right|_2^3 \\
&=& \sqrt{2} e^2(e - 1)
\end{eqnarray*}$$

</div>
</div>
</div>
</li>

</ol>
