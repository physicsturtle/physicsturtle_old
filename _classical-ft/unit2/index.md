---
layout: page
title: Limits and Continuity
course: calculus-I
unit: unit2
permalink: /calculus-I/unit2/
---

Unit 1 lays out the foundations for understanding how to work with objects in 3 dimensional space. There won't be any calculus yet, but we'll try and understand how to draw pictures, including vectors and graphs. This will be one of the most important skills throughout the rest of the course to intuitively understand the mathematics through graphical means. 

<ol>
{% assign lessonNames = "Limits, Limit-Laws" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: current_page.permalink}}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>

<!---
- The Tangent and Velocity Problems — Motivation
- The Limit of a Function 
- Calculating Limits Using the Limit Laws 
- The Precise Definition of a Limit 
- Continuity 
- Intermediate value theorem
- Limits at Infinity; Horizontal Asymptotes 
- Limits at Infinity: Slant Asymptotes
- Hyperbolic Functions 
--->
