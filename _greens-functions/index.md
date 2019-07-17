---
layout: course
title: Green's Functions and Variational Methods
permalink: /greens-functions/
banner: greens-functions.svg
---

Welcome to Green's Functions! 

<a class="page-link" href="/calculus-I/introduction"> Introduction - What is a Green's Function? </a>

The prerequisites are as follows
1. A strong background in multivariable and vector calculus.
2. A strong background in undergraduate ordinary and partial differential equations
3. A working knowledge of asymptotic analysis may be useful

{% assign unitNames = "Unit 1 - Green's Functions for ODEs, Unit 2 - Elliptic Equations, Unit 3 - Parabolic Equations, Unit 4 - Hyperbolic Equations, Unit 5 - Eigenvalue Problems, Unit 6 - Variational Calculus" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, unit6/" | split: ', ' %}

{% assign lessonNames1 = "Green's_Functions_for_1D_BVP" | split: ', ' %}

{% assign lessonNames2 = "Free_Space_Green's_Function, Method_of_Images" | split: ', ' %}

{% assign lessonNames3 = "Heat_Kernel" | split: ', ' %}

{% assign lessonNames4 = "Wave_Equation" | split: ', ' %}

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
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Calculus, 7 ed. - Stewart, James (2012)
