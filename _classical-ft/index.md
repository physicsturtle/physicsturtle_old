---
layout: course
title: Classical Field Theory
permalink: /classical-ft/
banner: classical-ft.svg
---

Welcome to Classical Field Theory, a subject which is severely undertaught in undergraduate and graduate physics programs. 

<a class="page-link" href="/classical-ft/introduction"> Introduction - What is Classical Field Theory? </a>

The prerequisites are as follows
1. An excellent background in electromagnetic theory
2. A working knowledge of continuum mechanics (fluid mechanics and elasticity)
3. A working knowledge of multivariable and vector calculus
4. A working knowledge of complex analysis

{% assign unitNames = "Unit 1 - Sets and Functions, Unit 2 - Limits and Continuity, Unit 3 - Differentiation, Unit 4 - Applications of Differentiation" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/" | split: ', ' %}

{% assign lessonNames1 = "Sets, Functions, Inverse_Functions" | split: ', ' %}

{% assign lessonNames2 = "Limits, Limit_Laws, Limit_Details, Squeeze_Theorem, Continuity, Intermediate-Value-Theorem, Limits_at_Infinity, Tangent_Problem" | split: ', ' %}

{% assign lessonNames3 = "Derivatives_and_Rate_of_Change, Definition_of_the_Derivative, Derivatives_of_Polynomials, Product_Rule, Quotient_Rule, Derivatives_of_Trigonometric_Functions, Derivatives_of_Exponentials, Derivatives_of_Hyperbolic_Functions*, Chain_Rule, Implicit_Differentiation, Derivatives_of_Logarithms, Derivatives_of_Inverse_Trigonometric_Functions, Derivatives_of_Inverse_Hyperbolic_Functions*, Logarithmic_Differentiation, Linear_Approximations_and_Differentials, Taylor_Polynomials, Lagrange_Remainder_Theorem" | split: ', ' %}

{% assign lessonNames4 = "Kinematics_Problems, Newton's_Law_of_Cooling, Exponential_Growth_and_Decay, Related_Rates, Extrema_1, Extrema_2, The_Mean_Value_Theorem, Curve_Sketching_1, Curve-Sketching_2, Optimization_Problems, L'Hopital's_Rule, Newton's_Method, Antiderivatives" | split: ', ' %}

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

1. Classical Theory of Fields - Landau and Liftshitz
2. Electrodynamics and Classical Theory of Fields and Particles - Barut
3. 
