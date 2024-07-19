---
layout: course
title: Calculus III - Multivariable and Vector Calculus
banner: calculus-III.svg
---

Welcome to Multi-Variable and Vector Calculus. This is a really exciting subject and is the first step into allowing one to tackle real world physics and engineering problems. 

Sections marked with an asterisk * should be regarded as optional, and everything else as essential. The ones chosen to be marked with an asterisk are ones which are normally left out of multivariable calculus courses, but may be included in an honours course. One of the goals is to be able to cater to as wide of an audience as possible, and for this reason those sections were written.

This is a course on calculus, *not analysis*. The goal is for students to understand how to compute important quantities and objects in multivariable calculus, and to understand the concepts without proof and be able to interpret concepts geometrically.

<a class="page-link" href="/calculus-III/introduction"> Introduction - What is Multivariable Calculus? </a>

1. Working knowledge of single variable differential calculus (Calculus I)
2. Working knowledge of single variable integral calculus (Calculus II) 
3. Rudimentary knowledge of linear algebra; any first course in linear algebra is more than sufficient
4. Knowledge of ordinary differential equations may be useful
5. An exposure to introductory physics will be useful for developing physical intuition

{% assign unitNames = "Unit 1 - Introduction to 3D Space and Vectors, Unit 2 - Space Curves, Unit 3 - Partial Differentiation, Unit 4 - Multiple Integration, Unit 5 - Vector Calculus, Supplementary Material" | split: ', ' %}

{% assign units = "unit1/, unit2/, unit3/, unit4/, unit5/, supplements/" | split: ', ' %}

{% assign lessonNames1 = "Three_Dimensional_Cartesian_Coordinates, Vectors_and_Their_Geometry, Algebraic_Operations_with-Vectors, Norm, Projections, Dot_Product, Determinant_and_Cross_Product, Equations_of_Lines, Equations_of_Planes, Quadric_Surfaces, Cylindrical_Coordinates, Spherical_Coordinates, General_Surfaces" | split: ', ' %}

{% assign lessonNames2 = "Vector_Functions, Limits_and_Continuity, Differentiation_and_Integration_of_Curves, Arc_Length, Curvature_and_Torsion, Frenet_Serret_Equations" | split: ', ' %}

{% assign lessonNames3 = "Functions_of_Multiple_Variables, Contour_Plots_and_Level_Sets, Limits_and_Continuity, Partial_Differentiation, Tangent_Planes_and_Linear_Approximations, Gradient_Vector, The_Differential, Non_Independent_Variables, Chain_Rule, Differentiation_of_Integrals, Directional_Derivative, Extrema_1, Extrema_2, Lagrange_Multipliers_1, Lagrange_Multipliers_2, Bordered_Hessian, Lagrange_Remainder, The_Jacobian_Derivative, Higher_Dimensional_Lagrange_Multipliers, Inflection_and_Saddle_Points_Lagrange_Multipliers" | split: ', ' %}

{% assign lessonNames4 = "Riemann_Sums, Double_Integral_Over_a_Rectangle, Double_Integral_Over_a_General_Plane_Region, Double_Integral_in_Polar_Coordinates, Surface_Area, Triple_Integrals, Triples_Integrals_In_Cylindrical_Coordinates, Triple_Integrals_in_Spherical_Coordinates, Change_of_Variables, Applications" | split: ', ' %}

{% assign lessonNames5 = "Vector_Fields, Line_Integrals_in_2D, Fundamental_Theorem_of_Line_Integrals, Green's_Theorem, Divergence, Curl, Laplacian, Surface_Integrals, Stokes_Theorem, Divergence_Theorem, Applications, Flow_of_a_Vector_Field, Maxwell's_Equations, Differential_Forms, Green'_Identities" | split: ', ' %}

{% assign lessonNames6 = "Chain_Rules, Coordinate_Change-Tensor, Coordinate_Change, Curvilinear_Coordinates, Notation, Product_Rules" | split: ', ' %}

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

1. Calculus, 7 ed. - Stewart, James (2012)
2. Vector Analysis - Spiegel, Murray R. (1959)
3. Differential Geometry of Curves and Surfaces - 2 ed. do Carmo, Manfredo (2016)
4. Calculus on Manifolds - Spivak, Michael (1965)
