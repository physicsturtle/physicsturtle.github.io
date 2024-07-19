---
layout: course
title: Calculus I
banner: calculus-I.svg
permalink: /calculus-I/
---
{% assign unitNames = "Unit 1 - Sets and Functions , Unit 3 - Differentiation , "\| split: ', ' %}

{% assign units = "unit1/, unit3/, " \| split: ', ' %}

{% assign lessonNames1 = "Sets , Functions , " \| split: ', ' %}
{% assign lessonNames3 = "Derivatives of Polynomials , " \| split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink \| append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
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
