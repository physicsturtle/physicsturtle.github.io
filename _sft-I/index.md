---
layout: course
title: Statistical Field Theory I
banner: sft-I.svg
permalink: /sft-I/
---
{% assign unitNames = "Unit 4 - From particles to fields , Unit 5 - Landau Theory , "\| split: ', ' %}

{% assign units = "unit4/, unit5/, " \| split: ', ' %}

{% assign lessonNames4 = "The Hubbard-Stratonovich transformation , " \| split: ', ' %}
{% assign lessonNames5 = "Wick's Theorem , " \| split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink \| append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames4 %}
{% elsif unitIndex== 1 %} {% assign lessonNames = lessonNames5 %}
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
