---
layout: unit
title: Path Integrals 
dept: physics
course: qm-V
unit: unit3
deptDisplay: Physics
courseDisplay: Quantum Mechanics V
unitDisplay: Unit 3
---
{% assign lessonNames = "The Propagator , Propagator as a Path Integral , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
