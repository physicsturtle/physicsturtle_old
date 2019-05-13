---
name: calculus-III/
layout: course
title: Calculus III - Multivariable and Vector Calculus
permalink: /calculus-III/
banner: calculus-III.png
---

Welcome to Multi-Variable and Vector Calculus. This is a really exciting subject and is the first step into allowing one to tackle real world physics and engineering problems. 

This course is a **work in progress**. The goal is for it to be finished by the end of December 2019. 

Sections marked with an asterisk * should be regarded as optional, and everything else as essential. The ones chosen to be marked with an asterisk are ones which are normally left out of multivariable calculus courses, but may be included in an honours course. One of the goals is to be able to cater to as wide of an audience as possible, and for this reason those sections were written.

Solutions to all exercises will eventually be written, even if they aren't available at the moment.

This is a course on calculus, *not analysis*, and will be treated as such. The idea is for everybody to understand how to compute important quantities and objects in multivariable calculus, and to understand the concepts without proof and be able to interpret things geometrically.

Often, after a student takes his/her vector calculus course, the student is unable to do the computations necessary for a course in, for example, electromagnetism or quantum mechanics. We aim to have examples and exercises here that will allow the student to perform such calculations.

<a class="page-link" href="/calculus-III/introduction">Introduction - What is Multivariable Calculus? </a>

<a class="page-link" href="/calculus-III/prerequisites"> Prerequisites</a>

<a class="page-link" href="/calculus-III/learning-outcomes"> Learning Outcomes</a>

<ul>
<li>  <a class="page-link" href="/calculus-III/unit1/"> Unit 1 - Introduction to 3D Space and Vectors </a> </li>
<ol>
{% assign lessonNames = "Three-Dimensional-Cartesian-Coordinates, Vectors-and-Their-Geometry" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit1/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li>  <a class="page-link" href="/calculus-III/unit2/"> Unit 2 - Space Curves </a> </li>
<ol>
{% assign lessonNames = "" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit2/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li>  <a class="page-link" href="/calculus-III/unit3/"> Unit 3 - Partial Differentiation </a> </li>
<ol>
{% assign lessonNames = "" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit3/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li>  <a class="page-link" href="/calculus-III/unit4/"> Unit 4 - Multiple Integration </a> </li>
<ol>
{% assign lessonNames = "" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit4/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li>  <a class="page-link" href="/calculus-III/unit5/"> Unit 5 - Vector Calculus </a> </li>
<ol>
{% assign lessonNames = "Maxwell's-Equations" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit5/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li> <a class="page-link" href="/calculus-III/supplement/"> Supplementary Material </a> </li>
<ol>
{% assign lessonNames = "Chain-Rules, Coordinate-Change-Tensor, Coordinate-Change, Curvilinear-Coordinates, Notation, Product-Rules" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
<li> <a class = "page-link" href = "{{ lessonName | prepend: "supplement/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
</ul>


**Sources**

1. Calculus, 7 ed. - Stewart, James (2012)
2. Vector Analysis - Spiegel, Murray R. (1959)
3. Differential Geometry of Curves and Surfaces - 2 ed. do Carmo, Manfredo (2016)
4. Calculus on Manifolds - Spivak, Michael (1965)
