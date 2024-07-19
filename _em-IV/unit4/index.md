---
layout: page
title: Multiple Integration
course: calculus-III
unit: unit4
permalink: /math/calculus-III/unit4/
---

Unit 2 introduces the idea of functions of a single variable with vector valued outputs. In other words, functions which take values in 2D or 3D space instead of along a line. 

<ol>
{% assign temp = "riemann-sums" %}
{% for my_page in site.calculus-III %}
{% for my_page in site.calculus-III %}
{% if my_page.unit == "unit4" and my_page.layout == "lesson" and my_page.lessonID == temp %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% assign temp = my_page.nextID %}
{% endif %}
{% endfor %}
{% endfor %}
</ol>
