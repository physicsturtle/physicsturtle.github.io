---
layout: unit
title: Unit 3
dept: math
course: calculus-I
deptDisplay: Math
courseDisplay: Calculus I
unit: unit3
---

{% assign lessonNames = "Definition_of_the_Derivative, Derivatives_of_Polynomials, Product_Rule, Quotient_Rule, Derivatives_of_Trigonometric_Functions, Derivatives_of_Exponentials, Derivatives_of_Hyperbolic_Functions*, Chain_Rule, Implicit_Differentiation, Derivatives_of_Logarithms, Derivatives_of_Inverse_Trigonometric_Functions, Derivatives_of_Inverse_Hyperbolic_Functions*, Logarithmic_Differentiation, Linear_Approximations_and_Differentials, Taylor_Polynomials, Lagrange_Remainder_Theorem" | split: ', ' %}

<ol>
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '_', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ lowerName | prepend: units[unitIndex] | prepend: current_page.permalink | append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
