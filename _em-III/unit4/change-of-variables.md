---
layout: lesson
title: CHANGE OF VARIABLES
course: calculus-III
unit: unit4
lessonID: change-of-variables
nextID: applications
---

- the jacobian revisited
- Changing bounds of integration
- Changing the function of itnegration
- Changing the area element

The process of changing variables for functions of several variables in order to calculate an integral is not quite as simple as it is for a function of a single variable. This is because we now have many different derivative combinations that we can take! How can we combine these to appropriately scale our area or volume element?

If we instead had a more general coordinate transformation $x = x(u,v)$, $y = y(u,v)$, we would write 
\[\iint f(x,y) dx dy = \iint f(x(u,v),y(u,v)) \left|\frac{\partial(x,y)}{\partial(u,v)} \right| du dv \]

where we define the \textit{Jacobian determinant} $\frac{\partial(x,y)}{\partial(u,v)}$ as

\[\frac{\partial(x,y)}{\partial(u,v)} = \begin{vmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\ \frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{vmatrix} = \frac{\partial x}{\partial u}\frac{\partial y}{\partial v} - \frac{\partial x}{\partial v}\frac{\partial y}{\partial u}\]

So that $\left|\frac{\partial(x,y)}{\partial(u,v)} \right|$ is actually the \textit{absolute value} of the determinant in the previous line. 

<div class="example">
<b> Example: </b>
Evaluate the double integral:

$$\iint_S(x-y)^2\sin^2(x+y)dxdy$$

where $S$ is the parallelogram with vertices $(\pi,0), (2\pi,\pi), (\pi,2\pi),(0,\pi)$.

<div class="exampleSolution">
<b> Solution:</b>
To evaluate this double integral, let's perform a change of variables, $u = x-y$ and $v = x+y$. This gives us the new corners for the paralellogram, which are $(u,v) = (\pi,\pi), (\pi,3\pi), (-\pi,3\pi), (-\pi,\pi)$. This is now a rectangle, which is easier to integrate over. The Jacobian determinant is
$$\begin{eqnarray*}
\left|\frac{\partial(x,y)}{\partial (u,v)}\right| &=& \left|\frac{\partial(u,v)}{\partial (x,y)}\right|^{-1} \\
&=& \begin{vmatrix}
1 & -1 \\ 1 & 1
\end{vmatrix}^{-1}\\
&=& \frac{1}{2}
\end{eqnarray*}$$
Thus our integral becomes

$$\int_{-\pi}^\pi \int_{\pi}^{3\pi} u^2\sin^2 (v) \frac{1}{2} du dv = \frac{\pi^4}{3}$$
</div>
</div>

### Exercises

<ol>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

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
