---
layout: unit
title: Introduction to Green functions and elementary examples 
dept: math
course: green_functions
unit: unit2
deptDisplay: Math
courseDisplay: Green functions
unitDisplay: Unit 2
---
{% assign lessonNames = "Introduction , First order linear equations , Second order equation with constant coefficients , Poisson's formula , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
