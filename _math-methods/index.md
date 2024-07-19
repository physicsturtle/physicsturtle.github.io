---
layout: course
title: Mathematical Methods in Physics
banner: math-methods.svg
---

Welcome to Mathematical Methods in Physics! 

{% assign unitNames = "Unit 1 - Partial Differential Equations, Unit 2 - Green's Functions, Unit 3 - Complex Variables, Unit 4 - Fourier Analysis, Unit 5 - Calculus of Functionals, Unit 6 - Calculus of Variations, Unit 7 - Integral Equations, Unit 8 - Linear Algebra, Unit 9 - Group Theory, Unit 10 - Differential Geometry, Unit 11 - Lie Theory, Unit 12 - Topology" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, unit6/, unit7/, unit8/, unit9/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

{% assign lessonNames5 = "" | split: ', ' %}

{% assign lessonNames6 = "" | split: ', ' %}

{% assign lessonNames8 = "Riemann_Curvature_Tensor" | split: ', ' %}

{% assign lessonNames9 = "" | split: ', ' %}

{% assign lessonNames10 = "" | split: ', ' %}

{% assign lessonNames11 = "" | split: ', ' %}

{% assign lessonNames12 = "" | split: ', ' %}

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
{% elsif unitIndex == 6 %}  {% assign lessonNames = lessonNames7 %}
{% elsif unitIndex == 7 %}  {% assign lessonNames = lessonNames8 %}
{% elsif unitIndex == 8 %}  {% assign lessonNames = lessonNames9 %}
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

1. Partial Differential Equations - Strauss
2. Applied Partial Differential Equations - Haberman
3. Partial Differential Equations of Applied Mathematics - Zauderer
4. Complex Variables and Applications - Churchill and Brown
5. Fourier Series - Tolstov
6. Calculus of Variations - Weinstock
7. Contemprary Abstract Algebra - Gallian
8. Introduction to Smooth Manifolds - Lee
9. Curvature in Mathematics and Physics - Sternberg
10. Riemannian Manifolds - Lee
11. Naïve Lie Theory - Stillwell
12. Topology - Munkres
13. Introduction to Topological Manifolds - Lee
