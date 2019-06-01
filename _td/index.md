---
layout: course
title: Thermodynamics
permalink: /thermodynamics/
---

In my experience, thermodynamics is often skimmed over at the undergraduate level, causing many problems when students are later expected to learn concepts in statistical physics or condensed matter physics. 

<a class="page-link" href="/physics/electromagnetism-I/introduction">Introduction </a>

<ul>
<li>  <a class="page-link" href="/math/calculus-III/"> Unit I </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.category == "td-I"%}
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

### References:
1. Concepts in Thermal Physics, by Stephen J. Blundell and Katherine M. Blundell
2. Thermal Physics, by Daniel Schroeder
3. Thermodynamics, by Enrico Fermi
4. Thermal Physics, by Charles Kittel
