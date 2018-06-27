---
layout: lesson
title: Change of Coordinates
course: calculus-III
unit: supplement
banner: ../calculus-III.png
---

Here we are going to discuss how to find formulas for gradient, divergence, curl, and laplacian in various coordinate systems, starting from their definitions in Cartesian. We will aim to provide intuition for this, and also will give formulas for the most common coordinate transformations, namely cylindrical and spherical. We will have other coordinate systems as exercises. 

In cartesian coordinates, the definition of the gradient of a function \\(f = f(x,y,z)\\) is 

\\[ \nabla f = \frac{\partial f}{\partial x} \hat{x} + \frac{\partial f}{\partial y}\hat{y} + \frac{\partial f}{\partial z}\hat{z} \\]

When we express this in terms of another coordinate system, we can't only change the derivative terms. We must also change the unit vectors, which is what makes this so difficult. Let's do this geometrically first! 

(fill this in)


Now let's do this completely generally. Suppose that we have two coordinate systems, \\(x,y,z\\), and \\(u,v,z\\). We also have the relationships between them, 

$$\left\{\begin{eqnarray}
x &=& x(u,v,w) \\
y &=& y(u,v,z) \\
z &=& z(u,v,w)
\end{eqnarray}\right.
$$
