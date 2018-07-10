---
layout: lesson
title: Limits and Continuity
course: calculus-III
unit: unit2
---

When taking the limit of a vector valued function, we define this by taking the limit of each component. Thus for a vector valued function \\(\textbf{r}(t) = (x(t),y(t),z(t))\\),

$$\lim_{t\to a} \textbf{r}(t) = \left(\lim_{t\to a}x(t) , \lim_{t\to a}y(t), \lim_{t\to a}z(t)\right) $$

This means that the limit of \\(\textbf{r}\\) exists if and only if the limits of all of its components exist. As in the case of a single variable, a vector valued function is continuous at a point \\(a\\) if 

$$ \lim_{t\to a}\textbf{r}(t) = \textbf{r}(a)$$

and similar to before, the vector function continuous if and only if all of the component functions are continuous. 




### Epsilon-Delta Definition*

Although I said earlier that we define the limit of a vector function by taking the limit of each component, this is not technically true. The actual definition is the following. We say that 

$$\lim_{t\to a} \textbf{r}(t) = \textbf{R}$$ 

if for every \\(\epsilon > 0\\), there exists some \\(\delta > 0\\) such that \\(\\|\textbf{r}(t) - \textbf{R}\\| < \epsilon \\) whenever \\(\|t - a\| < \delta\\). This actually implies the above definition of componentwise limit taking. Let us now show that.



#### Theorem
For a vector valued function \\(\textbf{r}(t) = (x(t),y(t),z(t))\\), 

$$\lim_{t\to a} \textbf{r}(t) = \left(\lim_{t\to a}x(t) , \lim_{t\to a}y(t), \lim_{t\to a}z(t)\right) $$

#### Proof



<button onclick="myFunction('answer')" class="answerButton">Show Answer</button>

<div  id="answer" class="answer">
\(x\)
</div>





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






