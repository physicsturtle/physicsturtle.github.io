---
layout: course
title: Superconductivity & Superfluidity
banner: superconductivity.svg
permalink: /superconductivity/
---
{% assign unitNames = "Unit 4 - BCS Theory , Unit 45 - Landau Theory; lattice system , "| split: ', ' %}

{% assign units = "unit4/, unit45/, " | split: ', ' %}

{% assign lessonNames4 = "Pairing requires an attractive interaction , Cooper instability , " | split: ', ' %}
{% assign lessonNames45 = "Landau Theory from BCS Theory , " | split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames4 %}
{% elsif unitIndex== 1 %} {% assign lessonNames = lessonNames45 %}
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
