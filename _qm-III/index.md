---
layout: page
title: Quantum Mechanics III
permalink: /qm-III/
banner: qm-III.svg
---

Welcome to Quantum Mechanics III, or, a first course in graduate quantum mechanics. A lot of the same topics as were covered in undergraduate quantum mechanics will be covered, but with a greater level of abstraction and rigour; it is expected that the reader can make the ideas concrete by relating them to example systems from undergraduate quantum mechanics. 

- Course outline.
- The Stern-Gerlach experiment.
- The framework for quantum mechanics: Hilbert spaces, linear operators
- foundations of quantum mechanics. 1. The measurement problem.
- foundations of quantum mechanics. 2. Bell inequalities and Kochen-Specker theorem.
- Measurement in quantum mechanics - the Born rule. Compatible and incompatible observables.
- The uncertainty principle and the Heisenberg uncertainty relation.
- The Schroedinger equation.
- Unitarity. The Heisenberg picture. The Schroedinger wave equation.
- The harmonic oscillator.
- Mixed states. The no-cloning theorem. Imposibility of superluminal communication in quantum mechanics.
- The theory of angular momentum (1).
- The theory of angular momentum (2).
- The theory of angular momentum (3). Lecture given by Dr. T.C. Wei.
- The theory of angular momentum (4).
- The theory of angular momentum (5).
- The theory of angular momentum (6).
- The theory of angular momentum (7).
- Discrete symmetries: Parity and discrete translations.
- Discrete symmetries: Time reversal.
- Time-independent perturbation theory, non-degenerate case. The quadratic Stark effect.
- Time-independent perturbation theory, degenerate case. The linear Stark effect.
- The WKB approximation.
- Approximation: Variational methods.
- Time-dependent potentials - the interaction picture. Time-dependent perturbation theory.
- Time-dependent perturbation theory continued. Fermi's golden rule.
- Identical particles. The symmetrization postulate. Bosons, fermions, Pauli exclusion principle.
- The spin-statistics theorem. Two-electron systems. Exchange density. Ortho and para-helium.
- Scattering theory. The Lippmann-Schwinger formalism. Methods: the Cauchy residue theorem.
- Scattering theory continued. The Born-Oppenheimer approximation. Examples: Scattering off a Yukawa and Coulomb potential. Higher-order Born-Oppenheimer approximation.
- Scattering theory continued. The optical theorem.
- Classical and quantum cryptography. Classical: the Vernam pad, Diffie-Hellman public key exchange. Quantum: the Bennett-Brassard protocol (BB84).

<a class="page-link" href="/qm-I/introduction">Quantum Mechanics III </a>


{% assign unitNames = "Unit 1 - , Unit 2 - , Unit 3 - , Unit 4 - , Unit 5 - , Unit 6 - " | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, unit6/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

{% assign lessonNames5 = "" | split: ', ' %}

{% assign lessonNames6 = "" | split: ', ' %}

<ul>
{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex == 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex == 3 %}  {% assign lessonNames = lessonNames4 %}
{% elsif unitIndex == 4 %}  {% assign lessonNames = lessonNames5 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '@', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. 
