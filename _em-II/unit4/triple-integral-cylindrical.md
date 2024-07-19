---
layout: lesson
title: TRIPLE INTEGRALS IN CYLINDRICAL COORDINATES
course: calculus-III
unit: unit4
lessonID: triple-integral-cylindrical
nextID: triple-integral-spherical
---

- the jacobiuan for cylindrical coordinates -- geometric derivation and determinant derivation
- Setting up integral in cylindrical coordinates
- Changing order of integration in cylindrical coordinates

When the system of interest presents cylindrical symmetry, integrals are often made simpler by switching to a different coordinate system. As in the case of polar coordinates, this requires us to change the volume element of integration.

<div class="example">
<b> Example:</b>
Find the volume of the region enclosed by $z = x^2+y^2$ and $z = 25 - 2x^2 - 2y^2$. 

<div class="exampleSolution">
<b> Solution: </b> First, let's determine the region of integration. We know that the surface $z = x^2+y^2$ is a paraboloid opening upwards, centred at the origin, and that the surface $z = 25 - 2x^2 - 2y^2$ is a paraboloid opening downwards centred at $(0,0,25)$. To find the curve of intersection, we set the two surfaces equal to one another:
$x^2 + y^2 = 25 - 2x^2 - 2y^2$, so $x^2+y^2 = r^2 = 25/3$. Thus the curve of intersection is a circle of radius $5/\sqrt{3}$ centred at the origin.

To find the volume of the region, let's do a triple integral. The triple integral will start at the lower surface $z = x^2+y^2$ and then go up to the top surface $z = 25 - 2x^2 - 2y^2$, and then goes in the circle.
$$\begin{eqnarray*}
V &=& \int_0^{2\pi}\int_0^{5/\sqrt{3}}\int_{x^2+y^2}^{25-2x^2-2y^2} r dz drd\theta\\
&=& \int_0^{2\pi}\int_0^{5/\sqrt{3}}(25-3r^2) r drd\theta\\
&=& \int_0^{2\pi} \left.\left(\frac{25 r^2}{2} - \frac{3r^4}{4}\right)\right|^{5/\sqrt{3}}_0 d\theta\\
&=& 2\pi \frac{25^2}{12}\\
&=& \frac{625\pi}{6}
\end{eqnarray*}$$
</div>
</div>

### Exercises

<ol>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
