---
layout: course
title: Ordinary Differential Equations I
banner: ode-I.svg
permalink: /ode-I/
---
{% assign unitNames = "Unit 2 - First Order Differential Equations , "\| split: ', ' %}

{% assign units = "unit2/, " \| split: ', ' %}

{% assign lessonNames2 = "Integrating Factor , " \| split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink \| append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames2 %}
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
