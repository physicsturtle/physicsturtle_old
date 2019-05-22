---
name: emptyCourse/
layout: course
title: Empty Course
permalink: /emptyCourse/
banner: banner.png
---

Welcome to EmptyCourse

<a class="page-link" href="/emptyCourse/introduction">Introduction - What is Multivariable Calculus? </a>

<a class="page-link" href="/emptyCourse/prerequisites"> Prerequisites</a>

<a class="page-link" href="/emptyCourse/learning-outcomes"> Learning Outcomes</a>

<ul>
<li>  <a class="page-link" href="/emptyCourseI/unit1/"> Unit 1 - Placeholder </a> </li>
<ol>
{% assign lessonNames = "Placeholder1, Placeholder2" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: "unit1/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
<li> <a class="page-link" href="/emptyCourse/supplements/"> Supplementary Material </a> </li>
<ol>
{% assign lessonNames = "Placeholder1, Placeholder 2" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
<li> <a class = "page-link" href = "{{ lessonName | prepend: "unit1/" | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
</ul>


**Sources**

1. Placeholder1 
2. Placeholder2
