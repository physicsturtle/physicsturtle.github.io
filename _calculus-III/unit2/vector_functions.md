---
layout: lesson
title: Vector Functions
dept: math
course: calculus-III
unit: unit2
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 2
---

- Parametric form of a curve
- Graphing a curve
- Transforming between parametric form and equation form

### Introduction
We are all familiar with curves in the plane. For example $y = x^2 $ is a curve in the 2D plane. That curve also has the property of passing the vertical line test (criteria of being a function). Today we will consider more general curves which do not need to pass the vertical line test, as well as 3 dimensional curves in space. We will discuss different ways of representing curves mathematically and introduce methods for studying these curves.

Often in single variable calculus, we had functions of the form $y = f(x)$; a single variable input and single variable output. Something else could write is $x = f(t)$, where, physically, this means the position $x$ of a particle as a function of the time $t$. 

<!--- (make javascript of particle moving) --->

It is often more interesting to consider a particle moving in 2 or 3 dimensions. Let's consider a function $\textbf{r}(t) = (x(t),y(t))$, or $\textbf{r}(t) = (x(t),y(t),z(t))$, describing the *vector valued* position of a particle in 2 or 3 dimensions. These functions trace out a curve in 2 or 3 dimensions as time is increased.

<!--- (make javascript of particle moving) --->

Since parametric equations are just vector valued functions, they can be added and subtracted and multiplied by scalars. The dot or cross product can also be taken between two vector valued functions. Similarly with the magnitude. 

### Definitions
<div class = "definition"> <b>Definition</b>: A <i>plane curve</i> is a function $\textbf{r} : I \to \mathbb{R}^2$, where $I = (a,b)$ is some open interval in $\mathbb{R}$. It is possible also that $I = \mathbb{R}$. </div>

Now we present an almost identical definition, the only difference being the range of the function.

<div class = "definition"> <b>Definition</b>: A <i>space curve</i> is a function $\textbf{r} : I \to \mathbb{R}^3$, where $I = (a,b)$ is some open interval in $\mathbb{R}$. It is possible also that $I = \mathbb{R}$. </div>

### Discussion

In single variable calculus, we studied functions like $y = f(x)$. This seems like a plane curve, but doesn't fit the form of the definition for plane curve above! If we want to express $y = f(x)$ in terms of so-called parametric equations, we write this as $x(t) = t$, and $y(t) = f(t)$.

### Examples
<ol>
<li> A straight line in any number of dimensions is parametrized by $\boldsymbol{\alpha}(t) = \textbf{a}t + \textbf{b}$. It goes through the point $\textbf{b}$ and in direction of $\textbf{a}$. The dimension of the line just depends on the dimension of the vectors $\textbf{a}$ and $\textbf{b}$. </li>
<li> A circle in the plane is parametrized by $\textbf{r}(t) = (\cos(t),\sin(t))$, $0\leq t < 2\pi$. 
</li>
<li> An alternate parametrization for the circle in the plane is $$\textbf{r}(t) = \left(\frac{1-t^2}{1+t^2}, \frac{2t}{1+t^2}\right)
</li>
<li> A helix is parametrized by $$\textbf{r}(t) = (\cos t,\sin t, t)$$ </li>
</ol>


### Exercises

<ol>
<li> <div> What are the \(x\), \(y\), and \(z\) components of the vector function \(\textbf{r}(t) = (\sin(t),\cos^2(2t),t^2e^t)\)? </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Consider the circle $x^2+y^2 = 1$. Find parametrizations $\gamma(t) = (x(t),y(t))$ satisfying the following conditions.

<ol "type=a">
<li> Clockwise, with $\gamma(0) = (0,1)$.
<li> The domain of $\gamma$ is $[0,\pi)$, and 
</ol></div>


<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li>  Plot the curve for $0 \leq t < 2\pi$ described by 

$$\textbf{r}(t) = (a\cos t, b\sin t),$$

where $a$ and $b$ are constants. 

</li>

</ol>
