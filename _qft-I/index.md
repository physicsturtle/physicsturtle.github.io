---
layout: course
title: Quantum Field Theory I
banner: qft-I.svg
---

Welcome to Quantum Field Theory I

The prerequisites are as follows:
1. A strong background in high school mathematics, including trigonometry, solving algebraic equations, working with exponentials and logarithms, and graphing.
2. An exposure to physics is useful; many examples will be drawn from physics. 

Notation and conventions used in this course are here

<a class = "page-link" href = "/qft-I/notation"> Notation and Conventions </a>

{% assign unitNames = "Unit 1 - , Unit 2 - , Unit 3 - , Unit 4 - " | split: ', ' %}

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

1. Introduction to Quantum Field Theory, Peskin & Schroeder
2. Quantum Field theory for the Gifted Amateur, Lancaster and Blundell
3. Quantum Theory of Fields, Volume 1, Weinberg
4. Quantum Field Theory in a Nutshell, Zee
