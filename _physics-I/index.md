---
layout: course
title: Physics I - Elasticity, Fluids, Thermodynamics, Oscillations, Acoustics
permalink: /physics-I/
banner: physics-I.svg
---

Welcome to your first course on Physics! The first year undergraduate physics curriculum is meant to introduce the student to most areas of study in classical physics, which include classical mechanics, thermodynamics, elasticity, fluids, acoustics, waves, electromagnetism, and optics. In Physics I, we will cover elasticity, fluids, thermodynamics, oscillations, and then acoustics, in that order. In Physics II, we will cover electromagnetism and optics. In Classical Mechanics I, we will have of course classical mechanics. Later in your physics education, you will be exposed to further topics in each of these areas, and a strong understanding of each of these will be very valuable when you eventually move to quantum mechanics.

{% assign unitNames = "Unit 1 - Fluids, Unit 2 - Gravitation, Unit 3 - Thermodynamics, Unit 4 - Equilibrium and Elasticity, Unit 5 - Waves, Unit 6 - Acoustics, Supplementary Material" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "Heat_Capacity, Thermal_Expansion, Latent_Heat_of_Transformation" | split: ', ' %}

{% assign lessonNames2 = "Newton's_Law, " | split: ', ' %}

{% assign lessonNames3 = "Temperature and Thermal Equilibrium 552
17.2 Thermometers and Temperature Scales 553
17.3 Gas Thermometers and the Kelvin Scale 554
17.4 Thermal Expansion 557
17.5 Quantity of Heat 562
17.6 Calorimetry and Phase Changes 565
17.7 Mechanisms of Heat Transfer 570

19 THE FIRST LAW OF THERMODYNAMICS 624
19.1 Thermodynamic Systems 624
19.2 Work Done During Volume Changes 625
19.3 Paths Between Thermodynamic States 628
19.4 Internal Energy and the First Law
of Thermodynamics 629
19.5 Kinds of Thermodynamic Processes 634
19.6 Internal Energy of an Ideal Gas 636
19.7 Heat Capacities of an Ideal Gas 636
19.8 Adiabatic Processes for an Ideal Gas 639
Summary 643 Questions/Exercises/Problems 644
20 THE SECOND LAW OF THERMODYNAMICS 652
20.1 Directions of Thermodynamic Processes 652
20.2 Heat Engines 654
20.3 Internal-Combustion Engines 657
20.4 Refrigerators 659
20.5 The Second Law of Thermodynamics 661
20.6 The Carnot Cycle 663
20.7 Entropy 669
20.8 Microscopic Interpretation of Entropy" | split: ', ' %}

{% assign lessonNames4 = "Stress_and_Strain" | split: ', ' %}

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
