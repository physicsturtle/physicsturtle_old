---
layout: lesson
title: Partial Differentiation
course: calculus-III
unit: unit3
---

- Geometric interpretation of partial derivative
- implicit differentiation

Here we will finally learn about how to differentiate functions of multiple variables. Recall the definition of the derivative from single variable calculus:

$$f'(x) = \lim_{h\to 0} \frac{f(x+h) - f(x)}{h}$$

This represents the slope of the graph of \\(y = f(x)\\) at the point \\(x\\). If we instead have a function \\(f(x,y)\\), it is now possible to calculate its derivative with respect to either \\(x\\) or \\(y\\). These are correspondingly called the *partial derivative with respect to \\(x\\)* and  *partial derivative with respect to \\(y\\)*, respectively. 

### Definition
<div class="definition"> 
We define the <i>partial derivative of \(f\) with respect to \(x\)</i> as

$$ \frac{\partial f}{\partial x} = \lim_{h\to 0} \frac{f(x+h,y) - f(x,y)}{h}$$

and the <i>partial derivative of \(f\) with respect to \(y\) </i> as

$$ \frac{\partial f}{\partial y} = \lim_{h\to 0} \frac{f(x,y+h) - f(x,y)}{h}$$
</div>

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

#### Examples of Partial Differentiation
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

[comment]: <> Geometric Interpretation
Similar to how the ordinary derivative of a function told us information about the slope of a curve at a certain point, the partial derivatives tell us information about the slope of a *surface* at a certain point. However, in the case of surfaces, it is not as clear what slope means. 


### Implicit Differentiation
It is also possible to perform implicit differentiation in multivariable calculus. This is best illustrated by a few examples. 

#### Examples of Implicit Partial Differentiation
<ol>
<li> <div> Calculate the first partial derivatives of \(z\) with respect to \(x\) and \(y\).  
\[\log(z^2 + y^2) = y^4 e^x\] </div> 

<div class = "boxed"> 
First we differentiate both sides with respect to \(x\).
$$\begin{eqnarray}
\frac{\partial}{\partial x}\log(z^2 + y^2) &=& \frac{\partial}{\partial x} (y^4 e^x) \\
\frac{1}{z^2+y^2}2z\frac{\partial z}{\partial x} &=& y^4 e^x
\end{eqnarray}$$
This gives us 
$$\frac{\partial z}{\partial x} = y^4e^x\frac{(y^2+z^2)}{2z} $$

Now we differentiate both sides with respect to \(y\).)
$$\begin{eqnarray}
\frac{\partial}{\partial y}\log(z^2+y^2) &=& \frac{\partial}{\partial y}(y^4 e^x)\\
\frac{1}{z^2+y^2}\left(2z\frac{\partial z}{\partial y} + 2y\right) &=& 4y^3 e^x \\
\end{eqnarray}$$
Then isolating \(\partial z/\partial y\), we get 

$$\frac{\partial z}{\partial y} = \frac{4y^3e^x(z^2+y^2) - 2y}{2z}$$
</div>
</li>

<li> <div> Calculate the first partial derivatives of \(z\) with respect to \(x\) and \(y\). 
\[z^2\sin(xz) = z\cos(y^2 + x^3y)\]</div>

<div> 
First we differentiate both sides with respect to \(x\). 
$$\begin{eqnarray}
\frac{\partial}{\partial x}(z^2\sin(xz) )&=& \frac{\partial}{\partial x}( z\cos(y^2 + x^3y))\\
2z\frac{\partial z}{\partial x}&=& 
\end{eqnarray}$$
</div>
</li>

</ol>


### Clairaut's Theorem
Clairaut's theorem says:

