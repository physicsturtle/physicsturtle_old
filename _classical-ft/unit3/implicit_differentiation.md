---
layout: lesson
title: Implicit Differentiation
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

So far we have looked at functions of the form $y = f(x)$, where $y$ is explicitly determined in terms given any $x$. It is also possible to construct curves in the $xy$ plane for which it is not possible to solve for $y$ in terms of $x$. For example, the points which satisfy the equation

$$y^3 + 2y = 3x + \sin x$$

form a curve, yet we cannot solve for $y = f(x)$, at least easily. In cases like these, we may be interested in finding the slope at some point along the curve. How can we calculate the slope without having it expressed in the form $y = f(x)$? It is possible to apply *implicit differentiation* to calculate this slope. This can be done by differentiating both sides of such an equation with respect to $x$ and then applying the chain rule. This is best illustrated by an example. 

<div class="example">
<p><b>Example:</b> Find the slope of the curve $y^3 + 2y = 3x + \sin x$ at the point $(0,0)$. </p>
<b>Solution:</b> We start by differentiating both sides with respect to $x$. 
$$\begin{eqnarray*}
\frac{d}{dx} (y^3 + 2y) &=& \frac{d}{dx}(3x + \sin x) \\
3y^2y' + 2y' &=& 3+\cos x \\
y' &=& \frac{3+\cos x}{3y^2+1}
\end{eqnarray*}$$
If we plug in $(0,0)$, we find that $y' = 4$. 
</div>

Now we work some more examples. 

<div class="example">
<p><b>Example:</b> Find the slope of the curve </p>

</div>














