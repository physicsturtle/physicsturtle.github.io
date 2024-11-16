---
layout: unit
title: Electrostatics 
dept: physics
course: em-I
unit: unit2
deptDisplay: Physics
courseDisplay: Electromagnetism I
unitDisplay: Unit 2
---
{% assign lessonNames = "Coulomb's Law , Coulomb's law for continuous charge distributions , Electric Flux , Gauss's Law , Using Gauss's Law , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
