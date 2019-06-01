---
name: nonlin-dyn-I/
layout: course
title: Nonlinear Dynamics and Chaos I
permalink: /nonlin-dyn-I/
banner: nonlin-dyn-I.svg
---

Welcome to EmptyCourse

<a class="page-link" href="/nonlin-dyn-I/introduction">Introduction to Chaos Theory </a>

<a class="page-link" href="/nonlin-dyn-I/prerequisites"> Prerequisites</a>

<a class="page-link" href="/nonlin-dyn-I/learning-outcomes"> Learning Outcomes</a>

<ul>
<li>  <a class="page-link" href="/nonlin-dyn-I/unit1/"> Unit 1 - Placeholder </a> </li>
<ol>
{% assign lessonNames = "One-Dimensional-Systems, Placeholder2" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit1/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li> <a class="page-link" href="/nonlin-dyn-I/supplements/"> Supplementary Material </a> </li>
<ol>
{% assign lessonNames = "Placeholder1, Placeholder 2" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
<li> <a class = "page-link" href = "{{ lessonName | prepend: "supplement/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
</ul>


**Sources**

1. Placeholder1 
2. Placeholder2
