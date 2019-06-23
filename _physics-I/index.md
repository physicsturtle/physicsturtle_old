---
layout: course
title: Physics I - Elasticity, Fluids, Thermodynamics, Oscillations, Acoustics
permalink: /physics-I/
banner: physics-I.svg
---

Welcome to your first course on Physics! The first year undergraduate physics curriculum is meant to introduce the student to most areas of study in classical physics, which include classical mechanics, thermodynamics, elasticity, fluids, acoustics, waves, electromagnetism, and optics. In Physics I, we will cover elasticity, fluids, thermodynamics, oscillations, and then acoustics, in that order. In Physics II, we will cover electromagnetism and optics. In Classical Mechanics I, we will have of course classical mechanics. Later in your physics education, you will be exposed to further topics in each of these areas, and a strong understanding of each of these will be very valuable when you eventually move to quantum mechanics.

{% assign unitNames = "Unit 1 - Elasticity, Unit 2 - Fluids, Unit 3 - Thermodynamics, Unit 4 - Oscillations, Unit 5 - Acoustics, Supplementary Material" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

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
{% elsif unitIndex == 4 %}  {% assign lessonNames = lessonNames5 %}
{% elsif unitIndex == 5 %}  {% assign lessonNames = lessonNames6 %}
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

1. 
