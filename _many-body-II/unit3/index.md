---
layout: unit
title: Fermionic Coherent State Path Integral 
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
{% assign lessonNames = "Path Integral for a Fermionic Field Theory , " \| split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName \| replace:  '_', ' ' %}
{% assign linkName = lessonName \| replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink \| append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
