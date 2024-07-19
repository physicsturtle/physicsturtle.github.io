---
layout: unit
title: Adiabatic theorem and Berry phase 
dept: physics
course: qm-II
unit: unit6
deptDisplay: Physics
courseDisplay: Quantum Mechanics II
unitDisplay: Unit 6
---
{% assign lessonNames = "Adiabatic Theorem , Berry Phase and Curvature , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
