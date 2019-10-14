---
layout: page
title: Quantum Mechanics II
banner: qm-II.svg
---

Welcome to Quantum Mechanics II. 

<a class = "page-link" href = "/qm-II/notation"> Notation and Conventions </a>

{% assign unitNames = " Unit 1 - Fundamentals, Unit 1 - Time Independent Perturbation Theory, Unit 2 - The Variational Principle, Unit 3 - WKB Approximation, Unit 4 - Time Dependent Perturbation Theory, Unit 5 - Adiabatic Approximation, Unit 6 - Scattering Theory" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "The_Schrödinger_Equation" | split: ', ' %}

{% assign lessonNames2 = "First_Order_Perturbation_Theory, Second_Order_Perturbation_Theory, Degenerate_Perturbation_Theory, Fine_Structure, Hyperfine_Structure, Zeeman_Effect, " | split: ', ' %}

{% assign lessonNames3 = "Theory, Helium_Atom, Hydrogen_Molecule" | split: ', ' %}

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

1. Introduction to Quantum Mechanics, Griffiths
2. Modern Quantum Mechanics, Sakurai
3. Principles of Quantum Mechanics, Shankar
4. Quantum Mechanics of One and Two Electron Atoms, Salpeter and Bethe
