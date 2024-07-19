---
layout: exercises
title: Equations of Planes - Exercises
dept: math
course: calculus-III
unit: unit1
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 1
---

### Exercises

<ol>
<li> <div class="exercise"> Find the point of intersection between the line $\textbf{r}(t) =  (3t -2)\textbf{i} + t\textbf{j} - (2t +5)\textbf{k}$ and the plane $z = 3x - 2y + 6$. Does there always exist a point of intersection between a line and a plane in $\mathbb{R}^3$?

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
With the line $\textbf{r}(t) =  (3t -2)\textbf{i} + t\textbf{j} - (2t +5)\textbf{k}$ and plane $z = 3x - 2y + 6$, we simply plug in the components of the line into the plane. Thus $(-2t - 5 = 3(3t - 2) - 2t + 6$. Solving for $t$ gives $t = -5/9$.

We plug this value of $t$ back into the equation of the line to find 
$$\textbf{r}(-5/9) =  -11/3\textbf{i} -5/9\textbf{j} -35/9\textbf{k}$$
So the point of intersection is $(-11/3, -5/9, -35/9)$.
</div> 
</div>
</div>
</li>

<li> <div class="exercise"> Calculate the minimum distance between the point $(9,0,-2)$ and the plane $z = 3x - 2y + 6$

<div class="answerBox">
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
</div> 
</div>
</div>
</li>
</ol>
