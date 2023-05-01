---
layout: lesson
title: Quantum States and the Schr\"odinger Equation
dept: physics
course: qm-I
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 2
---
{% assign lessonNames = "" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', '' %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
