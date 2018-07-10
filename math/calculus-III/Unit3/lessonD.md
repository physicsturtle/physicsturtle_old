---
layout: lesson
title: Partial Differentiation
course: calculus-III
unit: unit3
---

Here we will finally learn about how to differentiate functions of multiple variables. Recall the definition of the derivative from single variable calculus:

$$f'(x) = \lim_{h\to 0} \frac{f(x+h) - f(x)}{h}$$

This represents the slope of the graph of \\(y = f(x)\\) at the point \\(x\\). If we instead have a function \\(f(x,y)\\), it is now possible to calculate its derivative with respect to either \\(x\\) or \\(y\\). These are correspondingly called the *partial derivative with respect to \\(x\\)* and  *partial derivative with respect to \\(y\\)*, respectively. We define 

$$ \frac{\partial f}{\partial x} = \lim_{h\to 0} \frac{f(x+h,y) - f(x,y)}{h}$$

$$ \frac{\partial f}{\partial y} = \lim_{h\to 0} \frac{f(x,y+h) - f(x,y)}{h}$$

so, we see that we take the limit in \\(x\\) when taking the derivative with respect to \\(x\\), and correspondingly for \\(y\\). From this, we can define higher partial derivatives!

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







