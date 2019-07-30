---
layout: unit
title: Unit 1
dept: math
course: calculus-II
deptDisplay: Math
courseDisplay: Calculus II
unit: unit1
---

{% assign lessonNames = "Riemann_Sums, The_Definite_Integral, Fundamental_Theorem_of_Calculus" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
