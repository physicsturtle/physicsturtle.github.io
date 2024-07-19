---
layout: course
title: Classical Mechanics III
banner: cm-III.svg
permalink: /cm-III/
---
{% assign unitNames = "Unit 2 - The Calculus of Variations , Unit 3 - Lagrangian Mechanics , "\| split: ', ' %}

{% assign units = "unit2/, unit3/, " \| split: ', ' %}

{% assign lessonNames2 = "Introduction to the problem , Euler-Lagrange equation , Hanging rope , " \| split: ', ' %}
{% assign lessonNames3 = "Introductory Problems , " \| split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink \| append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex== 1 %} {% assign lessonNames = lessonNames3 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName \| replace:  '_', ' ' %}
{% assign linkName = lessonName \| replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink \| append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>
**Sources**
