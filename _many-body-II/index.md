---
layout: course
title: Many Body Physics II
banner: many-body-II.svg
permalink: /many-body-II/
---
{% assign unitNames = "Unit 2 - Bosonic Coherent State Path Integral , Unit 3 - Fermionic Coherent State Path Integral , Unit 10 - Fermi Hubbard Model , Unit 25 - Periodic Anderson and Kondo Lattice Model , Unit 31 - Appendix , "\| split: ', ' %}

{% assign units = "unit2/, unit3/, unit10/, unit25/, unit31/, " \| split: ', ' %}

{% assign lessonNames2 = "The Bosonic Coherent State Path Integral , " \| split: ', ' %}
{% assign lessonNames3 = "Path Integral for a Fermionic Field Theory , " \| split: ', ' %}
{% assign lessonNames10 = "Spin Density Wave Order , " \| split: ', ' %}
{% assign lessonNames25 = "RKKY Interaction , " \| split: ', ' %}
{% assign lessonNames31 = "Gaussian Integrals , " \| split: ', ' %}
<ul>

{% for unitName in unitNames %}
{% assign unitLink = page.permalink \| append: units[forloop.index0] %}
<li>  <a class="page-link" href="{{unitLink}}"> {{unitName}} </a> </li>
<ol> {%assign unitIndex = forloop.index0 %}
{% if unitIndex == 0 %} {% assign lessonNames = lessonNames2 %}
{% elsif unitIndex== 1 %} {% assign lessonNames = lessonNames3 %}
{% elsif unitIndex== 2 %} {% assign lessonNames = lessonNames10 %}
{% elsif unitIndex== 3 %} {% assign lessonNames = lessonNames25 %}
{% elsif unitIndex== 4 %} {% assign lessonNames = lessonNames31 %}
{% endif %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName \| replace:  '_', ' ' %}
{% assign linkName = lessonName \| replace: ' ', " %}
<li> <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink }}"> {{lessonTitle}} </a> - <a class = "page-link" href = "{{ linkName \| prepend: units[unitIndex] \| prepend: current_page.permalink \| append: "-exercises" }}"> Exercises </a> </li>
{% endfor %}
</ol>
{% endfor %}
</ul>
**Sources**
