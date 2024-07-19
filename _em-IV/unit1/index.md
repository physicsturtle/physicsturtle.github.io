---
layout: page
title: Electrostatics
course: electromagnetism-I
unit: unit1
permalink: /electromagnetism-I/unit1/
---

Unit 1, electrostatics, concerns itself with systems of electric charges which are not moving, or are moving very slowly.  Studying the effects of moving electric charges is beyond the scope of this course. We will examine point charges as well as continuous charge distributions.



<ol>
{% assign temp = "coulombs-law" %}
{% for my_page in site.calculus-III %}
{% for my_page in site.calculus-III %}
{% if my_page.unit == "unit1" and my_page.layout == "lesson" and my_page.lessonID == temp %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% assign temp = my_page.nextID %}
{% endif %}
{% endfor %}
{% endfor %}
</ol>
<!---
Three-dimensional cartesian coordinaes
vectors and geometry
algebraic operations with vectors
norm
--->