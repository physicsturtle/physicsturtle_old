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
</div> <br>

### Examples
<div class="example">
<p><b>Example:</b> Determine if the function $f : \R\to \R$ defined by $f(x) = x^2$ is invertible. </p>
<b>Solution:</b> This function is <i>not</i> invertible! For a particular value of $y = x^2$ (where $y > 0$), there are two values of $x\in\R$ that satisfy this equation! They are $x = \sqrt{y}$ and $x = -\sqrt{y}$. Thus, we don't have a unique value of $x$ for a given value of $y$.
</div> <br>

One might think that, because $f(x) = x^2$ maps both positive and negative numbers to positive numbers, it cannot be invertible! However, by simply restricting the domain, we can make $f(x) = x^2$ invertible. 

<div class="example">
<p><b>Example:</b> Determine if the function $f : [0,\infty) \to \R$ defined by $f(x) = x^2$ is invertible. </p>
<b>Solution:</b> This function is invertible! For a particular value of $y = x^2$ (where $y \geq 0$), there is only one value of $x \in [0,\infty)$ that satisfies this equation! It is $x = \sqrt{y}$. This is the unique value of $x$ for a given value of $y$. The difference between this example and the previous is that we don't allow $x$ to be negative at all.
</div> <br>

### Inverse Trigonometric Functions
The development so far can be used to define inverses for the trigonometric functions. If we want to invert $f(x) = \sin x$, we have two options. 
1. To solve $\sin x = y$ for $x$, we can find the preimage of $\sin$ and obtain a set of values for $x$. This is not constructing an inverse function but rather only looking at preimages. 
2. To solve $\sin x = y$ for $x$, we can restrict the domain of $\sin$ and obtain only a single value for $x$. This is the same as constructing an inverse function. 

Note that in high school you may have written $\sin^{-1}$ for inverse sine, but here we will use $\arcsin$ for inverse sine, $\arccos$ for inverse cosine, and $\arctan$ for inverse tangent, etc.

Here, we will construct the inverse functions for the $\sin,\cos,$ and $\tan$ according to the convention; there are other ways to construct these inverses but we won't consider those. 


#### Inverse Sine
First, let's construct the inverse of the sine function. Looking at the graph of the sine function, we see that it is invertible if we restrict the domain to the interval $\left[-\frac{\pi}{2},\frac{\pi}{2}\right]$; the sine doesn't take the same value twice on that interval. Thus, we construct the arcsine function as having domain $\left[-\frac{\pi}{2},\frac{\pi}{2}\right]$, so $f : [-1,1] \to \left[-\frac{\pi}{2},\frac{\pi}{2}\right]$, and write $f(x) = \arcsin x$. 

<figure>
<div class="imgContainer" style="float:left">
<img src="inverse_functions-Figures/sin.svg" alt="Function" style="width:350px;height:250px">
<p class="center">The sine function with its domain restricted</p>
</div>
<div class="imgContainer" style="float:left">
<img src="inverse_functions-Figures/arcsin.svg" alt="Function" style="width:350px;height:250px">
<p class="center">The corresponding inverse function</p>
</div>
</figure> <br>

#### Inverse Cosine
Next, we do the same for the cosine function. The domain that we pick for the cosine function is $[0,\pi]$. Thus, it becomes invertible, and define $f : [-1,1] \to \left[0,\pi\right]$, and write $f(x) = \arccos x$. Again, we graph cosine: 

<figure>
<div class="imgContainer" style="float:left">
<img src="inverse_functions-Figures/cos.svg" alt="Function" style="width:350px;height:250px">
<p class="center">The cosine function with its domain restricted</p>
</div>
<div class="imgContainer" style="float:left">
<img src="inverse_functions-Figures/arccos.svg" alt="Function" style="width:350px;height:250px">
<p class="center">The corresponding inverse function</p>
</div>
</figure> <br>

#### Inverse Tangent
Lastly, we do the arctangent function. We restrict the domain of tangent to $\left[-\frac{\pi}{2},\frac{\pi}{2}\right]$, and define $f : [-\infty,\infty]\to \left[-\frac{\pi}{2},\frac{\pi}{2}\right]$, and write $f(x) = \arctan x$. The arctangent function is graphed in the following plot:

<figure>
<div class="imgContainer" style="float:left">
<img src="inverse_functions-Figures/tan.svg" alt="Function" style="width:350px;height:250px">
<p class="center">The tangent function with its domain restricted</p>
</div>
<div class="imgContainer" style="float:left">
<img src="inverse_functions-Figures/arctan.svg" alt="Function" style="width:350px;height:250px">
<p class="center">The corresponding inverse function</p>
</div>
</figure> <br>

#### Summary of Inverse Functions
We now summarize our results. I include here the results for the other inverse trigonometric functions $\arcsec$, $\arccsc$ and $\arccot$.

<div class="result">
<b>Inverse Trigonometric Functions Summary:</b>
<table style="width:100%">
<tr>
<th>Function</th>
<th>Domain</th> 
<th>Range (conventional)</th> 
</tr>
<tr>
<td>$$\arcsin$$</td>
<td>$$[-1,1]$$</td> 
<td>$$\left[-\frac{\pi}{2},\frac{\pi}{2}\right]$$</td> 
</tr>
<tr>
<td>$$\arccos$$</td>
<td>$$[-1,1]$$</td> 
<td>$$[0,\pi]$$</td> 
</tr>
<tr>
<td>$$\arctan$$</td>
<td>$$\R$$</td> 
<td>$$\left(-\frac{\pi}{2},\frac{\pi}{2}\right)$$</td> 
</tr>
<tr>
<td>$$\arccsc$$</td>
<td>$$[1,\infty)$$</td> 
<td>$$\left[-\frac{\pi}{2},0\right)\cup \left(0,\frac{\pi}{2}\right]$$</td> 
</tr>
<tr>
<td>$$\arcsec$$</td>
<td>$$[1,\infty)$$</td> 
<td>$$\left[0,\frac{\pi}{2}\right)\cup \left(\frac{\pi}{2},\pi\right]$$</td> 
</tr>
<tr>
<td>$$\arccot$$</td>
<td>$$\R$$</td> 
<td>$$(0,\pi)$$</td> 
</tr>
</table>
</div> <br>

### Examples

<div class="example">
<p><b>Example:</b> Evaluate the following expression:
$$\arcsin(\sin(11\pi/6))$$ </p>
<b>Solution:</b> We need to be careful and not simply cancel out the arcsine and sine! First, we need to calculate the sine, which is $\sin(11\pi/6) = -1/2$. Next, we need to calculate the arcsine of this, which is $\arcsin(-1/2) = -\pi/6$. Thus, 
$$\arcsin(\sin(11\pi/6)) = -\pi/6$$ 
</div>
