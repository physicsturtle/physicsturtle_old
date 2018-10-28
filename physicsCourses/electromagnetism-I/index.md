---
layout: course
title: Electromagnetism I
permalink: /physics/electromagnetism-I/
---

Hey everyone! Welcome to Multi-Variable and Vector Calculus. This subject is super important, and you'll soon come to realize it has many applications pretty much anywhere you look. It is also a great step to bridge your first year calculus knowledge with some other areas of math, such as linear algebra and geometry. If you haven't had much experience with those areas of math, we'll explain some of that along the way. 

<a class="page-link" href="/physics/electromagnetism-I/introduction">Introduction </a>

<ul>
<li>  <a class="page-link" href="/math/calculus-III/"> Unit I </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.category == "electromagnetism-I"%}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
<li>  <a class="page-link" href="/math/calculus-III/"> Unit 3 </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.category == "electromagnetism-I" and my_page.id == "unit3" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
</ul>
