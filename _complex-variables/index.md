---
layout: course
title: Complex Variables
permalink: /complex-variables/
banner: complex-variables.svg
---

Welcome to Complex Variables! This course is often called complex analysis, but the level of rigour at which I will present this course does not warrant it being called analysis. 



<a class="page-link" href="/complex-variables/introduction">Introduction - What is Complex analysis? </a>

The prerequisites for this course are
1. A strong background in single variable calculus
2. A strong background in multivariable and vector calculus
3. A basic knowledge of proof writing
4. A basic knowledge of ordinary and partial differential equations

{% assign unitNames = "Unit 1 - Complex Numbers and Algebra, Unit 2 - Mappings and Differentiation, Unit 3 - Integration, Unit 4 - Applications, Unit 5 - Laurent Series and the Calculus of Residues, Unit 6 - Evaluation of Integrals by Contour Integration, Unit 7 - Applications 2" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, unit6/" | split: ', ' %}

{% assign lessonNames1 = "The_Complex_Plane, Complex_Arithmetic, Polar_Representation, Argument, De_Moivre's_Formula, Complex_Inequalities, Roots_of_Unity" | split: ', ' %}

{% assign lessonNames2 = "Elementary_Mappings, Compositions_of_Mappings, Differentiable_Functions, Harmonic_Functions, Multivalued_Functions, Branch_Cuts" | split: ', ' %}

{% assign lessonNames3 = "Contour_integration, Fundamental_Theorem_of_Calculus, Integral_Inequalities, Cauchy-Goursat_Theorem, Cauchy's_Integral_Theorem" | split: ', ' %}

{% assign lessonNames4 = "Nyquist_Criterion, Rouche's_Theorem, Möbius_Transformations, Symmetric_Points, Fluid_Flow, Electromagnetism, Conformal_Mappings, " | split: ', ' %}

{% assign lessonNames5 = "Laurent_Series, " | split: ', ' %}

{% assign lessonNames6 = "Trigonometric_Integrals, Improper_Integrals, Multivalued_Integrands, Integrals_with_Logarithms" | split: ', ' %}

{% assign lessonNames6 = "Infinite_Sums, Laplace_Transform" | split: ', ' %}

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
{% elsif unitIndex == 5 %}  {% assign lessonNames = lessonNames6 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Complex Variables and Applications, Churchill and Brown
