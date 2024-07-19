---
layout: lesson
title: CURL
course: calculus-III
unit: unit5
lessonID: curl
nextID: laplacian
---

- Definitions of divergence and curl
- Geometric interpretations of divergennce and curl
- Divergence and curl in 2D and 3D

The curl is an operation which can only be defined in three dimensions. 


#### Frequently Asked Questions

If we want to define curl in a different coordinate system, such as spherical, can we use the same definition? That is, if \\(\textbf{F} = F_r\hat{\textbf{r}} + F_\theta\hat{\boldsymbol{\theta}}+F_\varphi\hat{\boldsymbol{\varphi}}\\), can we say that

$$ \nabla\times\textbf{F} = \begin{vmatrix} \hat{\textbf{r}} & \hat{\boldsymbol{\theta}} & \hat{\boldsymbol{\varphi}} \\  \frac{\partial}{\partial r} & \frac{\partial}{\partial\theta} & \frac{\partial}{\partial\varphi} \\ F_r & F_\theta & F_\varphi \end{vmatrix} ?$$

The answer is **no**. 

Memory trick for the curl: Just remember that the first elmenet is $\partial F_z/\partial y$, and then we get permutations. $z\to y\to x$ and cyclic for the vector component, use logic to determine derivatives and unit vectors


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
