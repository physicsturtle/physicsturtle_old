---
layout: lesson
title: LINE INTEGRALS 2D
course: calculus-III
unit: unit5
lessonID: line-integrals
nextID: fundamental-theorem-line-integrals
---

A line integral allows us to integrate a function along a line in the plane or in space. There are different line integrals that can be set up for any given line, each of which has its own physical interpretation. They all however allow the same method of evaluation. Let us start here with line integrals in the plane.

Definition: Suppose $C$ is a plane curve parametrized by $t$, and that its endpoints are $((x(a),y(a))$ and $(x(b),y(b))$, where $t$ ranges from $a$ to $b$. Then the line integral of $f$ along $C$ is:

$$\int_C f(x,y) ds = \int_a^b f(x(t),y(t)) \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} dt$$

Let's start with some examples. 

Example: Integrate $f(x,y) = xe^y$ along the curve $y = x^2$, from $(-1,1)$ t0 $(1,1)$.

















If we have the case of a space curve, then the definition becomes 

$$\int_C f(x,y,z) ds = \int_a^b f(x(t),y(t),z(t)) \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 + \left(\frac{dz}{dt}\right)^2} dt$$




- Definition of a line integral
- Work and flux in the plane, line integral of a vector field
- Line integral of a scalar field
- Work in space, line integral of a vector field
- Line integral of a scalar field

Line integrals, not unlike integrals in a single variable, allow us to integrate along a one dimensional path, but this path need not be straight anymore. This means that we can calculate quantities like the work required to move along this path. Line integrals for work can be calculated in both 2 or 3 dimensions, but line integrals for flux are defined only for 2 dimensions.


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
