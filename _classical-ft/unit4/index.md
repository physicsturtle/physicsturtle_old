---
layout: page
title: Applications of Differentiation
course: calculus-I
unit: unit4
permalink: /calculus-III/unit4/
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
- Kinematics Problems
- Newton’s law of cooling
- Exponential Growth and Decay
- Related Rates 
- Extrema 1
- Extrema 2
- The Mean Value Theorem
- Curve Sketching 1
- Curve Sketching 2
- Optimization Problems 325
- Indeterminate Forms and l’Hospital’s Rule
- Newton’s Method 338
- Antiderivatives 344
--->
