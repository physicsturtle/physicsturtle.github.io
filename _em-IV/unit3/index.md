---
layout: page
title: Partial Differentiation 
course: calculus-III
unit: unit3
permalink: /calculus-III/unit3/
---

Unit 3 introduces the idea of functions which take multiple real numbers as inputs, but output a single real number as output. In symbols, this means functions like:

$$ f : \mathbb{R}^n \to \mathbb{R}$$


<ol>
{% assign temp = "functions-multiple-variables" %}
{% for my_page in site.calculus-III %}
{% for my_page in site.calculus-III %}
{% if my_page.unit == "unit3" and my_page.layout == "lesson" and my_page.lessonID == temp %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% assign temp = my_page.nextID %}
{% endif %}
{% endfor %}
{% endfor %}
</ol>
