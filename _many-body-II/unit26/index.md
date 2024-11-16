---
layout: unit
title: Periodic Anderson and Kondo Lattice Model 
dept: physics
course: many-body-II
unit: unit26
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 26
---
{% assign lessonNames = "RKKY Interaction , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
