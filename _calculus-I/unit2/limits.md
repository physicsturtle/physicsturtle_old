---
layout: lesson
title: Limits
dept: math
course: calculus-I
unit: unit2
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 2
---

### Introduction

In this section, we will introduce the idea of the limit of a function. We will also introduce some examples and think about limits intuitively without diving into any complicated functions yet.

It is easiest to introduce the limit idea with a picture.  Consider the following plot of $y = f(x)$, particularly about the point $x = 1$. What happens to the value of $y$ as we approach $x = 1$ from the left? Well, the value of $y$ gets closer and closer to $2$. How about if we approach from the right? In this case, the value of $y$ gets closer and closer to 1. At exactly the point $x = 1$, we have $y = 2$. 

<figure class="center">
<p><img src="limits-Figures/intro.svg" alt="Intro" style="width:350px;height:250px;"> </p>
<figcaption class="center">A Classic Example</figcaption> </figure>

To write this mathematically, we would say 

$$\lim_{x\to 1^-} f(x) = 2,\qquad \lim_{x\to 1^+} f(x) = 1.$$

These are read, respectively, as "the limit of $f(x)$ as $x$ approaches 1 from the left is 2" and "the limit of $f(x)$ as $x$ approaches 1 from the right is 1". So, $x\to 1^-$ means $x$ approaches from the left, and $x\to 1^+$ means that $x$ approaches from the right. We would say that *the limit does not exist*, because it is different from both sides. 

For certain functions, it is obvious what the value of the function $f(x)$ approaches as $x$ approaches a certain number. 

<div class="example">
<p><b> Example: </b> What is the limit of $f(x) = x+2$ as $x$ approaches $-1$? </p>
<b>Solution:</b> In this case, it is quite clear that $f(x)$ approaches $1$. This can be seen readily by graphing the function, or plugging in $x = -1$.
</div> <br>

For other functions, it is not immediately obvious what the function approaches! Consider the following example.

<div class="example">
<p><b> Example: </b> What is the limit of $f(x) = \frac{x^2-1}{x-1}$ as $x$ approaches $1$? </p>
<b>Solution:</b> One can notice that the numerator can be factored, and we write 

$$f(x) = \frac{(x+1)(x-1)}{x-1}$$

Of course, we cannot simply plug in the limiting value of $x$ as we did in the previous example, because this would cause $\frac{0}{0}$! However, the point of the limit is that we observe what the function does as $x$ approaches $1$, but $x$ never actually equals $1$. Thus, we don't have to worry about dividing by zero. Thus, we can simplify

$$\lim_{x\to1} f(x)= \lim_{x\to 1}\frac{(x+1)(x-1)}{x-1} = \lim_{x\to 1}(x+1) = 2.$$

This also agrees with a picture, if we graph the function.
</div> <br>

Now that we have some intuition behind limits, let's move on to practical tricks to calculate limits, even for complicated functions!



<!--- DONT' FORGET TO TALK ABOUT ONE SIDED LIMITS  --->
