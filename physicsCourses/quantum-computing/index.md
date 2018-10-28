---
layout: page
title: Quantum Computing 
permalink: /physics/quantum-computing/
---

Hey everyone! Welcome to your first rigorous course on quantum mechanics. You will likely have already taken a course on modern physics, which introduces the basics of quantum mechanics, special relativity, and various other discoveries in the early 1900s. This course will review the quantum mechanics that you were exposed to before, as well as go in to much more depth on the basics of quantum mechanics. This course will demand many more mathematical skills than your modern physics course, but we will make an effort to go through all of the derivations carefully so that you can follow all the steps. 

<a class="page-link" href="/physics/quantum-mechanics-I/introduction">Introduction </a>

<a class="page-link" href="/physics/quantum-mechanics-I/prerequisites"> Prerequisites</a>

<a class="page-link" href="/physics/quantum-mechanics-I/learning-outcomes"> Learning Outcomes</a>

<ul>
<li>  <a class="page-link" href="/physics/quantum-mechanics-I/unit1/"> Unit I </a> </li>
<ol>
{% for my_page in site.pages %}
{% if  my_page.course == "quantum-mechanics-I" and my_page.unit == "unit1" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
</ol>
</ul>

