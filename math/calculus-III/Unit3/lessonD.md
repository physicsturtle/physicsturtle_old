---
layout: lesson
title: Partial Differentiation
course: calculus-III
unit: unit3
---

Here we will finally learn about how to differentiate functions of multiple variables. Recall the definition of the derivative from single variable calculus:

$$f'(x) = \lim_{h\to 0} \frac{f(x+h) - f(x)}{h}$$

This represents the slope of the graph of \\(y = f(x)\\) at the point \\(x\\). If we instead have a function \\(f(x,y)\\), it is now possible to calculate its derivative with respect to either \\(x\\) or \\(y\\). These are correspondingly called the *partial derivative with respect to \\(x\\)* and  *partial derivative with respect to \\(y\\)*, respectively. We define 

$$ \frac{\partial f}{\partial x} = \lim_{h\to 0} \frac{f(x+h,y) - f(x,y)}{h}$$

$$ \frac{\partial f}{\partial y} = \lim_{h\to 0} \frac{f(x,y+h) - f(x,y)}{h}$$

so, we see that we take the limit in \\(x\\) when taking the derivative with respect to \\(x\\), and correspondingly for \\(y\\). In practice, what this means is that we take the derivative with respect to one of the variables leaving the other constant. 

### Second Partial Derivative
Once we have calculated the first partial derivative, it is possible to calculate the second partial derivative just by taking the derivatives again. Thus, we write 

$$\begin{eqnarray} 
\frac{\partial^2 f}{\partial x^2} &=& \frac{\partial}{\partial x}\frac{\partial f}{\partial x} \\
\frac{\partial^2 f}{\partial y^2} &=& \frac{\partial}{\partial y}\frac{\partial f}{\partial y}\\
\frac{\partial^2 f}{\partial x\partial y} &=& \frac{\partial}{\partial x}\frac{\partial f}{\partial y} \\
\frac{\partial^2 f}{\partial y\partial x} &=& \frac{\partial}{\partial y}\frac{\partial f}{\partial x}
\end{eqnarray}$$

so there are *four* second partial derivatives for a function of two variables. 

### Notation
There are various ways to denote partial differentiation. For first derivatives, we have 

$$\begin{eqnarray}
\frac{\partial f}{\partial x} = f_x = \partial_x f = \partial_1 f\\
\frac{\partial f}{\partial y} = f_y = \partial_y f = \partial_2 f\\
\end{eqnarray}$$

For second derivatives, 

$$\begin{eqnarray} 
\frac{\partial^2 f}{\partial x^2} &=& (f_x)_x = f_{xx} = (f_1)_1 = \partial_1(\partial_1 f) = \partial_{11}f = \partial_x(\partial_x f) = \partial_{xx} f \\
\frac{\partial^2 f}{\partial y^2} &=& (f_y)_y = f_{yy} = (f_2)_2 = \partial_2(\partial_2 f) =  \partial_{22}f = \partial_y(\partial_y f) = \partial_{yy} f\\
\frac{\partial^2 f}{\partial x\partial y} &=& (f_y)_x = f_{yx} =  f_{yy} = (f_2)_2 = \partial_{22}f = \partial_y(\partial_y f) = \partial_{xy} f\\
\frac{\partial^2 f}{\partial y\partial x} &=& (f_x)_y = f_{xy} = \partial_{yx} f
\end{eqnarray}$$

### Clairaut's Theorem
Clairaut's theorem says:

<div class="theorem">
Let \(f\) be defined on a domain \(D\) which contains the point \((a,b)\). Then if \(
</div>



#### Examples
<ol>
<li> <div> Calculate the first partial derivatives of the function \(f(x,y) = 3x^2 + xy - 2y^2\). </div> 

<div> Keeping \(y\) constant and differentiating with respect to \(x\), 
$$\frac{\partial f}{\partial x} = 6x + y$$ 
then keeping \(x\) constant and differentiating with respect to \(y\), we get 
$$ \frac{\partial f}{\partial y} = x - 4y$$</div>
</li>

<li> <div> Calculate the first partial derivatives of the function \(f(x,y,z) = \cos(x^2y)\sin(\sqrt{z})\) </div>

<div> Keeping \(y\) and \(z\) constant and differentiating with respect to \(x\), 
$$\frac{\partial f}{\partial x} = -2xy\sin(x^2y)\sin(\sqrt{z})$$ 
then keeping \(x\) and \(z\) constant and differentiating with respect to \(y\), we get 
$$ \frac{\partial f}{\partial y} = -x^2\sin(x^2y)\sin(\sqrt{z})$$
and finally keeping \(x\) and \(y\) constant and differentiating with respect to \(z\), 
$$\frac{\partial f}{\partial z} = \cos(x^2y)\frac{\cos(\sqrt{z})}{2\sqrt{z}}.$$
</div>
</li>

<li> <div> Calculate all second partial derivatives of the function \(f(x,y) = \frac{x^3}{y} - \frac{y^2}{x^2}\). </div>
<div> Before we calculate the second derivatives, we of course need to calculate the first partial derivatives. They are, 
$$\frac{\partial f}{\partial x} = \frac{3x^2}{y} + \frac{2y^2}{x^3},\quad \frac{\partial f}{\partial y} = -\frac{x^3}{y^2} - \frac{2y}{x^2}$$
In order to calculate the second partial derivatives, we simply need to take the derivatives of the derivatives. 
</div>
</li>
</ol>



### Exercises

<ol>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

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







