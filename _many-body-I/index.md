---
layout: course
title: Many Body Physics I
banner: many-body-I.svg
permalink: /many-body-I/
---
{% assign unitNames = "Unit 6 - Time-evolution pictures , Unit 29 - Interacting Electron Gas , "| split: ', ' %}

{% assign units = "unit6/, unit29/, " | split: ', ' %}

{% assign lessonNames6 = "Schrodinger Picture , Heisenberg Picture , Interaction Picture , " | split: ', ' %}
{% assign lessonNames29 = "Screening in the electron gas (physical discussion) , " | split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames6 %}
{% elsif unitIndex== 1 %} {% assign lessonNames = lessonNames29 %}
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
