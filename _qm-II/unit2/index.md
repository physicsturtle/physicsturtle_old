---
layout: page
title: Unit 2
course: qm-II
unit: unit2
---

Unit 2 introduces perturbation theory for the time independent case.

{% assign lessonNames = "First_Order_Perturbation_Theory, Degenerate_Perturbation_Theory" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
