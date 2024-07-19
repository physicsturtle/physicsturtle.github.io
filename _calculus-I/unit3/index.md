---
layout: unit
title: Differentiation 
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---
{% assign lessonNames = "Derivatives of Polynomials , Product and Quotient Rules , Derivatives of Trigonometric Functions , Derivatives of Hyperbolic Functions* , Chain Rule , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
