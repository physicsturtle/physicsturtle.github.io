---
layout: unit
title: Unit 2
dept: math
course: calculus-I
deptDisplay: Math
courseDisplay: Calculus I
unit: unit2
---

{% assign lessonNames = "Limits, Limit_Laws, Limit_Details, Squeeze_Theorem, Continuity, Intermediate_Value_Theorem, Limits_at_Infinity" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
