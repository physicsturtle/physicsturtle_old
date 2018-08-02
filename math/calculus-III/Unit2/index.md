---
layout: page
title: Plane and Space Curves 
course: calculus-III
unit: unit2
permalink: /math/calculus-III/unit2/
---

Unit 2 introduces the idea of functions of a single variable with vector valued outputs. In other words, functions which take values in 2D or 3D space instead of along a line. In symbols, this unit will concern functions of the type:

$$ f : I \to \mathbb{R}^n$$

where \\(I\\) is a subset of the real line. It could be a finite interval or even the entire real line. Functions like this look like curves in the plane or in space. If we are looking at curves in the plane, we would have \\(n = 2\\). If we look at curves in 3D space, it would be \\(n = 3\\). Curves in higher dimensions can also be defined, but we won't be looking at such things in these notes.

{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit2" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}

