---
layout: lesson
title: Line Integrals in 2D
dept: math
course: calculus-III
unit: unit5
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 5
---

### Introduction

A line integral allows us to integrate a function along a line in the plane or in space. There are different line integrals that can be set up for any given line, each of which has its own physical interpretation. In order to calculate these quantities, let's start with the idea of dividing the integral up into tiny pieces and then summing together.

If we have some curve in the plane, $\textbf{r} : \mathbb{R} \to \mathbb{R}^2$, we can integrate any function whose domain is $\mathbb{R}^2$ along this curve. The function could be either a scalar function $f : \mathbb{R}^2 \to \mathbb{R}$, or a vector field $\textbf{F} : \mathbb{R}^2 \to \mathbb{R}^2$. Although there are different integrals that one can set up for these quantities with their own physical interpretations. Luckily, they are all done the same way mathematically. Consider the simplest problem of finding a length of a curve in the plane. To find the length of a curve that is winding through space, we will begin by parameterizing the curve with some variable $t$. Next we consider chopping the curve up into very small sections using our variable $t$. We can consider the length of one of these small sections by taking a snapshot of the curve between $t$ and $t + \Delta t$. In this interval, our parameterization maps out a small section of the curve that almost looks like a straight line and therefore the length of this section can be approximated by the hypotenuse of a triangle with side lengths $\Delta x$ and $\Delta y$. If we call this length $\Delta s$, then $$\Delta s = \sqrt{(\Delta x)^2 + (\Delta y)^2} \approx \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} \Delta t$$ if $\Delta t$ is small enough. From this we can see that the total length of the wire is $$\int_C \, ds = \int_{t_0}^{t_f} \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} \, dt$$    

We are very detailed in this case because many of the harder problems you may face reduce to this problem. For example, a common problem you may see is finding the mass of a wire with a density that varies in space. A common notation for these kind of integrals is $$\int_C \, f(\textbf{r}) \, ds$$ but again the procedure is the same, we parametize our path and we can then make $f$ a function of $t$ and compute the integral. $$\int_C \, f(\textbf{r}) \, ds = \int_{t_0}^{t_f} f(x(t), y(t)) \, \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} \, dt$$
Finally consider the problem of finding the work done along a curve $C$ in a force field $\textbf{F}$. Then the work is defined by
$$W = \int_C \textbf{F}\cdot d\textbf{r}.$$
The question is then how do we integrate this function? If we parametrize our curve by a variable $t$, we can write the integral as
$$W = \int_C \textbf{F}\cdot d\textbf{r} = \int_a^b \textbf{F}(\textbf{r}(t)) \cdot \frac{d\textbf{r}}{dt} dt.$$    

<div class="definition">
<b> Definition: </b>Suppose $C$ is a plane curve parametrized by $t$, and that its endpoints are $((x(a),y(a))$ and $(x(b),y(b))$, where $t$ ranges from $a$ to $b$. Then the line integral of $f$ along $C$ is:
    $$\int_C f(x,y) ds = \int_a^b f(x(t),y(t)) \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} dt.$$
</div>

Another common problem for line integrals is finding the flux through a curve enclosing a region. If we have a closed curve $C$ and a vector field $\textbf{F}$, then we can find the flux $\Phi$ through the region by the following integral:
$$\Phi = \int_C  \textbf{F}\cdot \hat{\textbf{n}} ds$$
where $\hat{\textbf{n}}$ is the outward pointing normal vector of the region. This normal vector can usually be written (unnormalized) as $\hat{\textbf{n}} = \left< \frac{dy}{dt} ,-\frac{dx}{dt} \right> $ This can be computed by again parametrizing the curve in terms of a parameter $t$:
$$\Phi = \int_C  \textbf{F}\cdot \hat{\textbf{n}} ds= \int_C \textbf{F}(\textbf{r}(t))\cdot \hat{\textbf{n}} \left|\frac{d\textbf{r}}{dt}\right| dt.$$

There are some theorems that are useful for the calculation of line integrals. The following is known as the fundamental theorem for line integrals.
\begin{theorem} \normalfont
Suppose $C$ is a smooth curve given by the function $\textbf{r} : [a,b] \to \mathbb{R}^2$ (or $\mathbb{R}^3$), and that $f$ is a differentiable function of two (or three) variables whose gradient vector $\nabla f$ is continuous on $C$. Then
$$\int_C \nabla f \cdot d\textbf{r} = f(\textbf{r}(b)) - f(\textbf{r}(a)).$$
\end{theorem}

Let's start with some examples.

Example: Integrate $f(x,y) = xe^y$ along the curve $y = x^2$, from $(-1,1)$ to $(1,1)$.


<div class="example>
<b> Example: </b>

Calculate the line integral of the vector field $\textbf{F} = \left<x^2-2xy, y^2-2xy\right>$ , from $(-1,1)$ to $(1,1)$ along the parabola $y = x^2$.

<div class="exampleSolution">
<b> Solution: </b>
First, we parametrize the curve that we're integrating along as $x = t$, $y = t^2$. This gives $\textbf{r}(t) = \left< t, t^2\right>$. Then, we plug this in to $\textbf{F}(\textbf{r}(t)) = \left<t^2 - 2t^3,t^4 - 2t^3\right>$ and integrate
$$\begin{eqnarray*}
\int_C \textbf{F}\cdot d\textbf{r} &=& \int_{-1}^1 \left<t^2 - 2t^3, t^4 - 2t^3\right>\cdot\left<1,2t\right> dt \\
&=& \int_{-1}^1 t^2 - 2t^3 + 2t^5 - 4t^4 dt\\
&=& \frac{2}{3} - \frac{8}{5}\\
&=& -\frac{14}{15}
\end{eqnarray*}$$
</div>
</div>














If we have the case of a space curve, then the definition becomes

$$\int_C f(x,y,z) ds = \int_a^b f(x(t),y(t),z(t)) \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 + \left(\frac{dz}{dt}\right)^2} dt$$




- Definition of a line integral
- Work and flux in the plane, line integral of a vector field
- Line integral of a scalar field
- Work in space, line integral of a vector field
- Line integral of a scalar field

Line integrals, not unlike integrals in a single variable, allow us to integrate along a one dimensional path, but this path need not be straight anymore. This means that we can calculate quantities like the work required to move along this path. Line integrals for work can be calculated in both 2 or 3 dimensions, but line integrals for flux are defined only for 2 dimensions.


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
