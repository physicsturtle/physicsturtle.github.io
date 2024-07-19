---
layout: unit
title: Periodic Anderson and Kondo Lattice Model 
dept: physics
course: many-body-II
unit: unit25
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 25
---
{% assign lessonNames = "RKKY Interaction , " \| split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName \| replace:  '_', ' ' %}
{% assign linkName = lessonName \| replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink \| append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
