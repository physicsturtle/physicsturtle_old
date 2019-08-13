---
layout: unit
title: Unit 2
dept: math
course: calculus-II
deptDisplay: Math
courseDisplay: Calculus II
unit: unit2
---

{% assign lessonNames = "Basic_Formulas, Substitution_Rule, Integration_by_Parts, Trigonometric_Integrals, Method_of_Partial_Fractions, Trigonometric_Substitution, Hyperbolic_Substitution*, Improper_Integrals, Numerical_Integration, Miscellaneous_Tricks" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
