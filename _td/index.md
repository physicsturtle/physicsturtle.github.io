---
layout: course
title: Thermodynamics
permalink: /td/
banner: td.svg
---

Welcome to thermodynamics! In undergraduate physics, I have found that many skim over this material, but it is of extreme importance and often students are left to teach themselves later on. 

The prerequisites are as follows:
1. A working knowledge of multivariable and vector calculus.
2. A working knowledge of first year physics.

{% assign unitNames = "Unit 1 - , Unit 2 - Limits and Continuity, Unit 3 - Differentiation, Unit 4 - Applications of Differentiation" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/" | split: ', ' %}

{% assign lessonNames1 = "Sets, Functions, Inverse_Functions" | split: ', ' %}

{% assign lessonNames2 = "Introduction, Limits, Limit_Laws, Limit_Details, Squeeze_Theorem, Continuity, Intermediate_Value_Theorem, Limits_at_Infinity" | split: ', ' %}

{% assign lessonNames3 = "Definition_of_the_Derivative, Derivatives_of_Polynomials, Product_Rule, Quotient_Rule, Derivatives_of_Trigonometric_Functions, Derivatives_of_Exponentials, Derivatives_of_Hyperbolic_Functions*, Chain_Rule, Implicit_Differentiation, Derivatives_of_Logarithms, Derivatives_of_Inverse_Trigonometric_Functions, Derivatives_of_Inverse_Hyperbolic_Functions*, Logarithmic_Differentiation, Linear_Approximations_and_Differentials, Taylor_Polynomials, Lagrange_Remainder_Theorem" | split: ', ' %}

{% assign lessonNames4 = "Kinematics_Problems, Exponential_Growth_and_Decay, Newton's_Law_of_Cooling, Related_Rates, Extrema, Mean_Value_Theorem, Curve_Sketching, Optimization_Problems, L'Hopital's_Rule, Newton's_Method" | split: ', ' %}

<ul>
{% for unitName in unitNames %}
{% assign unitLink = page.permalink | append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames1 %}
{% elsif unitIndex== 1 %}  {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex == 2 %}  {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex == 3 %}  {% assign lessonNames = lessonNames4 %}
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

1. Calculus, 7 ed. - Stewart, James (2012)
2. Schaums Outline of Calculus, 4 ed. - Ayres Jr., Frank (2002)
3. Calculus - Spivak, Michael
4. Calculus, Vol. 1 - Apostol, Tom
