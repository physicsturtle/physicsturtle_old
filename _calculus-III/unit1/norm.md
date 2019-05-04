---
layout: lesson
title: NORM
course: calculus-III
unit: unit1
lessonID: norm
nextID: projections
---

Here we continue with the possible operations that one can do with vectors. The topic of this lesson is the *norm* of a vector. This is just a fancy word for the *length* or the *magnitude* of a vector. 

If we have a vector \\(\textbf{v} = (a,b)\\) in three dimensions, its magnitude, or norm, is defined as 

$$\|\textbf{v}\| = \sqrt{a^2+b^2}$$

<figure class="center">
<p><img src="vectorComps.svg" alt="Three Dimensional Coordinates" style="width:300px;height:300px;"> </p>
<figcaption class="center">Magnitude of a Vector by Pythagorean Theoremr</figcaption> </figure>

An alternative notation is 

$$|\textbf{v}| = \sqrt{a^2+b^2}$$

the latter of which we will primarily be using. Technically there is a distinction between the two, but it is beyond the scope of this course. Here they will be used interchangably. 

Similarly, this definition can be extended to three dimensions. For a vector in three dimensions \\(\textbf{v} = (a,b,c)\\), its norm is 

$$|\textbf{v}| = \sqrt{a^2+b^2+c^2}.$$

For the case of two dimensions, it is quite clear that the definition comes from the Pythagorean Theorem. However, what you might not have seen before is the Pythagorean Theorem extended to three dimensions. 

(insert image)

Because the norm calculates the length of a vector, it is possible to find the distance between two points in space by using the norm. Taking the difference of two points creates as vector that points from one to the other, which we can then calculate the norm of. 

### Properties
The properties of the norm include:

#### Scalar Multiplication
$$\|\lambda\textbf{v}\| = |\lambda|\|\textbf{v}\| $$

### Exercises

<ol>
<li> <div> Calculate the norm of each of the following vectors.
<ol type = "a">
<li> $(1,2,3)$,  </li>
<li> $(-1,-2,1)$,  </li>
<li> $(3,0,-6)$,  </li>
</ol>
</div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
<ol type = "a">
<li> </li>
</ol>
</div> </li>



<li> <div> Find the distance between each pair of points. 
<ol type = "a">
<li> $(1,1,2)$ and $(-1,2,2)$ </li>
<li> $(3,-3,4)$ and $(0,0,1)$ </li>
</ol>
</div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
answer here!
</div> </li>



<li> <div> Find the distance between each pair of points. 
<ol type = "a">
<li> $(1,1,2)$ and $(-1,2,2)$ </li>
<li> $(3,-3,4)$ and $(0,0,1)$ </li>
</ol>
</div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
answer here!
</div> </li>

``
<li> <div> Is it possible that $|\textbf{v} + \textbf{u}| = |\textbf{v}| + |\textbf{u}|$? If so, in which situations?
</div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
answer here!
</div> </li>


</ol>
