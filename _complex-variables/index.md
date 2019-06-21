---
layout: course
title: Complex Variables
permalink: /complex-variables/
banner: complex-variables.svg
---

Welcome to Complex Variables! This course is often called complex analysis, but the level of rigour at which I will present this course does not warrant it being called analysis. 



<a class="page-link" href="/calculus-III/introduction">Introduction - What is Multivariable Calculus? </a>

The prerequisites for this course are
1. 

{% assign unitNames = "Unit 1 - Complex Numbers and Algebra, Unit 2 - Mappings and Differentiation, Unit 3 - Integration, Unit 4 - Applications, Unit 5 - Laurent Series and the Calculus of Residues" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

{% assign lessonNames5 = "" | split: ', ' %}

<ul>
{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex == 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex == 3 %}  {% assign lessonNames = lessonNames4 %}
{% elsif unitIndex == 4 %}  {% assign lessonNames = lessonNames5 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Complex Variables and Applications, Churchill and Brown
