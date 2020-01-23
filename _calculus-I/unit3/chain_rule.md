---
layout: lesson
title: Chain Rule
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

The chain rule is used for finding the derivative of nested functions. For example, if we have a function of the form

$$y = \sin(e^x),$$

how would we calculate its derivative? That is the aim of this section. In general terms, we want to calculate the derivative of $y = f(g(x))$. In the previous example, $f(x) = \sin x$ and $g(x) = e^x$. 

<div class="theorem">
Chain Rule: If $f(x)$ and $g(x)$ are continuous functions, the derivative of $y = f(g(x))$ is
$$\frac{dy}{dx} = f'(g(x))g'(x).$$
</div>

Let us now prove this by using the definition of the derivative. 

<div class="proof">
To prove the above formula, we need to start from the definition of the derivative. 

\begin{align*}
y'(x) =& \lim_{h\to 0}\frac{f(g(x+h)) - f(g(x))}{h}\\\
=& \lim_{h\to 0}\frac{f(g(x+h)) - f(g(x))}{h}\frac{g(x+h) - g(x)}{g(x+h) - g(x)}\\
=& \lim_{h\to 0}\frac{f(g(x+h)) - f(g(x))}{g(x+h) - g(x)}\frac{g(x+h) - g(x)}{h}
\end{align*}

The second factor is simply $g'(x)$.
</div>

### Examples
Now let's work some examples of the chain rule. 

<div class="example">


</div>
