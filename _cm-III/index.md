---
layout: course
title: Classical Mechanics III
permalink: /cm-III/
---

Hey everyone! Welcome to Classical Mechanics III. This course is on the topic of *Lagrangian and Hamiltonian Mechanics*, also known as *analytical mechanics*. The first half of the course is on Lagrangian Mechanics, and the second on Hamiltonian Mechanics. The first half of the course will contain many real-world examples 


<a class="page-link" href="/cm-III/introduction">Introduction - What is analytical mechanics? </a>

<a class="page-link" href="/cm-III/notation">Notation and Conventions </a>

The prerequisites are as follows
1. A strong background in Newtonian mechanics
2. A working knowledge of multivariable and vector calculus
3. A working knowledge of ordinary differential equations
4. A working knowledge of basic electromagnetism

{% assign unitNames = "Unit 1 - The Calculus of Variations, Unit 2 - Lagrange's Equations, Unit 3 - Coupled Oscillators and Normal Modes, Unit 4 - Two Body Central Force Problems, Unit 5 - Noninertial Reference Frames, Unit 6 - Rotational Motion of Rigid Bodies, Unit 7 - Collision Theory, Unit 8 - Hamiltonian Mechanics" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/" | split: ', ' %}

{% assign lessonNames1 = "Introduction, Euler_Lagrange_Equation, Hanging_Rope " | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "Relative-Coordinates" | split: ', ' %}

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

1. Calculus, 7 ed. - Stewart, James (2012)

