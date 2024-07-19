---
layout: unit
title: Lagrangian Mechanics 
dept: physics
course: cm-III
unit: unit3
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 3
---
{% assign lessonNames = "Introductory Problems , " \| split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName \| replace:  '_', ' ' %}
{% assign linkName = lessonName \| replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink \| append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
