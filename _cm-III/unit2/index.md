---
layout: unit
title: The Calculus of Variations 
dept: physics
course: cm-III
unit: unit2
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 2
---
{% assign lessonNames = "Introduction to the problem , Euler-Lagrange equation , Hanging rope , " \| split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName \| replace:  '_', ' ' %}
{% assign linkName = lessonName \| replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink \| append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
