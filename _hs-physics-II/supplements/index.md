---
layout: page
title: Supplementary Material
course: emptyCourse
unit: supplement
---

<ul>
{% assign lessonNames = "placeholder1, placeholder2" | split: ', ' %}
{% for lessonName in lessonNames %}
{% assign lessonTitle = lessonName | replace:  '-', ' ' %}
<li> <a class = "page-link" href = "{{ lessonName | prepend: current_page.permalink}}"> {{lessonTitle}} </a> </li>
{% endfor %}
</ul>
