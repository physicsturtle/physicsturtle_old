---
layout: lesson
title: DOUBLE INTEGRAL IN POLAR COORDINATES
course: calculus-III
unit: unit4
lessonID: double-integral-polar
nextID: surface-area
---

- Jacobian in polar coordiantes
- switching order in polar coordinates (is htis a thing?)

In many physical problems, there is circular symmetry. In these cases it is advantageous to evaluate integrals in a coordinate system that suits the symmetry, namely, polar coordinates. When we integrate functions in polar coordinates, we will be integrating over the variables $r$ and $\theta$ instead of $x$ and $y$. One might expect that the integral would be

$$\cancelto{\text{wrong}}{\iint_R f(x,y) dx dy = \iint_R f(r\cos\theta,r\sin\theta) drd\theta}$$

This is *not* the case. The most obvious reason why this must be false is that $dxdy$ can be thought of as having units of squared length, while $dr d\theta$ has units only of length; angles are unitless. We need to find another factor containing length here! This can be done either analytically or geometrically. Here we will only show the geometric approach, and in an optional later section, we will discuss the analytic method. The analytic method is much more general, but is also more abstract.

### Geometric Derivation
There are two ways to do this geometrically. One can be done only with pictures, and the other will be done with matrices. 

In the following figure, we draw a small area element. Consider a general arc in a circle. What is its arc length? As you can probably recall from high school mathematics, its arc length is $r\theta$. Now consider a small area element $dA$.  The length of this area element is $dr$. The arc length of the area element is $rd\theta$. For small areas, we then have $$dA = rdr d\theta.$$

Now it has the correct dimensions, because there are two $r$'s, which makes length squared.

Geometric approach 2 (cross product approach)

Consider the vector  


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
