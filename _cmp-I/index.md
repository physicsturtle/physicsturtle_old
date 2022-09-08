---
layout: course
title: Condensed Matter Physics I
permalink: /cmp-I/
banner: cmp-I.svg
---

Welcome to your first graduate course in Condensed Matter Physics.

The prerequisites are as follows:
1. A background in undergraduate quantum and statistical mechanics
2. An undergraduate course in condensed matter physics.

{% assign unitNames = "Unit 1 - Lattice Systems, Unit 2 - Second Quantization, Unit 3 - Electrons in a Periodic Potential, Unit 4 - Weakly Interacting Electrons, Unit 5 - Phonons, Unit 6 - Electron-Phonon Coupling, Unit 7 - Superconductivity" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, unit6/, unit7/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

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

1. Solid State Physics - Ashcroft and Mermin
2. Introduction to Solid State Physics - Kittel
3. Fundamentals of Condensed Matter - Cohen and Louie
4. 
