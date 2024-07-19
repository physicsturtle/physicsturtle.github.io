---
layout: lesson
title: Double Integral over a General Plane Region
dept: math
course: calculus-III
unit: unit4
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 4
---

- Variable bounds of integration
- Swapping order of integration

The double integral over a rectangular region had constant bounds of integration. When considering regions that are not rectangular, we need to allow these bounds to be variable. 


### Exercises

<ol>
<li> <div> Find the volume in the first octant inside $y^2 + z^2 = 9$ and outside $y^2 = 3x$\\</div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
The graph of $y^2 + z^2 = 9$ is a cylinder in the $x$ direction with radius 3. The curve $y^2 = 3x$ is a parabola. We will integrate in $x,y$ To find the bounds for the double integral, graph $\displaystyle{ y^2+z^2=9 }$ and $\displaystyle{ y^2=3x }$ in the $xy$ plane. The first integral is easy:

\begin{eqnarray*}\int_{y=0}^{y=3}\int_{x=0}^{x=\frac{1}{3}y^2} \sqrt{9-y^2} \,dxdy &=& \int_{y=0}^{y=3} x\sqrt{9-y^2} \, \Big |_{x=0}^{x=\frac{1}{3}y^2} dy\\
&=& \int_{y=0}^{y=3} \frac{1}{3}y^2\sqrt{9-y^2} dy 
\end{eqnarray*}

To evaluate the integral in $y$, we need to make the substitution $y=3\sin(u)$, $dy=3\cos(u)du)$. The bounds transform as $u=\sin^{-1}(\frac{y}{3}) = \sin^{-1}(\frac{3}{3}) = \frac{\pi}{2}$.


\begin{eqnarray*}\int_{y=0}^{y=3} \frac{1}{3}y^2\sqrt{9-y^2} dy &=& \int_0^{\frac{\pi}{2}}\frac{1}{3}(9\sin^2(u))\sqrt{9-9\sin^2(u)}(3\cos(u))du\\
&=& \int_0^\frac{\pi}{2} 27\sin^2(u)\cos^2(u)du\\
&=& 27\int_0^\frac{\pi}{2} \sin^2(u)[1-\sin^2(u)] du\\
&=& 27\int_0^\frac{\pi}{2}\sin^2(u)du - 27 \int_0^\frac{\pi}{2}\sin^4(u)du\\
&=& \frac{27\pi}{16}
\end{eqnarray*}
</div> </li>

<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
