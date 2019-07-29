---
layout: course
title: Classical Mechanics IV
permalink: /cm-IV/
---

Hey everyone! Welcome to Classical Mechanics IV. This course extends the ideas of the previous course to further formulations of classical mechanics, for example Hamiltonian mechanics. The course will also introduce the reader to further topics such as the canonical formulation of classical mechanics, continuum mechanics, chaos theory, and perturbation theory. 


<a class="page-link" href="/cm-IV/introduction">Introduction - What is analytical mechanics? </a>

The prerequisites are as follows
1. A strong background in Newtonian mechanics
2. A working knowledge of multivariable and vector calculus
3. A working knowledge of ordinary differential equations
4. A working knowledge of basic electromagnetism

{% assign unitNames = "Unit 1 - Hamilton's Equations, Unit 2 - Canonical Transformations, Unit 3 - Hamilton-Jacobi Theory, Unit 4 - Classical Chaos Theory, Unit 5 - Perturbation Theory, Unit 6 - Relativistic Mechanics, Unit 7 - Continuum Mechanics and Fields" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/" | split: ', ' %}

{% assign lessonNames1 = "file" | split: ', ' %}

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
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Classical Mechanics - Goldstein
2. Mechanics - Landau and Lifshitz
3. Classical Mechanics - Taylor

