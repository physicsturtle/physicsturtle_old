---
layout: course
title: Calculus II
banner: calculus-II.svg
---

Welcome to Calculus II, single variable integral calculus!

{% assign unitNames = "Unit 1 - The Integral, Unit 2 - Methods of Integration, Unit 3 - Applications of Integration, Unit 4 - Polar Coordinates, Unit 5 - Sequences and Series" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "Riemann_Sums, The_Definite_Integral, Fundamental_Theorem_of_Calculus" | split: ', ' %}

{% assign lessonNames2 = "Basic_Formulas, Substitution_Rule, Integration_by_Parts, Trigonometric_Integrals, Method_of_Partial_Fractions, Trigonometric_Substitution, Hyperbolic_Substitution*, Improper_Integrals, Numerical_Integration, Miscellaneous_Tricks" | split: ', ' %}

{% assign lessonNames3 = "Area_Between_Curves, Volume_of_Revolution, Work, Average_Value_of_a_Function, Arc_Length, Surface_of_Revolution, Center_of_Mass, Probability, Differential_Equations" | split: ', ' %}

{% assign lessonNames4 = "Polar_Coordinates, Arc_Length_and_Area, Conic_Sections" | split: ', ' %}

{% assign lessonNames5 = "Sequences, Series_and_Divergence_Test, Comparison_Test, Integral_Test, Alternating_Series, Absolute_Convergence, Ratio_and_Root_Tests, Power_Series, Functions_as_Power_Series, Taylor_Series" | split: ', ' %}

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
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Calculus, 7 ed. - Stewart, James (2012)
