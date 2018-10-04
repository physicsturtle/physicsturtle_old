---
layout: lesson
title: DIRECTIONAL DERIVATIVE
course: calculus-III
unit: unit3
---

The partial derivatives represent the rate of change of a function in the \\(x\\) and \\(y\\) directions. It is also possible to calculate the rate of change of a function in any direction in the \\(xy\\) plane. This is called the directional derivative. Suppose we're interesting in calculating the derivative of a function \\(f(x,y)\\) in the direction of the *unit vector* \\(\hat{\textbf{u}}  = (a,b)\\). We define this as 

$$D_\hat{\textbf{u}}f = \lim_{h\to 0}\frac{f(x+ah,y+bh) - f(x,y)}{h}$$ 

How do we go about calculating this? Define the function \\(g(h) = f(x+ah,y+bh)\\). We then recognize that the formula defined above is actually 

$$D_\hat{\textbf{u}} f = \lim_{h\to 0}\frac{g(h) - g(0)}{h} = g'(0)$$

There is another way to calculate \\(g'(0)\\), and that is by the chain rule. The derivative of \\(g\\) is 

$$\begin{eqnarray}
g'(h) &=& \frac{\partial f}{\partial x}\frac{d}{dh}(x+ah) + \frac{\partial f}{\partial y}\frac{d}{dh}(y+bh)\\
&=& a\frac{\partial f}{\partial x} + b\frac{\partial f}{\partial y}\\
&=& \nabla f \cdot\hat{\textbf{u}}
\end{eqnarray}$$

where the derivative \\(\partial f/\partial x \\) actually means the derivative with respect to the *first argument*, or, \\(x+ah\\). When we plug in \\(h = 0\\), we get 

$$g'(0) = \nabla f \cdot \hat{\textbf{u}}$$

where now the gradient is evaluated at \\((x,y)\\), because \\(h = 0\\).

Matching these two, we get that 

<div class = "result">
$$D_\hat{\textbf{u}}f = \nabla f \cdot\hat{\textbf{u}}$$ </div>

Thus we have our formula for the directional derivative. 

### Exercises

<ol>
<li> <div> Calculate the directional derivative </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
