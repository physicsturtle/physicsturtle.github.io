---
layout: lesson
dept: physics
title: Introduction
course: cm-III
unit: unit1
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 1
---

In this section, we will introduce the subject of the calculus of variations and briefly describe the types of problems that we intend to solve with it. The calculus of variations is a field of optimization. You will have seen before two types of optimization in calculus. In your first semester of calculus, we considered functions of the form $y = f(x)$. For these functions, we were able to calculate $f'(x)$ and then set $f'(x) = 0$, then solve for $x$. This value of $x$ is called a *stationary point* of $f$. In multivariable calculus, we considered functions of the form $u = f(x_1,x_2,x_3)$ (or maybe more variables), then set $\nabla u = 0$ and solved for points $(x_1,x_2,x_3)$ such that $\nabla f(x_1,x_2,x_3) = 0$. There, we had multiple variables and had to solve for all of them. The calculus of variations extends this idea to having *infinitely* many variables; we need to find the values of all of them in order to find the *stationary points*, whereby a point consists of infinitely many numbers. By infinitely many numbers, we search for a *function* $x(t)$. Picking a value of $t$ determines a value of $x$; there are infinitely many possible values of $t$ and thus infinitely many corresponding values of $x$. The argument $t$ can be thought of as a continuous analogue of a value of the subscript $x_1,x_2,x_3$ from the multivariable calculus case.

### Statement of the Problem
The problem that we are interested in solving is finding the stationary points of the integral

$$\begin{equation} \label{functional} S[x] = \int_a^b \L(t,x,\dot{x}) dt \end{equation}$$

over all functions $x$. The function $\L$ is called the *Lagrangian*, and $S$ is called a *functional*. A function takes as input a function (in our case, $x$ is the function), and spits out a real number (in our case, the value of the integral). To help you understand what the problem is, let's calculate $S$ for some various functions $x$. 

<div class="example">
<p><b>Example:</b> Let $S$ be defined by 
$$S[x] = \int_0^1 \left(tx^2 - \dot{x}^3\right )dt$$
Calculate $S$ for the following functions of $t$. Give the answer in terms of a decimal; feel free to use a computer to evaluate the integral. Which gives the smallest value of $S$?
<ol type = "a">
<li> $x(t) = t^2$ </li>
<li> $x(t) = \sin(\pi t)$ </li>
<li> $x(t) = e^t$ </li>
</ol></p>
<b>Solution:</b> 
For this fun
<ol type = "a">
<li> For the case $x(t) = t^2$, the Lagrangian becomes 
$$L = t^5 - 8t^3.$$
The integral is then 
$$S = \int_0^1 \left(t^5 - 8t^3\right) dt.$$
The value of the integral is $-1.833$ </li>
<li> For the case of $x(t) = \sin(\pi t)$, the Lagrangian becomes
$$L = t\sin^2(\pi t) - \pi^3 \cos^3(\pi t).$$
The integral is then 
$$S = \int_0^1 \left(t\sin^2(\pi t) - \pi^3 \cos^3(\pi t)\right) dt.$$
The value of the integral is $0.25$ </li>
<li> For the case of $x(t) = e^t$, the Lagrangian becomes
$$\L = t e^{2t} - e^{3t}$$
The integral is then 
$$S = \int_0^1 \left(t e^{2t} - e^{3t}\right) dt.$$
The value of the integral is $-4.264$ </li>
</ol>
The smallest value of $S$ was for the case $x(t) = e^t$.
</div>

<br> 

As we have seen in this example, depending on the form of $x(t)$, we get a different value for $S[x]$. It will be our goal to find functions $x$ which give the *smallest possible value of* $S$. Later, we will introduce boundary conditions, by which I mean we will only consider functions $x$ which satisfy $x(a) = A$ and $x(b) = B$, where $a,b,A,B$ are all given. 

### Examples
Let's now conclude the lesson by giving some examples of problems which lead to the optimization of a functional of the form $\eqref{functional}$. You are not expected to understand how we came up with these functionals, but rather just recognize that we are presenting problems in the calculus of variations. 

<div class="example">
<b>Example:</b> Consider two points $(x_1,y_1)$ and $(x_2,y_2)$ in the $xy$ plane. If one connects these two points by a curve $y = y(x)$, then one can calculate the length of this curve. What curve gives the shortest distance between the two points? The length $L$ (nothing to do with the Lagrangian that we mentioned before) of a curve $y = y(x)$ is 
$$L[y] = \int_{x_1}^{x_2}\sqrt{1+(y')^2} dx.$$
You will not be surprised to find out that the function minimizing this function is a straight line.
</div>

<br> 

<div class = "example">
<b>Example:</b> <i>The Brachistochrone Problem</i>. Consider rolling a ball without friction down a (possibly curved)
incline which connects two points. Which shape of incline minimizes the time it takes to roll from the top to the bottom? This is known as the brachistochrone problem. The time $T$ that it takes to traverse an incline of shape $y = y(x)$ is given by 
$$T[y] = \int_0^L \sqrt{\frac{1+(y')^2}{2gy}}dx.$$
</div>

<br>

<div class="example">
<b>Example:</b> Suppose we are interested in finding the surface area of a solid of revolution whose radii at the top and bottom are $y_1$ and $y_2$, respectively. What curve defining the boundary will cause the lateral surface area of the solid to be minimized? The surface area $S$ of such a solid is given by 
$$S[y] =  2\pi\int_{x_1}^{x_2} y\sqrt{1+(y')^2} dx.$$
We are thus interested in finding a function $y$ which causes $S$ to be a minimum, such that $y(x_1) = y_1$ and $y(x_2) = y_2$. 
</div>

<br>

<div class="example">
<b>Example:</b> The following is an example of contrained optimization, analogous to the study of Lagrange multipliers from multivariable calculus. If one lets a rope (length $L$) of uniform mass density $\mu$ hang between two points (separated in the $x$ direction by a distance $a$), what is the shape that it makes? For a given shape of rope $y = y(x)$, the potential energy $V$ of the rope is
$$V[y] = g\mu \int_0^a \left(y\sqrt{1+(y')^2} \right) dx$$
where we pick the heights of the endpoints by only allowing functions such that $y(0) = h_1$ and $y(a) = h_2$. An additional constraint that we must place on the function $y$ is that it must satisfy
$$L = \int_0^a \sqrt{1+(y')^2} dx,$$
where $L > a$. This is the constraint that the length of the curve $y(x)$ indeed matches the length $L$ of the given rope. The function $y$ (satisfying the boundary conditions) which minimizes the <i>potential energy</i> $V$ subject to the constraint of being length $L$ and satisfying the boundary conditions $y(0) = h_1$ and $y(a) = h_2$ is the shape that the rope will actually take. 
</div>

### Remarks
1. We usually use square brackets around the argument of a functional; we would write $S[x]$ instead of $S(x)$.

