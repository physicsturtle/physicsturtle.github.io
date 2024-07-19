---
layout: unit
title: Electrons in a periodic potential 
dept: physics
course: cmp-I
unit: unit4
deptDisplay: Physics
courseDisplay: Condensed Matter Physics I
unitDisplay: Unit 4
---
{% assign lessonNames = "Tight-binding model , Relativistic effects , Schrodinger equation with spin-orbit coupling , " \| split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName \| replace:  '_', ' ' %}
{% assign linkName = lessonName \| replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink \| append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
