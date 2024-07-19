---
layout: lesson
title: CURVATURE AND TORSION
course: calculus-III
unit: unit2
lessonID: curvature-torsion
nextID: frenet-serret-equations
---

- Definitions of curvature and torsion using parametrization by arc length
- Formulas for curvature and torsion with time (not arc length)

### Definitions

Torsion and curvature are two quantities that describe geometric properties of a curve. Curvature can be defined for curves in either 2 or 3 dimensions, but has slightly different properties in each, and torsion can only be defined in three dimensions. Let's begin with the definitions. 

<div class="definition">
<b> Definition </b>
Let $\textbf{r}$ be a curve. Suppose $\textbf{T}$ is the unit tangent vector to $\textbf{r}$. Then, if $s$ is the arc length of $\textbf{r}$, we define the <i>curvature</i> $\kappa$ to be
$$\kappa = \left|\frac{d\textbf{T}}{ds}\right|$$
</div>

In two dimensions, we can actually define a *signed curvature*, whereas in three dimensions, curvature can only be nonnegative. We then define:

<div class = "definition">
<b> Definition </b>
 Let $\textbf{r}$ be a plane curve, and suppose $\textbf{T}$ is the unit tangent vector to $\textbf{r}$, and let $\textbf{N}$ be the unit vector rotated $90\degree$ counterclockwise from $\textbf{T}$. Then, 
$$\frac{d\textbf{T}}{ds} = \kappa\textxbf{N}$$
where $\kappa$ is the <i>signed curvature</i>.
</div>

<div class="definition">
<b>Definition </b>: Let $\textbf{r}$ be a space curve, and suppose $\textbf{T}$ is the unit tangent vector to the curve, and $\kappa$ is the curvature. Then the <i>normal vector</i> $\textbf{N}$ is given by
$$\frac{d\textbf{T}}{ds} = \kappa\textbf{N}.$$
</div>

Next, we define the binormal vector.

### Discussion 




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
