---
layout: unit
title: Landau Theory 
dept: physics
course: superconductivity
unit: unit39
deptDisplay: Physics
courseDisplay: Superconductivity & Superfluidity
unitDisplay: Unit 39
---
{% assign lessonNames = "Landau Theory from BCS Theory , " \| split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName \| replace:  '_', ' ' %}
{% assign linkName = lessonName \| replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink \| append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
