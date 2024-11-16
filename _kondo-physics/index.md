---
layout: course
title: Kondo and Heavy Fermion physics
banner: kondo-physics.svg
permalink: /kondo-physics/
---
{% assign unitNames = "Unit 3 - The Kondo impurity model , Unit 4 - Kondo Model in Weak Coupling , "| split: ', ' %}

{% assign units = "unit3/, unit4/, " | split: ', ' %}

{% assign lessonNames3 = "Effective Hamiltonian Method , " | split: ', ' %}
{% assign lessonNames4 = "Conduction electron self energy (spin operators) , " | split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex== 1 %} {% assign lessonNames = lessonNames4 %}
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
