---
layout: unit
title: Magnetism and Strong coupling of the Hubbard model 
dept: physics
course: cmp-II
unit: unit3
deptDisplay: Physics
courseDisplay: Condensed Matter Physics II
unitDisplay: Unit 3
---
{% assign lessonNames = "Hubbard Subbands , " | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
