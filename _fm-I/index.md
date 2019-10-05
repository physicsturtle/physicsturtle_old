---
layout: course
title: Fluid Mechanics I
permalink: /fm-I/
---

<a class="page-link" href="/cm-III/introduction">Introduction - What is fluid mechanics? </a>

<a class="page-link" href="/cm-III/notation">Notation and Conventions </a>

The prerequisites are as follows
1. A strong background in Newtonian mechanics
2. A strong knowledge of multivariable and vector calculus
3. A working knowledge of ordinary differential equations
4. A working knowledge of basic electromagnetism

{% assign unitNames = "Unit 1 - , Unit 2 - , Unit 3 - , Unit 4 - , Unit 5 - , Unit 6 - , Unit 7 - , Unit 8 - " | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

{% assign lessonNames3 = "Introduction" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

<ul>
{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex == 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex == 3 %}  {% assign lessonNames = lessonNames4 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Classical Mechanics - John Taylor
2. 

