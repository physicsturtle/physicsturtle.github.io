---
layout: unit
title: Interacting Electron Gas 
dept: physics
course: many-body-I
unit: unit29
deptDisplay: Physics
courseDisplay: Many Body Physics I
unitDisplay: Unit 29
---
{% assign lessonNames = "Screening in the electron gas (physical discussion) , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
