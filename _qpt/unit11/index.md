---
layout: unit
title: Hertz-Millis-Moriya Theory 
dept: physics
course: qpt
unit: unit11
deptDisplay: Physics
courseDisplay: Quantum Phase Transitions
unitDisplay: Unit 11
---
{% assign lessonNames = "Ising Order , Spin Density Wave Order , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
