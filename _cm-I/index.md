---
layout: course
title: Classical Mechanics I
permalink: /cm-I/
---

Welcome to Classical Mechanics I. This is a calculus based course that will introduce you to the mechanics of particles and rigid bodies. 

<b>Prerequisites</b>
1. A working knowledge of single variable calculs
2. A working knowledge of vector algebra
3. A strong background in high school physics

{% assign unitNames = "Unit 1 - Vectors # Unit 2 - Statics and Equilibrium # Unit 3 - Kinematics and Dynamics # Unit 4 - Work and Energy # Unit 5 - Circular Motion # Supplementary Material" | split: ' # ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "Displacement,_Time,_and_Velocity#Instantaneous Velocity#Average and Instantaneous Acceleration#Motion with Constant Acceleration#Freely Falling Bodies#Velocity and Position by Integration" | split: '#' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

{% assign lessonNames5 = "" | split: ', ' %}

{% assign lessonNames6 = "" | split: ', ' %}

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

