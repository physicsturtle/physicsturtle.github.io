---
layout: unit
title: Time-evolution pictures 
dept: physics
course: many-body-I
unit: unit6
deptDisplay: Physics
courseDisplay: Many Body Physics I
unitDisplay: Unit 6
---
{% assign lessonNames = "Schrodinger Picture , Heisenberg Picture , Interaction Picture , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
