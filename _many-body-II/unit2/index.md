---
layout: unit
title: Bosonic Coherent State Path Integral 
dept: physics
course: many-body-II
unit: unit2
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 2
---
{% assign lessonNames = "The Bosonic Coherent State Path Integral , " \| split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName \| replace:  '_', ' ' %}
{% assign linkName = lessonName \| replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink \| append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
