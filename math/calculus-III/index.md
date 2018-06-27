---
layout: course
title: Calculus III - Multivariable and Vector Calculus
permalink: /math/calculus-III/
banner: calculus-III.png
---

Hey everyone! Welcome to Multi-Variable and Vector Calculus. This subject is super important, and you'll soon come to realize it has many applications pretty much anywhere you look. It is also a great step to bridge your first year calculus knowledge with some other areas of math, such as linear algebra and geometry. If you haven't had much experience with those areas of math, we'll explain some of that along the way.


<a class="page-link" href="/math/calculus-III/introduction">Introduction </a>

<ul>
<li>  <a class="page-link" href="/math/calculus-III/unit1/"> Unit I </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit1" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/math/calculus-III/"> Unit 3 </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit3" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li> <a class="page-link" href="/math/supplements/"> Supplementary Material </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "supplement" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
</ul>

