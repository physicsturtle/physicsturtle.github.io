---
layout: page
title: Introduction to 3D Space
course: quantum-mechanics-I
unit: unit1
---

Unit 1 lays out the basic ideas of quantum theory. This includes some mathematics, as well as the idea of a wave-function. We will also discuss some of the differences between quantum and classical mechanics. 

{% for my_page in site.pages %}
{% if  my_page.course == "quantum-mechanics-I" and my_page.unit == "unit1" %}
<li> <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a> </li>
{% endif %}
{% endfor %}
