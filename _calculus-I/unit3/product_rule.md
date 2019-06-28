---
layout: lesson
title: The Product Rule
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

### Introduction
In this section, we will learn how to compute derivatives if there are two functions multiplied together, for example $f(x) = x\sin x$. The product rule is not as simple as the sum rule which we have seen so far, but is intuitive if one thinks about it the right way. We will start simply with what the product rule is, and then have a discussion on the intuition behind it later. 

### Theorem and Derivation

<div class="theorem">
<b>Theorem:</b> Let $f(x)$ and $g(x)$ each be differentiable functions. Then, their derivative is 
$$\frac{d}{dx}\left[f(x)g(x)\right] = \frac{df}{dx} g(x) + f(x) \frac{dg}{dx}$$
</div>

For the proof, we will use the definition of the derivative. 

<div class="proof">
<b>Proof:</b> 
$$\begin{eqnarray*}
(f(x)g(x))' &=& \lim_{h\to 0} \frac{f(x+h)g(x+h) - f(x)g(x)}{h} \\
&=& \lim_{h\to 0} \frac{f(x+h)g(x+h) - f(x)g(x+h) + f(x)g(x+h) - f(x)g(x)}{h} \\
&=& \lim_{h\to 0} \frac{f(x+h)g(x+h) - f(x)g(x+h)}{h}  + \lim_{h\to 0} \frac{f(x)g(x+h) - f(x)g(x)}{h} \\
&=& \lim_{h\to 0} \frac{g(x+h)[f(x+h) - f(x)]}{h}  + \lim_{h\to 0} \frac{f(x)[g(x+h) - g(x)]}{h} \\
&=& \lim_{h\to 0}g(x+h) \lim_{h\to 0} \frac{f(x+h) - f(x)}{h}  + f(x) \lim_{h\to 0} \frac{g(x+h) - g(x)}{h} \\
&=& \frac{df}{dx}g(x) + f(x)\frac{dg}{dx}
\end{eqnarray*}$$
</div>

### Examples
Now, let's proceed with some examples of the product rule. 

$$f(x) = x\sin x$$


