---
layout: course
title: Physics II - Electromagnetism, Circuits, and Optics
permalink: /physics-II/
banner: physics-II.svg
---

Welcome to your second course on Physics! This course will spend a little bit of time building on the topics of the previous course, Physics I, but the majority will be completely distinct. Much of this material you should have seen already in high school, but without the calculus point of view. 

{% assign unitNames = "Unit 1 - Electrostatics, Unit 2 - Potentials, Unit 3 - Magnetostatics, Unit 4 - Electrodynamics, Unit 5 - Electronic Circuits, Unit 6 - Optics" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "Coulomb's_Law, Coulomb's_Law_Line_Distributions, Gauss's_Law, Superposition" | split: ', ' %}

{% assign lessonNames2 = "Electrostatic_Potential_Energy, Electric_Potential_Function, Capacitance" | split: ', ' %}

{% assign lessonNames3 = "Lorentz_Force_Law, Biot-Savart_Law, Ampere's Law, Superposition" | split: ', ' %}

{% assign lessonNames4 = "Faraday's_Law, Inductance" | split: ', ' %}

{% assign lessonNames5 = "Ohm's_Law, RC_Circuits, LR_Circuits, LC_Circuits, RLC_Circuits" | split: ', ' %}

{% assign lessonNames6 = "Superposition, Double_Slit_Experiment, Thin_Films" | split: ', ' %}

<ul>
{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex == 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex == 3 %}  {% assign lessonNames = lessonNames4 %}
{% elsif unitIndex == 4 %}  {% assign lessonNames = lessonNames5 %}
{% elsif unitIndex == 5 %}  {% assign lessonNames = lessonNames6 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. 
