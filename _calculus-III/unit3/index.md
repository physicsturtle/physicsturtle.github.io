---
layout: page
dept: math
title: Partial Differentiation 
course: calculus-III
unit: unit3
permalink: /calculus-III/unit3/
---

Unit 3 introduces the idea of functions which take multiple real numbers as inputs, but output a single real number as output. In symbols, this means functions like:

$$ f : \mathbb{R}^n \to \mathbb{R}$$


<ol>
{% assign lessonNames = "" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: current_page.permalink}}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
