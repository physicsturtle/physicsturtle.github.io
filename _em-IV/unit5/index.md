---
layout: page
title: Vector Calculus
course: calculus-III
unit: unit5
permalink: /math/calculus-III/unit5/
---

Unit 5 studies the last kind of function between sets of real numbers. That is, functions which take a vector input and give a vector output. In symbols, this is functions like 

$$ f: \mathbb{R}^n \to \mathbb{R}^m$$

we will be considering functions where \\(n = m = 2\\) or \\(n = m = 3\\). These kinds of functions are known as *vector fields*. 

<ol>
{% assign temp = "vector-fields" %}
{% for my_page in site.calculus-III %}
{% for my_page in site.calculus-III %}
{% if my_page.unit == "unit5" and my_page.layout == "lesson" and my_page.lessonID == temp %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% assign temp = my_page.nextID %}
{% endif %}
{% endfor %}
{% endfor %}
</ol>
