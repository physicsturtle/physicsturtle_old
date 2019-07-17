---
layout: unit
title: Unit 4
dept: math
course: calculus-I
deptDisplay: Math
courseDisplay: Calculus I
unit: unit4
permalink: /calculus-I/unit4/
---

{% assign lessonNames = "Kinematics_Problems, Exponential_Growth_and_Decay, Newton's_Law_of_Cooling, Related_Rates, Extrema_1, Extrema_2, Mean_Value_Theorem, Curve_Sketching_1, Curve-Sketching_2, Optimization_Problems, L'Hopital's_Rule, Newton's_Method" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