<div class="theorem">
Let \(f\) be defined on a domain \(D\) which contains the point \((a,b)\). Then if \(
</div>



## Exercises
For this lesson, there is going to be more exercises than usual because it is important that the student be able to perform partial differentiation quickly and without errors. 
<ol>

<li> <div> Find the partial derivatives \(f_x, f_y\) of the function \(f\). 
\[f(x,y) = [\sin(xy)]^{\sin5}\] </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
\begin{eqnarray*}
f_x &=& (\sin5)[\sin(xy)]^{\sin5-1}\cdot \cos(xy)y\\
f_y &=& (\sin5)[\sin(xy)]^{\sin5-1}\cdot \cos(xy)x
\end{eqnarray*}
</div> </li>

<li> <div> Find all second partial derivatives of \(z\). 
\[z = x\cos y - y \cos x\] </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
First find the first partial derivatives. 
\begin{eqnarray*}
\frac{\partial z}{\partial x} &=& \cos y + y\sin x\\
\frac{\partial z}{\partial y} &=& -x\sin y - \cos x
\end{eqnarray*}

Second derivatives are: 
\begin{eqnarray*}
\frac{\partial^2 z}{\partial x^2} &=& y\cos x\\
\frac{\partial^2 z}{\partial y \partial x} &=& -\sin y + \sin x\\
\frac{\partial^2 z}{\partial x \partial y} &=& -\sin y + \sin x\\
\frac{\partial^2 z}{\partial y^2} &=& -x\cos y
\end{eqnarray*}
Note that the mixed partials are equal to one another, so we didn't really need to compute both. 
</div> </li>


<li> <div> Find the first partial derivatives of the function. \[g(x,y) = \cos(x\cos y)\] </div>

<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer">
$$ \begin{eqnarray}
g_x = -\sin(x\cos y) \cdot \cos y\\
g_y = \sin(x\cos y) \cdot x \sin y
\end{eqnarray}$$
</div> </li>

<li> <div> Find the partial derivatives \(f_x, f_y\) of the function \(f\). 
\[f(x,y) = x^2+y^2\sin(xy)\]</div>

<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer">
$$ \begin{eqnarray}
f_x = 2x + y^3 \cos(xy)\\
f_y = 2y\sin(xy) + y^2x\cos(xy)
\end{eqnarray} $$
</div> </li>

<li> <div> Find the partial derivatives \(f_x, f_y\) of the function \(f\).
\[f(x,y) = \tan\left(\frac{x^2}{y}\right)\] </div>

<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer">


$$ \begin{eqnarray}
f_x = \frac{2x}{y}\sec^2\left(\frac{x^2}{y}\right)\\
f_y = -\frac{x^2}{y^2}\sec^2\left(\frac{x^2}{y}\right)
\end{eqnarray}$$
</div> </li>

<li> <div> Find all first partial derivatives of the function \[f(x,y) = y^4\log(x^3 + \sqrt{y})\] </div>

<button onclick="myFunction('answer6')" class="answerButton">Show Answer</button>
<div  id="answer6" class="answer">
\[f_x = \frac{3x^2y^4}{x^3 + \sqrt{y}}\]
\[f_y = 4y^3\log(x^3 + \sqrt{y}) + \frac{y^4}{2\sqrt{y}(x^3 + \sqrt {y})}\]
</div> </li>

<li> <div> Find all first partial derivatives of \(f\). \[f(x,y,z) = \sqrt{\sin(x^2y) + z^4}\] </div>

<button onclick="myFunction('answer7')" class="answerButton">Show Answer</button>
<div  id="answer7" class="answer">
\[ f_x = \frac{xy\cos(x^2y)}{\sqrt{\sin(x^2y) + z^4}}\]
\[f_y = \frac{x^2\cos(x^2y)}{2\sqrt{\sin(x^2y) + z^4}}\]
\[f_z = \frac{2z^3}{\sqrt{\sin(x^2y) + z^4}}\]
</div> </li>

<li> <div> Find all first partial derivatives of \(g\). Don't forget the fundamental theorem of calculus! \[\displaystyle{g(x,y) = \log(y-x) \cdot \int^{\cos y}_{x^2} e^{t^2 - t} dt}\] </div>

<button onclick="myFunction('answer8')" class="answerButton">Show Answer</button>
<div  id="answer8" class="answer">
\[g_x = \frac{1}{x-y}\int^{\cos y}_{x^2} e^{t^2-t} dt - 2x\log (y-x) e^{x^4-x^2}\]
\[g_y = \frac{1}{y-x} \int^{\cos y}_{x^2} e^{t^2-t} dt - \sin y \log(y-x) e^{\cos^2y - \cos y}\]
</div> </li>

</ol>

