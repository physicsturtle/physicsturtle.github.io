---
layout: course
title: Asymptotic Analysis I
permalink: /asymptotics/
banner: asymptotics.svg
---

Welcome to Asymptotic Analysis I! This fits into the world of PDE somewhere between real analysis and analytic methods. On the other side of analytic methods is numerical methods. 

<a class="page-link" href="/asympI/introduction"> Introduction - What is Asymptotic Analysis? </a>

The prerequisites are as follows
1. A strong background in solution methods of ODE and PDE
2. A working knowledge of complex analysis
3. An exposure to physics is useful; many examples will be drawn from physics.

{% assign unitNames = "Unit 1 - Algebraic Perturbations, Unit 2 - Basic Perturbations of Self-Adjoint Differential Equations, Unit 3 - Integrals, Unit 4 - Boundary Layers, Unit 5 - Multiple Scales Analysis" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

{% assign lessonNames5 = "generalizations" | split: ', ' %}

<ul>
{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex == 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex == 3 %}  {% assign lessonNames = lessonNames4 %}
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

1. Calculus, 7 ed. - Stewart, James (2012)
