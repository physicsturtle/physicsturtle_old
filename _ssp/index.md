---
layout: page
title: Introduction to Solid State Physics
permalink: /physics/ssp/
banner: ssp.svg
---

Welcome to Quantum Mechanics I

<a class="page-link" href="/ssp/introduction">Introduction - Solid State Physics? </a>


{% assign unitNames = "Unit 1 - Crystallography, Unit 2 - Phonons, Unit 3 - Free Electron Model, Unit 4 - Nearly Free Electron Model, Unit 5 - Tight Binding Model, Unit 6 - Semiconductors, Unit 7 - Metals, Unit 8 - Superconductivity" | split: ', ' %}

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
