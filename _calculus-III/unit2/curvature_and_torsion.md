---
layout: lesson
title: Curvature and Torsion
dept: math
course: calculus-III
unit: unit2
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 2
---

- Definitions of curvature and torsion using parametrization by arc length
- Formulas for curvature and torsion with time (not arc length)

### Definitions

Torsion and curvature are two quantities that describe geometric properties of a curve. Curvature can be defined for curves in either 2 or 3 dimensions, but has slightly different properties in each, and torsion can only be defined in three dimensions. Let's begin with the definitions. 

<div class="definition">
<b> Definition </b>
Let $\textbf{r}$ be a space curve (range is $\mathbb{R}^3$). Suppose $\textbf{T}$ is the unit tangent vector to $\textbf{r}$. Then, if $s$ is the arc length of $\textbf{r}$, we define the <i>curvature</i> $\kappa$ to be
$$\kappa = \left|\frac{d\textbf{T}}{ds}\right|$$
</div>

Because the curve is not always given parametrized in terms of arc length, and it is not always easy to parametrize in terms of arc length, we can rewrite $\kappa$ in the following way. Assuming that $t$ is a valid change of parameter (i.e. $ds/dt$ is never zero), we get

$$\begin{eqnarray}

\kappa &=& \left|\frac{d\textbf{T}}{ds}\right| \\

&=& \left|\frac{d\textbf{T}/dt}{ds/dt}\right| \\

&=&  \frac{|\hat{\textbf{T}}'(t)|}{|\textbf{r}'(t)|}

\end{eqnarray}$$

Which allows us to calculate the curvature just in terms of derivatives with respect to $t$. 



In two dimensions, we can actually define a *signed curvature*, whereas in three dimensions, curvature can only be nonnegative. In two dimensions, we obtain the following definition.

<div class = "definition">
<b> Definition: </b>
 Let $\textbf{r}$ be a plane curve (range is $\mathbb{R}^2$), and suppose $\textbf{T}$ is the unit tangent vector to $\textbf{r}$, and let $\textbf{N}$ be the unit vector rotated $90\degree$ counterclockwise from $\textbf{T}$. Then, 
$$\frac{d\textbf{T}}{ds} = \kappa\textxbf{N}$$
where $\kappa$ is the <i>signed curvature</i>.
</div>

In this case, we have that $\kappa$ can be positive, negative, or zero. 

<div class="definition">
<b>Definition:</b> Let $\textbf{r}$ be a plane or space curve, and suppose $\textbf{T}$ is the unit tangent vector to the curve, and $\kappa$ is the curvature. Then the <i>normal vector</i> $\textbf{N}$ is given by
$$\hat{\textbf{N}} = \frac{1}{\kappa}\frac{d\textbf{T}}{ds}$$
</div>

The normal vector is only well defined if the curvature is nonzero. Next, we define the binormal vector, which only exists in 3 dimensions. 

<div class="definition">
<b>Definition:</b> Let $\hat{\textbf{T}}$ and $\hat{\textbf{N}}$ be the unit tangent and unit normal vectors, respectively. Then, the binormal vector is 
    $$\hat{\textbf{B}} = \hat{\textbf{T}}\times\hat{\textbf{B}}$$
</div>

<div class="definition">
<b>Definition:</b> Let $\hat{\textbf{B}}$ be the binormal vector to a curve, and $\hat{\textbf{N}}$ be the normal vector. Then, we define torsion $\tau$ by
    $$\tau = -\frac{d\hat{\textbf{B}}{ds}\cdot\hat{\textbf{N}}$$
</div>

For the definition of torsion, some books define it as $\tau = \frac{d\hat{\textbf{B}}{ds}\cdot\hat{\textbf{N}}$, without the negative. We

### Discussion 

After that slough of definitions, I think we need some discussion. First, let's look at what these things mean geometrically. First, let's do the two dimensional case.

(insert picture here)

For the three dimensional case, the picture is a bit more complicated:

(insert picture here)

### Examples




### Exercises

<ol>
<li> <div> Pose Question here </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>

<div  id="answer2" class="answer">
Coming soon.
</div> </li>

<li> <div> An osculating circle is defined as the circle that is in the plane spanned by $\hat{\textbf{T}}$ and $\hat{\textbf{N}}$, with radius of curvature equal to $1/\kappa$. Derive parametric equations for this circle as a function of the curve parameter. </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>

<div  id="answer2" class="answer">
Coming soon 
</div> </li>

<li> <div> Derive the following formulas for curvature and torsion in terms of the original variable $t$ for a curve. (see math 424 hw 1) </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>

<div  id="answer2" class="answer">
Coming soon 
</div> </li>







</ol>
