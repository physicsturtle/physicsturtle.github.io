---
layout: lesson
title: Spherical Coordinates
dept: math
course: calculus-III
unit: unit1
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 1
---

Spherical coordinates are a set of three coordinates used when the objects we're studying have spherical symmetry. They will simplify our calculations and make the results much more transparent. The three coordinates are the distance from the origin \\(r\\), the angle measured down from the \\(z\\) axis \\(\theta\\), and the angle measured in the \\(xy\\) plane, \\(\varphi\\). This can be represented graphically by 

(insert figure here)

Algebraically, the transformation equations are 

$$\left\{\begin{eqnarray}
r &=& \sqrt{x^2+y^2+z^2}\\
\theta &=& \arccos\left(\frac{z}{\sqrt{x^2+y^2+z^2}}\right)\\
\varphi &=& \arctan\left(\frac{y}{x}\right)
\end{eqnarray} \right.$$

$$\left\{\begin{eqnarray}
x &=& r\sin\theta\cos\varphi \\
y &=& r\sin\theta\sin\varphi \\
z &=& r\cos\theta \end{eqnarray} \right.$$



### Exercises

<ol>
<li> <div> Express the points $(1,2,3)$ in terms of the three spherical coordinates. </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
