---
layout: page
title: Multiple Integration
course: calculus-III
unit: unit4
permalink: /calculus-III/unit4/
---

Unit 2 introduces the idea of functions of a single variable with vector valued outputs. In other words, functions which take values in 2D or 3D space instead of along a line. 

<ol>
{% assign lessonNames = "" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: current_page.permalink}}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
