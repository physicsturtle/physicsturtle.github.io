---
layout: page
title: Basic Concepts
course: cm-III
unit: unit1
---

The Calculus of Variations

<ol>
{% assign lessonNames = "Euler-Lagrange, Hanging-Rope" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: current_page.permalink}}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
