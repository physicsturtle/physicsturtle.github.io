---
layout: page
title: Introduction to 3D Space and Vectors
course: intro-to-physics
unit: unit1
---

Unit 1 lays out the foundations for understanding how to work with objects in 3 dimensional space. There won't be any calculus yet, but we'll try and understand how to draw pictures, including vectors and graphs. This will be one of the most important skills throughout the rest of the course to intuitively understand the mathematics through graphical means. 

{% for my_page in site.pages %}
{% if  my_page.course == "calculus-III" and my_page.unit == "unit1" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
