---
layout: unit
title: BCS Theory 
dept: physics
course: superconductivity
unit: unit4
deptDisplay: Physics
courseDisplay: Superconductivity & Superfluidity
unitDisplay: Unit 4
---
{% assign lessonNames = "Pairing requires an attractive interaction , Cooper instability , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
