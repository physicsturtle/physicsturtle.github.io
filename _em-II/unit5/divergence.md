---
layout: lesson
title: DIVERGENCE
course: calculus-III
unit: unit5
lessonID: divergence
nextID: curl
---

- Definitions of divergence and curl
- Geometric interpretations of divergennce and curl
- Divergence and curl in 2D and 3D

The divergence is a quantity that measures the, well, *divergence* of a vector field. Suppose we had a velocity field modelling fluid flow, and somewhere in this velocity field is a source that emits fluid. Fluid will then flow *away from* this source, and thus all of the velocity vectors will also point away from the source. The vector field would be *diverging* close to this source. On the contrary, suppose we had a sink that sucks up the fluid. The vectors would all be pointing towards the sink because the fluid is flowing there, and thus the vector field would have a *negative divergence*, or, convergence, there. 

Definition
$$\nabla\cdot\textbf{F} = \frac{\partial F_x}{\partial x} + \frac{\partial F_y}{\partial y} + \frac{\partial F_z}{\partial z}$$


This is the definition in cartesian coordinates. The definition is different in different coordinate systems, but the conceptual interpretation is the same. For the illustrations here, we will be looking at *two dimensional* vector fields only. Although the definition for three dimensional vector fields was given just above, we can also compute the divergence of a two dimensional vector field $\textbf{F}(x,y) = P(x,y)\hat{\textbf{x}} + Q(x,y)\hat{\textbf{y}}$ as follows

$$\nabla\cdot\textbf{F} = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y}$$

It is vector fields like these upon which our pictures will be based. We said before that the divergence of a vector field measures how much the vector field is spreading away at a certain point. 



### Alternative Definition
An alternative definition of the divergence which is more intuitive is 
$$\nabla\cdot\textbf{F} = \lim_{V\to 0} \frac{1}{V}\iint_{\partial V} \textbf{F}\cdot\hat{\textbf{n}} dS$$

Let's show that these definitions are equivalent. 









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
