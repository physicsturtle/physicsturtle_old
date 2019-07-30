---
layout: course
title: Ordinary Differential Equations I
banner: ode-I.svg
---

Welcome to Ordinary Differential Equations I. 

The prerequisites are as follows:
1. Single variable differential and integral calculus.
2. A first course in linear algbera
3. An exposure to physics is useful; many examples will be drawn from physics. 
4. A concurrent course in multivariable calculus will be useful

Notation and conventions used in this course are here

<a class = "page-link" href = "/ode-I/notation"> Notation and Conventions </a>

{% assign unitNames = "Unit 1 - What are Differential Equations?, Unit 2 - First Order Differential Equations, Unit 3 - Second Order Differential Equations, Unit 4 - Higher Order Differential Equations, Unit 5 - Laplace Transform, Unit 6 - Linear Systems of Differential Equations, Unit 7 - Nonlinear Systems of Differential Equations" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, unit6/, unit7/" | split: ', ' %}

{% assign lessonNames1 = "Introduction, Classification, Slope_Fields" | split: ', ' %}

{% assign lessonNames2 = "Separable_Equations, First_Order_Inhomogeneous_Equations, Exact_Equations, First_Order_Nonlinear_Equations, Autonomous_Equations, Existence_and_Uniqueness" | split: ', ' %}

{% assign lessonNames3 = "Constant_Coefficients, Wronskian, Undetermined_Coefficients, Reduction_of_Order, Variation_of_Parameters" | split: ', ' %}

{% assign lessonNames4 = "Constant_Coefficients, Undetermined_Coefficients, Variation_of_Parameters" | split: ', ' %}

{% assign lessonNames5 = "Definitions, Inverse_Transform, Derivatives, Heaviside_Function, Dirac_Delta_Function, Convolution" | split: ', ' %}

{% assign lessonNames6 = "Linear_Systems, Fundamental_Matrix, Inhomogeneous_Systems" | split: ', ' %}

{% assign lessonNames7 = "Stability" | split: ', ' %}


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
{% elsif unitIndex == 6 %}  {% assign lessonNames = lessonNames7 %}
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
2. Schaums Outline of Calculus, 4 ed. - Ayres Jr., Frank (2002)
3. Calculus - Spivak, Michael 
4. Calculus, Vol. 1 - Apostol, Tom 
