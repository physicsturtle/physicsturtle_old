---
layout: course
title: Calculus I - In Progress
permalink: /calculus-I/
banner: calculus-I.svg
---

Welcome to Calculus I, single variable differential calculus! This is generally a student's first exposure to post-secondary mathematics, and success in this course is crucial to further studies in mathematics or science. Calculus is the language of physics and engineering, but is also a beautiful subject to study on its own. 

<a class="page-link" href="/calculus-I/introduction"> Introduction - What is Calculus? </a>

The prerequisites are as follows
1. A strong background in high school mathematics, including trigonometry, solving algebraic equations, working with exponentials and logarithms, and graphing.
2. An exposure to physics is useful; many examples will be drawn from physics. 

{% assign unitNames = "Unit 1 - Sets and Functions, Unit 2 - Limits and Continuity, Unit 3 - Differentiation, Unit 4 - Applications of Differentiation" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/" | split: ', ' %}

{% assign lessonNames1 = "Sets, Functions, Inverse-Functions" | split: ', ' %}

{% assign lessonNames2 = "Limits, Limit-Laws, Limit-Details, Squeeze-Theorem, Continuity, Intermediate-Value-Theorem, Limits-at-Infinity, Tangent-Problem" | split: ', ' %}

{% assign lessonNames3 = "Derivatives-and-Rate-of-Change, Definition-of-the-Derivative, Derivatives-of-Polynomials, Product-Rule, Quotient-Rule, Derivatives-of-Trigonometric-Functions, Derivatives-of-Exponential-Functions, Derivatives-of-Hyperbolic-Functions*, Chain-Rule, Implicit-Differentiation, Derivatives-of-Logarithmic-Functions, Derivatives-of-Inverse-Trigonometric-Functions, Derivatives-of-Inverse-Hyperbolic-Functions*, Logarithmic-Differentiation, Linear-Approximations-and-Differentials, Taylor-Polynomials, Lagrange-Remainder-Theorem" | split: ', ' %}

{% assign lessonNames4 = "Kinematics-Problems, Newton's-Law-of-Cooling, Exponential-Growth-and-Decay, Related-Rates, Extrema-1, Extrema-2, The-Mean-Value-Theorem, Curve-Sketching-1, Curve-Sketching-2, Optimization-Problems, L'Hopital's-Rule, Newton's-Method, Antiderivatives" | split: ', ' %}

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
