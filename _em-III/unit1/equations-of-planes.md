---
layout: lesson
title: EQUATIONS OF PLANES
course: calculus-III
unit: unit1
lessonID: equations-of-planes
nextID: quadric-surfaces
---

- Equation form of line
- Parametrized form of line
- going between equation and parametrized form of line
- Equation form of plane
- Parametrized form of plane
- Formula with normal vector
- going between equation and parametrized form of line

As with the case of lines, there are two ways to define planes.

### Equation Form

Suppose we have a point $(x_0,y_0,z_0)$ which is in our plane, and the plane has normal vector \\((a,b,c)\\). Let \\(\textbf{r} = (x,y,z) \\) be a vector to some point in 3D space. Let's find a condition on this vector \\(\textbf{r}\\) such that its terminal point lies within the plane. If \\(\textbf{r}\\) points to the plane, then the vector \\(\textbf{r} - (x_0,y_0,z_0)\\) will be a vector that is parallel, or, tangent, to the plane. If it is tangent to the plane, its dot product with the plane's normal vector will be zero. Thus the condition we are left with is 

$$(a,b,c)\cdot(\textbf{r} - (x_0,y_0,z_0)) = 0$$

This can be expanded out to be 

$$a(x-x_0) + b(y-y_0) + c(z-z_0) = 0$$

or, moving the constant terms to the other side, 

$$ax + by + cz = ax_0 + by_0 + cz_0$$

where we can relabel the right hand side as \\(d\\):

$$ax + by + cz = d$$

### Parametric Form
In the parametric form, we express the plane in terms of a vector function of two parameters. Let $(x_0,y_0,z_0)$ be a point in the plane, and $\textbf{u}$ and $\textbf{v}$ be two non-collinear vectors that span the plane. Then we can write the plane as 

$$\textbf{r}(s,t) = \begin{bmatrix} x_0 \\ y_0 \\ z_0 \end{bmatrix} + s\textbf{u} + t\textbf{v}$$

### Exercises

<ol>
<li> <div> Find the point of intersection between the line $\textbf{r}(t) =  (3t -2)\textbf{i} + t\textbf{j} - (2t +5)\textbf{k}$ and the plane $z = 3x - 2y + 6$. Does there always exist a point of intersection between a line and a plane in $\mathbb{R}^3$?
</div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
With the line $\textbf{r}(t) =  (3t -2)\textbf{i} + t\textbf{j} - (2t +5)\textbf{k}$ and plane $z = 3x - 2y + 6$, we simply plug in the components of the line into the plane. Thus $(-2t - 5 = 3(3t - 2) - 2t + 6$. Solving for $t$ gives $t = -5/9$.

We plug this value of $t$ back into the equation of the line to find 
$$\textbf{r}(-5/9) =  -11/3\textbf{i} -5/9\textbf{j} -35/9\textbf{k}$$
So the point of intersection is $(-11/3, -5/9, -35/9)$.
</div> </li>

<li> <div> Calculate the minimum distance between the point $(9,0,-2)$ and the plane $z = 3x - 2y + 6$ </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
First, find the parametric form of the plane. First find 3 points inside the plane by inspection. Three points could be $(0,0,6)$, $(0,1,4)$, $(1,0,9)$. It doesn't matter what these are actually chosen to be; all would give the same answer.

By subtracting points, we can then find 2 vectors which are in the plane. \textbf{u} = \textbf{j} - 2\textbf{k} and \textbf{v} = \textbf{i} + 3\textbf{k}. If you are not convinced by this, take $\textbf{u} \times \textbf{v}$ and see that it is indeed the normal vector of the original plane. 

The parametric form of the plane is then $\textbf{r}(s,t) = s\textbf{i} + t\textbf{j} + (6-2t + 3s)\textbf{k}$ Then, the general vector between the point of interest $(9,0,-2)$ and the plane is:
$$\textbf{d}(s,t) = (s-9)\textbf{i} + t\textbf{j} + (8-2t+3s)\textbf{k}$$
Since the minimum distance between the point and plane occurs if the point lies along the normal vector to the plane, let's project the vector $\textbf{d}$ onto the normal vector of the plane, $\textbf{n} = \langle 3,-2,-1\rangle$. 
\begin{eqnarray*}
d &=& \left|\frac{\textbf{d}\cdot\textbf{n}}{\textbf{n}\cdot\textbf{n}}\right||\textbf{n}|\\
&=& \left|\frac{3s - 27 - 2t -8 + 2t - 3s}{9+4+1}\right|\sqrt{9+4+1}\\
&=& \frac{35}{\sqrt{14}}
\end{eqnarray*}
</div> </li>
</ol>
