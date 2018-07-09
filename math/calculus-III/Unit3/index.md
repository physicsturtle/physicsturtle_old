---
layout: page
title: Partial Differentiation 
course: calculus-III
unit: unit3
---

Unit 3 introduces the idea of functions which take multiple real numbers as inputs, but output a single real number as output. In symbols, this means functions like:

$$ f : \mathbb{R}^n \to \mathbb{R}$$


{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit3" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
