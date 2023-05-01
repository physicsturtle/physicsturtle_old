---
layout: course
title: Quantum Mechanics I
banner: qm-I.svg
permalink: /qm-I/
---
{% assign unitNames = "Unit 1 - Linear Algebra, Unit 2 - Quantum States and the Schrödinger Equation, Unit 3 - 2-State Systems, Unit 4 - Symmetries and Rotations, Unit 5 - Multiparticle Systems, Unit 6 - Problems in 1 Dimension, Unit 7 - Advanced topics, "| split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, unit6/, unit7/, " | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}
{% assign lessonNames2 = "" | split: ', ' %}
{% assign lessonNames3 = "" | split: ', ' %}
{% assign lessonNames4 = "" | split: ', ' %}
{% assign lessonNames5 = "" | split: ', ' %}
{% assign lessonNames6 = "Infinite Square Well , " | split: ', ' %}
{% assign lessonNames7 = "" | split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex== 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex== 3 %}  {% assign lessonNames = lessonNames4 %}
{% elsif unitIndex== 4 %}  {% assign lessonNames = lessonNames5 %}
{% elsif unitIndex== 5 %}  {% assign lessonNames = lessonNames6 %}
{% elsif unitIndex== 6 %}  {% assign lessonNames = lessonNames7 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', '' %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>
**Sources**
