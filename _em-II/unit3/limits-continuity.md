---
layout: lesson
title: LIMITS AND CONTINUITY*
course: calculus-III
unit: unit3
lessonID: limits-continuity
nextID: partial-differentiation
---

- Definition of continuity
- When a limit doesn't exist
- Limits in polar coordinates

In this optional section, we will discuss limits and continuity.


### Exercises

<ol>
<li> <div> Does the limit of the function
$$f(x,y) = \frac{x + y^3}{x^2 + y^2}$$ 
as we approach the origin exist? </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
No. Consider approaching the origin along the line $x = 0$. Then 
$$f(0,y) = \frac{y^3}{y^2} = y$$
so, along this line, the limit is zero. If we instead approach along the line $x = y^2$, then
$$f(y^2,y) = \frac{y^2 + y^3}{y^4 + y^2} = \frac{1+y}{1+y^2}$$
As we approach the origin, the limit is then 1. Since the limit is different when we approach along different paths, it does not exist.
</div> </li>

<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
