---
layout: course
title: Classical Field Theory
permalink: /classical-ft/
banner: classical-ft.svg
---

Welcome to Classical Field Theory, a subject which is severely undertaught in undergraduate and graduate physics programs. 

<a class="page-link" href="/classical-ft/introduction"> Introduction - What is Classical Field Theory? </a>

The prerequisites are as follows
1. An excellent background in electromagnetic theory
2. A working knowledge of continuum mechanics (fluid mechanics and elasticity)
3. A working knowledge of multivariable and vector calculus
4. A working knowledge of complex analysis

{% assign unitNames = "Unit 1 - , Unit 2 - , Unit - 3, Unit 4 - " | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

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
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Classical Theory of Fields - Landau and Liftshitz
2. Electrodynamics and Classical Theory of Fields and Particles - Barut
3. 
