---
layout: unit
title: Unit 5
dept: math
course: calculus-II
deptDisplay: Math
courseDisplay: Calculus II
unit: unit5
---

{% assign lessonNames = "Sequences, Series_and_Divergence_Test, Comparison_Test, Integral_Test, Alternating_Series, Absolute_Convergence, Ratio_and_Root_Tests, Power_Series, Functions_as_Power_Series, Taylor_Series" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
