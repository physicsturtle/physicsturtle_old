---
layout: page
title: Introduction to 3D Space and Vectors
course: calculus-III
unit: unit1
permalink: /calculus-III/unit1/
---

Unit 1 lays out the foundations for understanding how to work with objects in 3 dimensional space. There won't be any calculus yet, but we'll try and understand how to draw pictures, including vectors and graphs. This will be one of the most important skills throughout the rest of the course to intuitively understand the mathematics through graphical means. 

<ol>
{% assign temp = "three-dimensional-cartesian" %}
{% for my_page in site.calculus-III %}
{% for my_page in site.calculus-III %}
{% if my_page.unit == "unit1" and my_page.layout == "lesson" and my_page.lessonID == temp %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% assign temp = my_page.nextID %}
{% endif %}
{% endfor %}
{% endfor %}
</ol>

<!---
Three-dimensional cartesian coordinaes
vectors and geometry
algebraic operations with vectors
norm
--->
