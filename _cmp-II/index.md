---
layout: course
title: Condensed Matter Physics II
banner: cmp-II.svg
permalink: /cmp-II/
---
{% assign unitNames = "Unit 3 - Magnetism and Strong coupling of the Hubbard model , "| split: ', ' %}

{% assign units = "unit3/, " | split: ', ' %}

{% assign lessonNames3 = "Hubbard Subbands , " | split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames3 %}
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
