---
layout: course
title: Quantum Mechanics II
banner: qm-II.svg
permalink: /qm-II/
---
{% assign unitNames = "Unit 6 - Adiabatic theorem and Berry phase , "| split: ', ' %}

{% assign units = "unit6/, " | split: ', ' %}

{% assign lessonNames6 = "Adiabatic Theorem , Berry Phase and Curvature , " | split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames6 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign linkName = lessonName | replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>
**Sources**
