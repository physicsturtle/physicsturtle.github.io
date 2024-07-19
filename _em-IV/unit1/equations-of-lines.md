---
layout: lesson
title: EQUATIONS OF LINES
course: calculus-III
unit: unit1
lessonID: equations-of-lines
nextID: equations-of-planes
---


There are a few different ways to define a line in three dimensional space. 

### Parametric Form of a Line
A parametric equation is not a relationship between the spatial variables, but instead is a function of a *parameter*, usually $t$ for time, that, as it is increased, traces out the line. 

We learned before that we can draw a  vector $\textbf{r}_0 = (x_0,y_0,z_0)$ pointing from the origin to the point $(x_0,y_0,z_0)$. If we have the direction $\textbf{v}$ of a line, then we can trace out all the points on the line by starting at the point $\textbf{r}_0$, and then adding vectors of different lengths but in the same direction as $\textbf{v}$. This gives us the parametric equation 

$$\textbf{r}(t) = \textbf{r}_0 + \textbf{v}t$$

This can be visualized by (insert graphic here)

When we define a line like this, $\textbf{r}_0$ is not unique. We could have picked *any* point on the line!

### Equation Form of a Line

I personally don't like the "equation form" way of defining a line. I find it opaque and cumbersome. Nonetheless, we should know what it is and how to work with it. The equation form of a line is actually *two* equations. In particular, the equations of two planes. Two planes, if they aren't parallel, will intersect in a line. This line is the line defined by the equations of the two planes. 


### Switching Between Forms
One useful skill is switching between the equation form and the parametric form of a line. 


### Exercises

<ol>
<li> <div> Find the parametric form of the line which passes through $\textbf{a} = (1,2,3)$ and $\textbf{b} = (-1,-1,3)$. </div>
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>

<div  id="answer1" class="answer">
This is a plane that is parallel to the $xz$ plane. 
</div> </li>

<li> <div> Find the equation form of the line which passes through $\textbf{a} = (4,-1,1)$ in the direction $\textbf{b} = (0,2,1)​$. </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>

<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Find the equation form of the line which passes through $\textbf{a} = (4,-1,1)$ in the direction $\textbf{b} = (0,2,1)$. </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>


</ol>
