---
name: emptyCourse/
layout: course
title: Empty Course
permalink: /emptyCourse/
banner: banner.png
---

Welcome to Multi-Variable and Vector Calculus. This is a really exciting subject and is the first step into allowing one to tackle real world physics and engineering problems. 

This course is a **work in progress**.

Sections marked with an asterisk * should be regarded as optional, and everything else as essential. The ones chosen to be marked with an asterisk are ones which are normally left out of multivariable calculus courses, but may be included in an honours course. One of the goals is to be able to cater to as wide of an audience as possible, and for this reason those sections were written.

This is a course on calculus, *not analysis*. The goal is for students to understand how to compute important quantities and objects in multivariable calculus, and to understand the concepts without proof and be able to interpret concepts geometrically.

<a class="page-link" href="/calculus-III/introduction">Introduction - What is Multivariable Calculus? </a>

<a class="page-link" href="/calculus-III/prerequisites"> Prerequisites</a>

<a class="page-link" href="/calculus-III/learning-outcomes"> Learning Outcomes</a>

{% assign unitNames = "Unit 1 - Introduction to 3D Space and Vectors, Unit 2 - Space Curves, Unit 3 - Partial Differentiation, Unit 4 - Multiple Integration, Unit 5 - Vector Calculus, Supplementary Material" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "Three-Dimensional-Cartesian-Coordinates, Vectors-and-Their-Geometry, Algebraic-Operations-with-Vectors, Norm, Projections" | split: ', ' %}

{% assign lessonNames2 = "Three-Dimensional-Cartesian-Coordinates, Vectors-and-Their-Geometry, Algebraic-Operations-with-Vectors, Norm, Projections" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

{% assign lessonNames5 = "Maxwell's-Equations" | split: ', ' %}

{% assign lessonNames6 = "Chain-Rules, Coordinate-Change-Tensor, Coordinate-Change, Curvilinear-Coordinates, Notation, Product-Rules" | split: ', ' %}

<ul>
{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> "{{unitName}}" </a> </li>
<ol>
{% if forloop.index == 1 %} {% assign lessonNames = lessonNames1 %}
{% elsif forloop.index == 2 %}  {% assign lessonNames = lessonNames2 %}
{% elsif forloop.index == 3 %}  {% assign lessonNames = lessonNames3 %}
{% elsif forloop.index == 4 %}  {% assign lessonNames = lessonNames4 %}
{% elsif forloop.index == 5 %}  {% assign lessonNames = lessonNames5 %}
{% elsif forloop.index == 6 %}  {% assign lessonNames = lessonNames6 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[forloop.index0] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. Calculus, 7 ed. - Stewart, James (2012)
2. Vector Analysis - Spiegel, Murray R. (1959)
3. Differential Geometry of Curves and Surfaces - 2 ed. do Carmo, Manfredo (2016)
4. Calculus on Manifolds - Spivak, Michael (1965)
