---
layout: lesson
title: Equations of Planes
course: calculus-III
unit: unit1
---

As with the case of lines, there are two ways to define planes.

### Equation Form

Suppose we have a point \\((x_0,y_0,z_0)\\) which is in our plane, and the plane has normal vector \\((a,b,c)\\). Let \\(\textbf{r} = (x,y,z) \\) be a vector to some point in 3D space. Let's find a condition on this vector \\(\textbf{r}\\) such that its terminal point lies within the plane. If \\(\textbf{r}\\) points to the plane, then the vector \\(\textbf{r} - (x_0,y_0,z_0)\\) will be a vector that is parallel, or, tangent, to the plane. If it is tangent to the plane, its dot product with the plane's normal vector will be zero. Thus the condition we are left with is 

$$(a,b,c)\cdot(\textbf{r} - (x_0,y_0,z_0)) = 0$$

This can be expanded out to be 

$$a(x-x_0) + b(y-y_0) + c(z-z_0) = 0$$

or, moving the constant terms to the other side, 

$$ax + by + cz = ax_0 + by_0 + cz_0$$

where we can relabel the right hand side as \\(d\\).

### Parametric Form

