---
layout: page
title: Quantum Mechanics IV
permalink: /qm-IV/
banner: qm-IV.svg
---

Welcome to Quantum Mechanics IV

Scattering Theory:
-time-dependent versus time-independent view
-the Born approximation
-Spherically symmetric potentials and phase shifts
-Feshbach Resonances in atomic scattering
Phonons and Second Quantization
Photons and Second Quantization:
-stimulated and spontaneous emission
Cavity QED:
-the Jayne-Cummings Model
Relativity and Quantum Mechanics:
-The Dirac Equation
-fine structure
Feynman Path Integral formulation of Quantum Mechanics
-instantons and tunnelling in the double-well potential
-instantons and unstable ground states

{% assign unitNames = "Unit 1 - , Unit 2 - , Unit 3 - , Unit 4 - , Unit 5 - , Unit 6 - " | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, unit6/" | split: ', ' %}

{% assign lessonNames1 = "" | split: ', ' %}

{% assign lessonNames2 = "Infinite@Square@Well, Probability@Current, Non-Normalizable@Wave@Functions, Spherically@Symmetric@Problems" | split: ', ' %}

{% assign lessonNames3 = "" | split: ', ' %}

{% assign lessonNames4 = "" | split: ', ' %}

{% assign lessonNames5 = "" | split: ', ' %}

{% assign lessonNames6 = "" | split: ', ' %}

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
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '@', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>

**Sources**

1. 
