---
layout: page
title: Vector Calculus
course: calculus-III
unit: unit5
---

Unit 5 studies the last kind of function between sets of real numbers. That is, functions which take a vector input and give a vector output. In symbols, this is functions like 

$$ f: \mathbb{R}^n \to \mathbb{R}^m$$

we will be considering functions where \\(n = m = 2\\) or \\(n = m = 3\\). These kinds of functions are known as *vector fields*. 

{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit5" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
