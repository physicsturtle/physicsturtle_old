---
layout: lesson
title: Algebraic Operations with Vectors
course: calculus-III
unit: unit1
---

In the last section, we discussed adding and subtracting vectors geometrically. Now we will do the same, but algebraically. This is a little bit more abstract, but is much more useful when solving problems that are difficult to draw by hand.

#### Addition 
Two vectors $\textbf{v} = (v_1,v_2,v_3)$ and $\textbf{u} = (u_1,u_2,u_3)$ can be added *componentwise*.

$$ \textbf{v} + \textbf{u} = (v_1+u_1,v_2+u_2,v_3+u_3) $$

from which we see that $\textbf{u} + \textbf{v} = \textbf{v} + \textbf{u}$.

#### Subtraction
Next, we have subtraction, which is defined in the obvious way 

$$ \textbf{v} - \textbf{u} = (v_1-u_1,v_2-u_2,v_3-u_3) $$

#### Scalar Multiplication

Vectors can also be scaled by some *scalar* $\lambda \in \mathbb{R}$. The scalar $\lambda$ is distributed in to each component.

$$ \lambda\textbf{v} = (\lambda v_1, \lambda v_2, \lambda v_3) $$

It is then straightforward to define *linear combinations* of multiple vectors. A linear combination is a sum of vectors, each multiplied by their own scalar (which could be any number, positive or negative, 1 or 0, rational or irrational). For example, a linear combination of \\(\textbf{u}\\) and \\(\textbf{v}\\) could be 

$$ a\textbf{u} + b\textbf{v} = (au_1 + bv_1,au_2 + bv_2, au_3 + bv_3) $$

Linear combinations can also be taken between more than 2 vectors. 

You may now be wondering now if there are ways to multiply vectors together or to divide vectors. In this course, there are no ways to multiply or divide vectors in a way that is analogous to your preexisting notions of multiplication and division. However, there are two other ways of multiplying vectors which we will cover: the dot and cross products. Those will be covered in the next couple sections. 


#### Remarks
A common question that is asked at around this point is, "What is the difference between a point and a vector?" This is a question that students often think too much about. The way that I like to think about it is that a point is a geometric object, while a vector is an algebraic object. What I mean by that is that points cannot be added together, subtracted, or multiplied by numbers. They can only be drawn. On the other hand, vectors can be added, subtracted, multiplied by scalars, and even differentiated or integrated. They, of course, can be drawn as well, as was demonstrated in the geometry of vectors section. In these notes, we will draw few distinctions between vectors and points.

#### Notation
In addition to the notation that we will be using, $\textbf{v} = (a,b,c)$, it is also common for vectors to be written as follows:

$$ \textbf{v} = \langle a,b,c \rangle $$

$$ \textbf{v} = \begin{bmatrix} a & b & c \end{bmatrix} $$

$$ \textbf{v} = \begin{pmatrix} a \\ b \\ c \end{pmatrix} $$

$$ \textbf{v} = \begin{bmatrix} a \\ b \\ c \end{bmatrix} $$

When vectors are written this way, at least in this course, they will usually be referring to the *Cartesian* components of the vectors. That is, each of these notations can also be written as $$\textbf{v} = a\hat{\textbf{x}} + b\hat{\textbf{y}} + c\hat{\textbf{z}}$$.  If we want to write vectors in different basis, then we will denote that explicitly by writing in terms of the basis elements.


### Exercises

<ol>
<li> <div> Calculate the following quantities.
<ol type = "a">
<li> \((3,2,-1) + (-1,2,2)\)</li>
<li> \(2(1,1,5) + 3(6,-2,5)\)</li>
<li> \(-2(4,1,8) + 0(5,1,2) +(2,2,2)\)</li>
<li> \(\frac{1}{3}(4,7,6) - \frac{3}{2} (0,2,-1)\)</li>
</ol>
 </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
<ol type = "a">
<li> $(3,2,-1) + (-1,2,2) = (2,4,1)$</li>
<li> \(2(1,1,5) + 3(6,-2,5) = (2,2,10) + (18,-6,15) = (20,-4,25)\)</li>
<li> \(-2(4,1,8) + 0(5,1,2) + (2,2,2) = (-8,-2,-16) + (0,0,0) + (2,2,2) = (-6,0,-14)\)</li>
<li> \(\frac{1}{3}(4,7,6) - \frac{3}{2} (0,2,-1) = \left(\frac{4}{3},\frac{7}{3},2\right) - \left(0,3,\frac{-1}{3}\right) = \left(\frac{4}{3},\frac{16}{3},\frac{5}{3}\right)\)</li>
</ol>
</div> </li>


</ol>

