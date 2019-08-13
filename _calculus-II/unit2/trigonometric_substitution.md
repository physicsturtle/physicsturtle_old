---
layout: lesson
title: Trigonometric Substitution
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---

In this section, we will work to reduce complicated integrals to trigonometric integrals, which we explored in the last section. For this section, recall the Pythagorean trigonometric identities:

$$\sin^2 \theta + \cos^2\theta = 1,\qquad 1 + \tan^2\theta = \sec^2\theta.$$

There are three trigonometric substitutions which we will most commonly use. 

1. For expressions of the form $\sqrt{a^2 - x^2}$, substitute $x = a\cos \theta$ or $x = a\sin\theta$. Either will work. 
2. For expressions of the form $\sqrt{x^2 + a^2}$, substitute $x = a\tan\theta$. 
3. For expressions of the for m$\sqrt{x^2 - a^2}$, substitute $x = a\sec\theta$. 

The reason that these substitutions work is because it changes the complicated square root expressions into simple trigonometric expressions. For example, in $\sqrt{a^2 -x^2}$, if we put $x = a\sin\theta$, then the expression becomes 

$$\sqrt{a^2 - x^2} = \sqrt{a^2 - a^2\sin^2\theta} = \sqrt{a^2\cos^2\theta} = a\cos\theta,$$

which is much simpler than before!

### Examples

<div class="example">
<p><b>Example:</b> Evaluate the following integral
$$\int \frac{\sqrt{9-x^2}}{x^2} dx$$
</p>
<b>Solution:</b> Make the substitution $x = 3\sin\theta$, $dx = 3\cos\theta d\theta$. Substituting this into the integral, we get 
\begin{eqnarray*}
\int \frac{\sqrt{9-x^2}}{x^2} dx &=& \int \frac{\sqrt{9-9\sin^2\theta}}{9\sin^2\theta}3\cos\theta d\theta \\
&=& \int \frac{3\sqrt{1-\sin^2\theta}}{3\sin^2\theta} \cos\theta d\theta \\
&=& \int \frac{\cos^2\theta}{\sin^2\theta} d\theta\\
&=& \int \cot^2\theta d\theta\\
&=& \int (\csc^2\theta - 1) d\theta\\
&=& -\cot\theta -\theta
\end{eqnarray*}
Now that we have integrated, we have to plug back in the substitution $x = 3\sin\theta$. However, there are no sines to be found. We only have a cotangent! This can actually be rewritten in terms of sines. 
\begin{eqnarray*}
-\cot\theta -\theta &=& -\frac{\cos\theta}{\sin\theta} - \theta \\
&=& -\frac{\sqrt{1-\sin^2\theta}}{\sin\theta} - \theta \\
&=& -\frac{\sqrt{1-x^2/9}}{x/3} - \arcsin\left(\frac{x}{3}\right) \\
&=& -\frac{\sqrt{9-x^2}}{x} - \arcsin\left(\frac{x}{3}\right)
\end{eqnarray*}
Summarizing, 
$$\int \frac{\sqrt{9-x^2}}{x^2} dx = -\frac{\sqrt{9-x^2}}{x} - \arcsin\left(\frac{x}{3}\right) + C$$
</div>





