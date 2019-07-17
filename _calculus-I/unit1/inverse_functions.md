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

Here, we will construct the inverse functions for the $\sin,\cos,$ and $\tan$ according to the convention; there are other ways to 
