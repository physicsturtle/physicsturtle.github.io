---
layout: course
title: Green functions
banner: green_functions.svg
permalink: /green_functions/
---
{% assign unitNames = "Unit 1 - Introduction , Unit 2 - Introduction to Green functions and elementary examples , "| split: ', ' %}

{% assign units = "unit1/, unit2/, " | split: ', ' %}

{% assign lessonNames1 = "Dirac delta Function , Test functions , " | split: ', ' %}
{% assign lessonNames2 = "Introduction , First order linear equations , Second order equation with constant coefficients , Poisson's formula , " | split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %} {% assign lessonNames = lessonNames2 %}
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
