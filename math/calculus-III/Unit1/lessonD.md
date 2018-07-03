---
layout: lesson
title: Dot Product
course: calculus-III
unit: unit1
---

The dot product is one of the two ways of multiplying vectors. It can be defined between vectors in 1, 2, 3 or even more dimensions. There are two equivalent definitions of the dot product. One is very geometric, and helps us to get an intuition of what the dot product means. Unfortunately, it is not very useful when performing complex calculations. For this, the abstract definition will come in handy. 

### Geometric Definition
Suppose we have two vectors \\(\textbf{a}\\) and \\(\textbf{b}\\), in any number of dimensions. Then we define 

$$\textbf{a}\cdot\textbf{b} = \|\textbf{a}\|\|\textbf{b}\|\cos\theta$$

where \\(\theta\\) is the angle between the two vectors. This can be represented graphically by (insert picture here)

This should be thought of as calcaulting the *projection* of one vector onto the other. But, which vector is being projected onto which? Actually, it doesn't matter which vector is being projected onto which, because both results turn out to be the exact same!

If we project 

### Abstract Definition
The more abstract definition of the dot product uses the *components* of the vector. The dot product between the vectors \\(\textbf{a} = (a_1,a_2,a_3)\\) and \\(\textbf{b} = (b_1,b_2,b_3)\\) is 

$$\textbf{a}\cdot\textbf{b} = a_1b_1 + a_2b_2 + a_3b_3$$

The definition for vectors in dimensions other than 3 has the same form. For example, in 2 dimensions with vectors \\(\textbf{a} = (a_1,a_2)\\) and \\(\textbf{b} = (b_1,b_2)\\), the dot product is 

$$\textbf{a}\cdot\textbf{b} = a_1b_1 + a_2b_2$$

### Properties
The dot product has a few properties which are familiar from multiplication between scalars. 


### Equivalence of the Definitions
Now we will show that the two definitions of the dot product are actually identical. This will be done by using the cosine law, and the proof applies in either 2 or 3 dimensions. 