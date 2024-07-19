---
layout: page
title: Vector Calculus
course: calculus-III
unit: unit5
---

Unit 2 introduces the idea of functions of a single variable with vector valued outputs. In other words, functions which take values in 2D or 3D space instead of along a line. 

{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit2" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
