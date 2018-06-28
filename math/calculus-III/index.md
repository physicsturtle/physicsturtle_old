---
layout: course
title: Calculus III - Multivariable and Vector Calculus
permalink: /math/calculus-III/
banner: calculus-III.png
---

Welcome to Multi-Variable and Vector Calculus. This is a really exciting subject and is the first step into allowing one to tackle real world physics and engineering problems. 

This course is a **work in progress**. The goal is for it to be finished by the end of December 2018. 

<a class="page-link" href="/math/calculus-III/introduction">Introduction - What is Multivariable Calculus? </a>

<ul>
<li>  <a class="page-link" href="/math/calculus-III/unit1/"> Unit 1 - Introduction to 3D Space and Vectors </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit1" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/math/calculus-III/unit2/"> Unit 2 - Plane and Space Curves </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit2" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/math/calculus-III/"> Unit 3 - Partial Differentiation </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit3" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/math/calculus-III/unit1/"> Unit 4 - Multiple Integration </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit4" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/math/calculus-III/unit1/"> Unit 5 - Vector Calculus </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit5" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li> <a class="page-link" href="/math/supplements/"> Supplementary Material </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "supplement" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
</ul>


**Sources**
1. Calculus - 7 ed. Stewart, James (2012)
2. Vector Analysis - Spiegel, Murray R. (1959)
3. Differential Geometry of Curves and Surfaces - 2 ed. do Carmo, Manfredo (2017)
