---
layout: course
title: Calculus I
banner: calculus-I.svg
permalink: /calculus-I/
---
{% assign unitNames = "Unit 1 - Sets and Functions, Unit 2 - Limits and Continuity, Unit 3 - Differentiation, Unit 4 - Applications of Differentiation, Unit 5 - Problems to be sorted, "| split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, " | split: ', ' %}

{% assign lessonNames1 = "Sets , Functions , " | split: ', ' %}
{% assign lessonNames2 = "" | split: ', ' %}
{% assign lessonNames3 = "" | split: ', ' %}
{% assign lessonNames4 = "" | split: ', ' %}
{% assign lessonNames5 = "" | split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex== 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex== 3 %}  {% assign lessonNames = lessonNames4 %}
{% elsif unitIndex== 4 %}  {% assign lessonNames = lessonNames5 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', '' %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>
**Sources**
