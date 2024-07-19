---
name: ode-II/
layout: course
title: Ordinary Differential Equations II
permalink: /ode-II/
banner: ode-II.svg
---

Ordinary Differential Equations II -- In progress

In this course, we continue with more methods for solving ordinary differential equations. As in the first course on ordinary differential equations, we will not go heavy on the theory here, but focus on illustrating the theory with examples and applications. 

The prerequisites for this course are 
1. A working knowledge of Ordinary Differential Equations I
2. A working knowledge of Calculus III - Multivariable and Vector Calculus
3. The units on the Fourier transform and Laplace transform require a working knowledge of the calculus of complex variables, in particular contour integration. 

<a class="page-link" href="/calculus-III/introduction"> Introduction </a>

{% assign unitNames = "Unit 1 - Power Series Solutions, Unit 2 - Fourier Series, Unit 3 - Sturm Liouville Boundary Value Problems, Unit 4 - Operators, Unit 5 - Fourier Transform, Unit 6 - Laplace Transform" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

{% assign lessonNames5 = "Introduction, Properties, Solving-ODEs" | split: ', ' %}

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
{% elsif unitIndex == 5 %}  {% assign lessonNames = lessonNames6 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Elementary Differential Equations and Boundary Value Problems, Boyce and Di Prima
2. Complex Variables and Applications, by Churchill and Brown
3. Ordinary Differential Equations, by Morris and Tenenbaum
