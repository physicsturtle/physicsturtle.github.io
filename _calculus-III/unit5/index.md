---
layout: page
title: Vector Calculus
course: calculus-III
unit: unit5
permalink: /calculus-III/unit5/
---

Unit 5 studies the last kind of function between sets of real numbers. That is, functions which take a vector input and give a vector output. In symbols, this is functions like 

$$ f: \mathbb{R}^n \to \mathbb{R}^m$$

we will be considering functions where \\(n = m = 2\\) or \\(n = m = 3\\). These kinds of functions are known as *vector fields*. 

<ol>
{% assign lessonNames = "Maxwell's-Equations" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
{% assign lowerName = lessonName | downcase %}
<li> <a class = "page-link" href = "{{ lowerName | prepend: current_page.permalink}}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ol>
