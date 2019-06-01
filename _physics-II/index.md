---
layout: course
title: Physics II
permalink: /physics-II/
banner: physics-II.svg
---

Welcome to your first course on Physics!

<a class="page-link" href="/physics/intro-to-physics/introduction">Introduction - What is Physics? </a>

<ul>
<li>  <a class="page-link" href="/physics/intro-to-physics/unit1/"> Unit 1 - Introduction to 3D Space and Vectors </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "intro-to-physics" and my_page.unit == "unit1" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/physics/intro-to-physics/unit2/"> Unit 2 - Plane and Space Curves </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "intro-to-physics" and my_page.unit == "unit2" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/physics/intro-to-physics/unit3"> Unit 3 - Partial Differentiation </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "intro-to-physics" and my_page.unit == "unit3" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/physics/intro-to-physics/unit4/"> Unit 4 - Multiple Integration </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "intro-to-physics" and my_page.unit == "unit4" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/physics/intro-to-physics/unit5/"> Unit 5 - Vector Calculus </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "intro-to-physics" and my_page.unit == "unit5" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li> <a class="page-link" href="/physics/intro-to-physics/supplements/"> Supplementary Material </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "intro-to-physics" and my_page.unit == "supplement" and my_page.layout == "lesson" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
</ul>


**Sources**
1. Calculus - 7 ed. Stewart, James (2012)
2. Vector Analysis - Spiegel, Murray R. (1959)
3. Differential Geometry of Curves and Surfaces - 2 ed. do Carmo, Manfredo (2017)
