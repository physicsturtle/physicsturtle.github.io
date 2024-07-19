---
layout: course
title: Condensed Matter Physics I
banner: cmp-I.svg
permalink: /cmp-I/
---
{% assign unitNames = "Unit 4 - Electrons in a periodic potential , "\| split: ', ' %}

{% assign units = "unit4/, " \| split: ', ' %}

{% assign lessonNames4 = "Tight-binding model , Relativistic effects , Schrodinger equation with spin-orbit coupling , " \| split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink \| append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames4 %}
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
