---
layout: lesson
title: Inverse Functions
dept: math
course: calculus-I
unit: unit1
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit I
---

### Definition
Our definition of a function $f : A\to B$ before was from the set $A$ to the set $B$, where, to each element of $A$, a single element of $B$ was specified. It is possible that two elements from $A$ map to the same element of $B$. You have seen before that if we want to solve $x^2 = 4$ for $x$, we have to consider the positive or negative square root of 4, that is, $x = \pm 2$. This is an example of inverting a function which *does not have an inverse*. Let's make this statement more precise. 

<div class="definition">
<b>Definition:</b> Let $f : A\to B$ be a function. If, for any element $b\in B$, the preimage of $\{b\}$ under $f$, $f^{-1}(\{b\}) = \{a\}$ has only a single element, then $f$ is said to be <i>invertible</i>. Furthermore, if $f$ has an inverse then the <i>inverse function</i> of $f$ satisfies $f^{-1}(b) = a$ if $f(a) = b$. 
</div>

### Examples
<div class="example">
<p><b>Example:</b> Determine if the function $f : \R\to \R$ defined by $f(x) = x^2$ is invertible. </p>
<b>Solution:</b>

</div> <br>
One might think that, because $f(x) = x^2$ maps both positive and negative numbers to positive numbers, it cannot be invertible! However, by simply restricting the domain, we can make $f(x) = x^2$ invertible. 

<div class="example">
<p><b>Example:</b> Determine if the function $f : [0,\infty) \to \R$ defined by $f(x) = x^2$ is invertible. </p>
<b>Solution:</b>

</div> <br>

### Inverse Trigonometric Functions
The development so far can be used to define inverses for the trigonometric functions. If we want to invert $f(x) = \sin x$, we have two options. 
1. To solve $\sin x = y$ for $x$, we can find the preimage of $\sin$ and obtain a set of values for $x$. This is not constructing an inverse function but rather only looking at preimages. 
2. To solve $\sin x = y$ for $x$, we can restrict the domain of $\sin$ and obtain only a single value for $x$. This is the same as constructing an inverse function. 

Note that in high school you may have written $\sin^{-1}$ for inverse sine, but here we will use $\arcsin$ for inverse sine, $\arccos$ for inverse cosine, and $\arctan$ for inverse tangent, etc.

Here, we will construct the inverse functions for the $\sin,\cos,$ and $\tan$ according to the convention; there are other ways to construct these inverses but we won't consider those. First, let's construct the inverse of the sine function. Looking at the graph of the sine function, we see that it is invertible if we restrict the domain to the interval $\left[-\frac{\pi}{2},\frac{\pi}{2}\right]$; the sine doesn't take the same value twice on that interval. Thus, we construct the arcsine function as having domain $\left[-\frac{\pi}{2},\frac{\pi}{2}\right]$, so $f : [-1,1] \to \left[-\frac{\pi}{2},\frac{\pi}{2}\right]$, and write $f(x) = \arcsin x$. 

(insert sine and arcsine graph here)

Next, we do the same for the cosine function. The domain that we pick for the cosine function is $[0,\pi]$. Thus, it becomes invertible, and define $f : [-1,1] \to \left[0,\pi\right]$, and write $f(x) = \arccos x$. Again, we graph cosine:

(insert cosine and arccosine graph here)

 Lastly, we do the arctangent function. We restrict the domain of tangent to $\left[-\frac{\pi}{2},\frac{\pi}{2}\right]$, and define $f : [-\infty,\infty]\to \left[-frac{\pi/2},\frac{\pi}{2}\right]$, and write $f(x) = \arctan x$. The arctangent function is graphed in the following plot:

(insert tangent and arctangent graph here)

We now summarize our results. I include here the results for the other inverse trigonometric functions $\arcsec$, $\arccsc$ and $\arccot$.

<div class="result">
<b>Inverse Trigonometric Functions:</b>
</div>

### Examples

<div class="example">
<p><b>Example:</b> Evaluate the following expression:
$$\arcsin(\sin(11\pi/6))$$ </p>

</div>
