---
layout: page
title: Differentiation
course: calculus-I
unit: unit3
permalink: /calculus-III/unit3/
---

Unit 1 lays out the foundations for understanding how to work with objects in 3 dimensional space. There won't be any calculus yet, but we'll try and understand how to draw pictures, including vectors and graphs. This will be one of the most important skills throughout the rest of the course to intuitively understand the mathematics through graphical means. 

<ol>
{% assign lessonNames = "Three-Dimensional-Cartesian-Coordinates, Vectors-and-Their-Geometry, Algebraic-Operations-with-Vectors, Norm, Projections" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: current_page.permalink}}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>

<!---
- Derivatives and Rates of Change
-  Derivatives of Polynomials 
- Derivatives of Exponential functions
- Derivatives of Trigonometric Functions
- Derivatives of Hyperbolic Functions* 
- The product rule
- The quotient Rule
- The chain rule
- Implicit Differentiation
- Derivatives of logarithmic functions
- Derivatives of Inverse Trigonometric functions
- Derivatives of Inverse Hyperbolic Functions*
- Logarithmic differentiation
- Linear Approximations and Differentials
- Taylor Polynomials
- Lagrange Remainder Theorem
--->
