---
layout: unit
title: The Kondo impurity model 
dept: physics
course: kondo-physics
unit: unit3
deptDisplay: Physics
courseDisplay: Kondo and Heavy Fermion physics
unitDisplay: Unit 3
---
{% assign lessonNames = "Effective Hamiltonian Method , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
