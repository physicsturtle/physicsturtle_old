---
layout: page
title: Introduction to 3D Space and Vectors
course: calculus-III
unit: unit1
permalink: /calculus-III/unit1/
---

Unit 1 lays out the foundations for understanding how to work with objects in 3 dimensional space. There won't be any calculus yet, but we'll try and understand how to draw pictures, including vectors and graphs. This will be one of the most important skills throughout the rest of the course to intuitively understand the mathematics through graphical means. 

<ol>
{% assign lessonNames = "Three-Dimensional-Cartesian-Coordinates, Vectors-and-Their-Geometry, Algebraic-Operations-with-Vectors, Norm, Projections, Dot-Product, Determinant-and-Cross-Product, Equations-of-Lines, Equations-of-Planes, Quadric-Surfaces, Cylindrical-Coordinates, Spherical-Coordinates, General-Surfaces" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
<li> <a class = "page-link" href = "{{ lessonName | prepend: current_page.permalink}}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>

<!---
Three-dimensional cartesian coordinaes
vectors and geometry
algebraic operations with vectors
norm
--->
