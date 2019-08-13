---
layout: lesson
title: Method of Partial Fractions
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---

In this section, we study integrals of the form

$$\int \frac{p(x)}{q(x)} dx,$$

where both $p$ and $q$ are polynomial functions. In solving these problems we do a partial fraction decomposition, which splits the integrand into a sum of simple terms. For example, a rational function and its partial fraction decomposition is

$$\frac{1}{(x+1)(x+2)} = \frac{1}{x+1} - \frac{1}{x+2}.$$

The decomposed function is much easier to integrate, but how would we actually calculate this? That is the goal of this lesson.

We only apply partial fraction decomposition if the degree of the numerator is strictly less than the degree of the denominator. The degree of a polynomial is its highest power. For example, the degree of $x^3 - 2x + 5$ is 3 because of the $x^3$ term. 

1. If the degree of $p$ is greater than or equal to the degree of $q$, apply polynomial long division first, then partial fractions.
2. If the degree of $p$ is less than the degree of $q$, proceed directly to partial fractions. 

The student is expected to recall polynomial long division from secondary school, but we will review it here.

### Polynomial Long Division

$$\polylongdiv{X^3+X^2-1}{X-1}$$

### Partial Fraction Decomposition
There are four forms that we can tackle with partial fraction decomposition. 

#### Case 1: Distinct Linear Factors
<div class="example">
<p><b>Example:</b> Decompose the function
$$\frac{1}{(x+1)(x+3)}$$
in a partial fractions decomposition. </p>
<p><b>Solution:</b>We write
$$\frac{1}{(x+1)(x+3)} = \frac{A}{x+1} + \frac{B}{x+3}$$
where $A$ and $B$ are coefficients to be found. There are two methods to find $A$ and $B$, and I will illustrate both here. </p>

<p><b>Method 1:</b> Multiply both sides by $(x+1)(x+3)$, so that we get 
$$1 = A(x+3) + B(x+1) = (A+B)x + (3A + B)$$
Since this is supposed to be an identity (meaning that the equation works for every value of $x$), we match coefficients to get
$$A+B = 0,\qquad 3A + B = 1.$$
There are no $x$ terms on the left hand side, which is why we got $A+B =0$, and the constant terms need to match too. If we solve this system of equations, we find that $A = 1/2$ and $B = -1/2$. </p>

<p><b>Method 2:</b> Multiply both sides by $(x+1)(x+3)$, so that we get 
$$1 = A(x+3) + B(x+1) = (A+B)x + (3A + B).$$
Since this is supposed to be an identity (meaning that the equation works for every value of $x$), it is true in particular for $x = -1$. Plugging in $x = -1$ to both sides gives us $1 = A(-1+3)$, so $A = 1/2$. The equation is also true for $x = -3$. Plugging in $x = -3$ to both sides gives us $1 = B(-3 + 1)$, so $B = -1/2$. </p>

Thus both methods give the same result so the decomposition is

$$\frac{1}{(x+1)(x+3)} = \frac{1}{2}\frac{1}{x+1} - \frac{1}{2}\frac{1}{x+3}.$$
</div> <br>

<div class="example">
<p><b>Example:</b> Decompose the function
$$\frac{x-2}{(2x+1)(x+3)}$$
in a partial fractions decomposition. </p>
<p><b>Solution:</b>We write
$$\frac{x-2}{(x+1)(x+3)} = \frac{A}{2x+1} + \frac{B}{x+3}$$
where $A$ and $B$ are coefficients to be found. There are two methods to find $A$ and $B$, and I will illustrate both here. </p>

<p><b>Method 1:</b> Multiply both sides by $(x+1)(x+3)$, so that we get 
$$1 = A(x+3) + B(x+1) = (A+B)x + (3A + B)$$
Since this is supposed to be an identity (meaning that the equation works for every value of $x$), we match coefficients to get
$$A+B = 0,\qquad 3A + B = 1.$$
There are no $x$ terms on the left hand side, which is why we got $A+B =0$, and the constant terms need to match too. If we solve this system of equations, we find that $A = 1/2$ and $B = -1/2$. </p>

<p><b>Method 2:</b> Multiply both sides by $(x+1)(x+3)$, so that we get 
$$1 = A(x+3) + B(x+1) = (A+B)x + (3A + B).$$
Since this is supposed to be an identity (meaning that the equation works for every value of $x$), it is true in particular for $x = -1$. Plugging in $x = -1$ to both sides gives us $1 = A(-1+3)$, so $A = 1/2$. The equation is also true for $x = -3$. Plugging in $x = -3$ to both sides gives us $1 = B(-3 + 1)$, so $B = -1/2$. </p>

Thus both methods give the same result so the decomposition is

$$\frac{1}{(x+1)(x+3)} = \frac{1}{2}\frac{1}{x+1} - \frac{1}{2}\frac{1}{x+3}.$$
</div>


### Case 2: Unfactorable Quadratic
<div class="example">
<p><b>Example:</b> Decompose the function
$$\frac{1}{(x^2+2x+7)(x-1)}$$
in a partial fractions decomposition. </p>
<p><b>Solution:</b>We write
$$\frac{1}{(x+1)(x+3)} = \frac{A}{x+1} + \frac{B}{x+3}$$
where $A$ and $B$ are coefficients to be found. There are two methods to find $A$ and $B$, and I will illustrate both here. </p>

Multiply both sides by $(x+1)(x+3)$, so that we get 
$$1 = A(x+3) + B(x+1) = (A+B)x + (3A + B)$$
Since this is supposed to be an identity (meaning that the equation works for every value of $x$), we match coefficients to get
$$A+B = 0,\qquad 3A + B = 1.$$
There are no $x$ terms on the left hand side, which is why we got $A+B =0$, and the constant terms need to match too. If we solve this system of equations, we find that $A = 1/2$ and $B = -1/2$. </p>


$$\frac{1}{(x+1)(x+3)} = \frac{1}{2}\frac{1}{x+1} - \frac{1}{2}\frac{1}{x+3}.$$
</div>
