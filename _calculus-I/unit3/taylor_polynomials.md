---
layout: lesson
title: Taylor Polynomials
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

Suppose we have a function $f(x)$, and we are interested in approximating its value near $x = a$. A truly awful approximation would be $f(x)\approx f(a)$. This is an awful approximation because it works only at the value $x = a$. Everywhere else, the approximation, which is simply a horizontal line, isn't even close to the value of the actual function. 

(insert figure here)

A better approximation would be a straight line which not only passes through the point $(a,f(a))$, but also has the same slope as the original function at that point. This approximation is the linear approximation which we have discussed before:

$$L(x) = f(a) + (x-a)f'(a)\approx f(x).$$

(insert figure here)

One can see that this approximation not only passes through the curve at $(a,f(a))$, but also is pretty close to the curve in a small neighbourhood around $x=a$. 

The next best approximation would match the second derivative as well. This approximation is 

$$f(x) = f(a) + (x-a)f'(a) + \frac{(x-a)^2f''(a)}{2}.$$



