---
layout: unit
title: Unit 4
dept: math
course: calculus-II
deptDisplay: Math
courseDisplay: Calculus II
unit: unit4
---

{% assign lessonNames = "Polar_Coordinates, Arc_Length_and_Area, Conic_Sections" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
