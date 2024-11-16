---
layout: unit
title: Adiabatic theorem and Berry phase 
dept: physics
course: top_phys-I
unit: unit2
deptDisplay: Physics
courseDisplay: Topological Physics I
unitDisplay: Unit 2
---
{% assign lessonNames = "Adiabatic Theorem , Berry Phase and Curvature , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
