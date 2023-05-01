---
layout: page
title: Many Body Physics II
banner: many-body-II.svg
permalink: /many-body-II/
---
<a class="page-link" href="/many-body-II/introduction">Many Body Physics II </a>

{% assign unitNames = "Unit 1 - Introduction to the Path Integral, Unit 2 - Bosonic Coherent State Path Integral, Unit 3 - Fermionic Coherent State Path Integral, Unit 4 - Zero Temperature Path Integrals, Unit 5 - Fermionic Path Integrals, Unit 6 - Feynman Diagrams for Interacting Fermions: the Jellium Model, Unit 7 - Fermi Liquid Theory, Unit 8 - Bose Hubbard Model, Unit 9 - The Fermi-Hubbard Model: Electron-Electron Interactions, Unit 10 - Fermi Hubbard Model, Unit 11 - Electron-Phonon Interaction, Unit 12 - Feynman Diagrams for Electron-Phonon Interactions, Unit 13 - The Kondo Impurity Model, Unit 14 - Conductivity - Detailed Treatment, Unit 15 - Formalism of RG, Unit 16 - Interacting Fermions in 1 Dimension, Unit 17 - Bosonization (constructive), Unit 18 - Nonabelian Bosonization, Unit 19 - Bosonization (me), Unit 20 - affleck Bosonization, Unit 21 - Lecture March 15, Unit 22 - Lecture March 20, Unit 23 - RG for Interacting Fermions in \\(d = 2\\) and \\(d = 3\\), Unit 24 - Lecture March 22, Unit 25 - March 27 Lecture, Unit 26 - Lecture March 29, Unit 27 - Spin Models, Unit 28 - Spin Coherent State Path Integrals, Unit 29 - Models of Electron-Phonon Coupling, Unit 30 - Superconductivity Beyond \\(s\\)-wave: the \\(t\\)-\\(J\\) Model, Unit 31 - Periodic Anderson and Kondo Lattice Model, Unit 32 - Superconductivity and Superfluidity, Unit 33 - Gauge Theories, Unit 34 - Renormalization Group for Interaction Fermions: 2 dimensions, Unit 35 - Appendix, Unit 36 - Mathematical Results and Conventions, "| split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, unit6/, unit7/, unit8/, unit9/, unit10/, unit11/, unit12/, unit13/, unit14/, unit15/, unit16/, unit17/, unit18/, unit19/, unit20/, unit21/, unit22/, unit23/, unit24/, unit25/, unit26/, unit27/, unit28/, unit29/, unit30/, unit31/, unit32/, unit33/, unit34/, unit35/, unit36/, " | split: ', ' %}

{% assign lessonNames1 = "Real Space Path Integral, " | split: ', ' %}
{% assign lessonNames2 = "Review of Coherent States, Bosonic Coherent States, Resolution of Identity and Trace, The Bosonic Coherent State Path Integral, Coherent state stuff, " | split: ', ' %}
{% assign lessonNames3 = "Grassman Numbers, Fermionic Coherent States, Resolution of Identity and Trace, Many-Particle Hilbert Space -- Occupation Number Basis, Determinant formula, Path Integral for a Single Fermionic Oscillator, Path Integral for a Fermionic Field Theory, Feynman Rules, Relation Between Path Integral and Canonical Quantization, " | split: ', ' %}
{% assign lessonNames4 = "" | split: ', ' %}
{% assign lessonNames5 = "The Fermionic Oscillator, " | split: ', ' %}
{% assign lessonNames6 = "Single Particle Green Function, Self Energy, Vertex Function, " | split: ', ' %}
{% assign lessonNames7 = "Self-Energy in the Random Phase Approximation, Vertex Function in the Random Phase Approximation??, Scattering Rate, Resistivity, Heat Capacity, Magnetic Susceptibility, Landau Parameters, " | split: ', ' %}
{% assign lessonNames8 = "Weakly interacting superfluid, " | split: ', ' %}
{% assign lessonNames9 = "" | split: ', ' %}
{% assign lessonNames10 = "Spin Density Wave Order, Charge Density Wave Order, Mott Transition, Pairing and Superconductivity, " | split: ', ' %}
{% assign lessonNames11 = "Fröhlich Hamiltonian, " | split: ', ' %}
{% assign lessonNames12 = "" | split: ', ' %}
{% assign lessonNames13 = "Kondo Hamiltonian, Effective Action of the Kondo Model (my notes), Effective Action of the Kondo Model, Conduction electron Green function for Kondo effect, " | split: ', ' %}
{% assign lessonNames14 = "" | split: ', ' %}
{% assign lessonNames15 = "Low Energy Fixed Point of Kondo Model, Irrelevant Operator Corrections to Low Energy Fixed Point, " | split: ', ' %}
{% assign lessonNames16 = "Taking the Thermodynamic Limit, " | split: ', ' %}
{% assign lessonNames17 = "Bosonic Fock Space, Klein Factors, Boson Fields -- definition and properties, Action on a generic state \\(\ket{\textbf{N_0\\) , Action on a generic state \\(\ket{\textbf{N\\) , Important Bosonization Formulas, Hamiltonian with Linear Dispersion, Green Functions for Hamiltonian with Linear Dispersion, " | split: ', ' %}
{% assign lessonNames18 = "Abelian Bosonization Reframing, Wick's Theorem, The OPE, Commutator of Fourier modes, The Stress-Energy Tensor and more OPEs, Tomonaga Form of Hamiltonian, Spin charge separation, " | split: ', ' %}
{% assign lessonNames19 = "Massless Dirac Fermion, Massless Scalar Boson, Fermion-Boson Mapping, " | split: ', ' %}
{% assign lessonNames20 = "" | split: ', ' %}
{% assign lessonNames21 = "" | split: ', ' %}
{% assign lessonNames22 = "" | split: ', ' %}
{% assign lessonNames23 = "" | split: ', ' %}
{% assign lessonNames24 = "\\(\D=3\\) case spherical fermi surface. , " | split: ', ' %}
{% assign lessonNames25 = "1 loop RG in \\(D = 2,3\\), " | split: ', ' %}
{% assign lessonNames26 = "" | split: ', ' %}
{% assign lessonNames27 = "Heisenberg Model, Dzyaloshinskii-Moriya Interaction, Abrikosov Pseudofermions, Schwinger Bosons, " | split: ', ' %}
{% assign lessonNames28 = "Path Integral, " | split: ', ' %}
{% assign lessonNames29 = "" | split: ', ' %}
{% assign lessonNames30 = "Pairing and Superconductivity, " | split: ', ' %}
{% assign lessonNames31 = "RKKY Interaction, " | split: ', ' %}
{% assign lessonNames32 = "Gap Equation, Mean-Field Theory, Heat Capacity, " | split: ', ' %}
{% assign lessonNames33 = "State Space and Gauge Equivalence Classes, Gauge Theory Without Gauge Field 1, Gauge Theory Without Gauge Field 2, " | split: ', ' %}
{% assign lessonNames34 = "" | split: ', ' %}
{% assign lessonNames35 = "Fourier Transforms, Examples, Multi-Dimensional Generalizations, Summary, " | split: ', ' %}
{% assign lessonNames36 = "Fourier Transforms, Cumulant Expansion, Complex Analysis, Hubbard-Stratonovich Transform, " | split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex== 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex== 3 %}  {% assign lessonNames = lessonNames4 %}
{% elsif unitIndex== 4 %}  {% assign lessonNames = lessonNames5 %}
{% elsif unitIndex== 5 %}  {% assign lessonNames = lessonNames6 %}
{% elsif unitIndex== 6 %}  {% assign lessonNames = lessonNames7 %}
{% elsif unitIndex== 7 %}  {% assign lessonNames = lessonNames8 %}
{% elsif unitIndex== 8 %}  {% assign lessonNames = lessonNames9 %}
{% elsif unitIndex== 9 %}  {% assign lessonNames = lessonNames10 %}
{% elsif unitIndex== 10 %}  {% assign lessonNames = lessonNames11 %}
{% elsif unitIndex== 11 %}  {% assign lessonNames = lessonNames12 %}
{% elsif unitIndex== 12 %}  {% assign lessonNames = lessonNames13 %}
{% elsif unitIndex== 13 %}  {% assign lessonNames = lessonNames14 %}
{% elsif unitIndex== 14 %}  {% assign lessonNames = lessonNames15 %}
{% elsif unitIndex== 15 %}  {% assign lessonNames = lessonNames16 %}
{% elsif unitIndex== 16 %}  {% assign lessonNames = lessonNames17 %}
{% elsif unitIndex== 17 %}  {% assign lessonNames = lessonNames18 %}
{% elsif unitIndex== 18 %}  {% assign lessonNames = lessonNames19 %}
{% elsif unitIndex== 19 %}  {% assign lessonNames = lessonNames20 %}
{% elsif unitIndex== 20 %}  {% assign lessonNames = lessonNames21 %}
{% elsif unitIndex== 21 %}  {% assign lessonNames = lessonNames22 %}
{% elsif unitIndex== 22 %}  {% assign lessonNames = lessonNames23 %}
{% elsif unitIndex== 23 %}  {% assign lessonNames = lessonNames24 %}
{% elsif unitIndex== 24 %}  {% assign lessonNames = lessonNames25 %}
{% elsif unitIndex== 25 %}  {% assign lessonNames = lessonNames26 %}
{% elsif unitIndex== 26 %}  {% assign lessonNames = lessonNames27 %}
{% elsif unitIndex== 27 %}  {% assign lessonNames = lessonNames28 %}
{% elsif unitIndex== 28 %}  {% assign lessonNames = lessonNames29 %}
{% elsif unitIndex== 29 %}  {% assign lessonNames = lessonNames30 %}
{% elsif unitIndex== 30 %}  {% assign lessonNames = lessonNames31 %}
{% elsif unitIndex== 31 %}  {% assign lessonNames = lessonNames32 %}
{% elsif unitIndex== 32 %}  {% assign lessonNames = lessonNames33 %}
{% elsif unitIndex== 33 %}  {% assign lessonNames = lessonNames34 %}
{% elsif unitIndex== 34 %}  {% assign lessonNames = lessonNames35 %}
{% elsif unitIndex== 35 %}  {% assign lessonNames = lessonNames36 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', '' %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>
**Sources**
