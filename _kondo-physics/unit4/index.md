---
layout: unit
title: Kondo Model in Weak Coupling 
dept: physics
course: kondo-physics
unit: unit4
deptDisplay: Physics
courseDisplay: Kondo and Heavy Fermion physics
unitDisplay: Unit 4
---
{% assign lessonNames = "Conduction electron self energy (spin operators) , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
