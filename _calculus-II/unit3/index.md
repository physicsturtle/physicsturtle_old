---
layout: unit
title: Unit 3
dept: math
course: calculus-II
deptDisplay: Math
courseDisplay: Calculus II
unit: unit3
---

{% assign lessonNames = "Area_Between_Curves, Volume_of_Revolution, Work, Average_Value_of_a_Function, Arc_Length, Surface_of_Revolution, Center_of_Mass, Probability, Differential_Equations" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
