---
name: calculus-III/
layout: course
title: Calculus III - Multivariable and Vector Calculus
permalink: /calculus-III/
banner: calculus-III.png
---

Welcome to Multi-Variable and Vector Calculus. This is a really exciting subject and is the first step into allowing one to tackle real world physics and engineering problems. 

This course is a **work in progress**. The goal is for it to be finished by the end of December 2018. Sections with ALL CAPITALS are in progress, those in normal text are complete.

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
{% assign lessonNames = "Three-Dimensional-Cartesian-Coordinates, Vectors-and-Their-Geometry, Algebraic-Operations-with-Vectors, Norm, Projections, Dot-Product, Determinant-and-Cross-Product, Equations-of-Lines, Equations-of-Planes, Quadric-Surfaces, Cylindrical-Coordinates, Spherical-Coordinates, General-Surfaces" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit1/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li>  <a class="page-link" href="/calculus-III/unit2/"> Unit 2 - Space Curves </a> </li>
<ol>
{% assign lessonNames = "Vector-Functions, Limits-and-Continuity, Differentiation-and-Integration-of-Curves, Arc-Length, Curvature-and-Torsion, Frenet-Serret-Equations" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit2/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li>  <a class="page-link" href="/calculus-III/unit3/"> Unit 3 - Partial Differentiation </a> </li>
<ol>
{% assign lessonNames = "Functions-of-Multiple-Variables, Contour-Plots-and-Level-Sets, Limits-and-Continuity, Partial-Differentiation, Tangent-Planes-and-Linear-Approximations, Gradient-Vector, The-Differential, Non-Independent-Variables, Chain-Rule, Differentiation-of-Integrals, Directional-Derivative, Extrema-1, Extrema-2, Lagrange-Multipliers-1, Lagrange-Multipliers-2, Bordered-Hessian, Lagrange-Remainder, The-Jacobian-Derivative, Higher-Dimensional-Lagrange-Multipliers, Inflection-and-Saddle-Points-Lagrange-Multipliers" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit3/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li>  <a class="page-link" href="/calculus-III/unit4/"> Unit 4 - Multiple Integration </a> </li>
<ol>
{% assign lessonNames = "Riemann-Sums, Double-Integral-Over-a-Rectangle, Double-Integral-Over-a-General-Plane-Region, Double-Integral-in-Polar-Coordinates, Surface-Area, Triple-Integrals, Triples-Integrals-In-Cylindrical-Coordinates, Triple-Integrals-in-Spherical-Coordinates, Change-of-Variables, Applications" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit4/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li>  <a class="page-link" href="/calculus-III/unit5/"> Unit 5 - Vector Calculus </a> </li>
<ol>
{% assign lessonNames = "Vector-Fields, Line-Integrals-in-2D, Fundamental-Theorem-of-Line-Integrals, Green's-Theorem, Divergence, Curl, Laplacian, Surface-Integrals, Stokes-Theorem, Divergence-Theorem, Applications, Flow-of-A-Vector-Field, Maxwell's-Equations, Differential-Forms, Green's-Identities" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit5/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li> <a class="page-link" href="/calculus-III/supplements/"> Supplementary Material </a> </li>
<ol>
{% assign lessonNames = "Three-Dimensional-Cartesian-Coordinates, Vectors-and-Their-Geometry, Algebraic-Operations-with-Vectors, Norm, Projections, Dot-Product, Determinant-and-Cross-Product, Equations-of-Lines, Equations-of-Planes, Quadric-Surfaces, Cylindrical-Coordinates, Spherical-Coordinates, General-Surfaces" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
<li> <a class = "page-link" href = "{{ lessonName | prepend: "unit1/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
</ul>


**Sources**

1. Calculus, 7 ed. - Stewart, James (2012)
2. Vector Analysis - Spiegel, Murray R. (1959)
3. Differential Geometry of Curves and Surfaces - 2 ed. do Carmo, Manfredo (2016)
4. Calculus on Manifolds - Spivak, Michael (1965)
