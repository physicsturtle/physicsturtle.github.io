---
layout: lesson
title: Differentiation and Integration of Curves
dept: math
course: calculus-III
unit: unit2
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 2
---

In this section we introduce differentiation of curves and integration of curves. This is directly applicable to 2D and 3D kinematics of point particles, as well as the study of geometric properties of curves. It also lays the groundwork for topics later in the course where we will be integrating vector fields over curves.

We now want to discuss how to differentiate vector valued functions. The definition of differentiation of vector valued functions is identical to the definition for a single variable. 

<div class="definition">
<b>Definition:</b> The derivative of a curve $\textbf{r}:\mathbb{R}\to\mathbb{R}^n$ at a point $t$ is defined by
    $$\textbf{r}'(t) = \lim_{h\to 0}\frac{\textbf{r}(t+h) - \textbf{r}(t)}{h}.$$
If this limit does not exist at a particular point $t$, the derivative is said not to exist at $t$.
</div>

This derivative exists if and only if all of the *components* $(x_1,x_2,\dots,x_n)$ of $$\textbf{r}(t) = (x_1(t),x_2(t),\dots,x_n(t))$$ have derivatives at $t$.

<!--- It can be shown that this is equivalent to the condition that the derivatives of all the  components have derivatives. Show the proof --->

When computing this derivative in practice, we take the derivative componentwise. If $\textbf{r}(t) = (x_1(t),x_2(t),\dots,x_n(t))$, we can calculate its deerivative

$$ \frac{d\textbf{r}}{dt} = \left(\frac{dx_1}{dt},\frac{dx_2}{dt},\dots,\frac{dx_n}{dt}\right).$$

Geometrically, $\textbf{r}'(t)$ represents the *tangent* vector to the curve at the point $\textbf{r}(t)$. We then define the *unit tangent vector* by

$$\hat{\textbf{T}}(t) = \frac{\textbf{r}'(t)}{|\textbf{r}'(t)|}$$ 

#### Remark on Mechanics

Another word for the derivative of a curve is its velocity

### Derivative Properties

There are various properties of the derivative for plane and space curves. Some of these are the same as for functions $f : \mathbb{R}\to\mathbb{R}$, and some are new, but nonetheless intuitive. If $\textbf{r}_1(t)$ and $\textbf{r}_2(t)$ are functions $\textbf{r}_1,\textbf{r}_2 : \mathbb{R}\to\mathbb{R}^n$ and $\lambda$ is a constant, then the following properties hold.

<ol>
<li> The sum rule 
    $$\frac{d}{dt}(\mathbb{r}_1 + \mathbb{r}_2) = \frac{d\textbf{r}_1}{dt} + \frac{d\textbf{r}_2}{dt}$$
</li>
<li> The scalar multiplication rule $$\frac{d}{dt}(\lambda\textbf{r}) = \lambda\frac{d\textbf{r}}{dt}$$
</li>
<li> The product rule for dot products
    $$\frac{d}{dt}(\textbf{r}_1\cdot\textbf{r}_2) = \frac{d\textbf{r}_1}{dt}\cdot\textbf{r}_2 + \textbf{r}_1\cdot\frac{d\textbf{r}_1}{dt}$$
</li>
<li> The product rule for cross products
    $$\frac{d}{dt}(\textbf{r}_1\times\textbf{r}_2) = \frac{d\textbf{r}_1}{dt}\times\textbf{r}_2 + \textbf{r}_1\times\frac{d\textbf{r}_2}{dt}$$
</li>

</ol>

### Integration
Integration for curves is defined componentwise. This is identical to how differentiation is defined. If we have a curve $\textbf{r} : \mathbb{R}\to\mathbb{R}^n$, then in symbols, 

$$\int_a^b \textbf{r}(t) dt = \left(\int_a^b x_1(t) dt, \int_a^b x_2(t) dt,\dots,\int_a^b x_n(t) dt\right)$$

This way of integrating a curve is not used very often, except perhaps when doing kinematics of particles moving in several dimensions. We will not enter a lengthy discussion of integration of curves here.


### Exercises

<ol>
<li> <div> Compute the unit tangent vector to the curve $$\textbf{r}(t) = (t\cos t, t\sin t)$$ </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>

<div  id="answer2" class="answer">
Coming soon 
</div> </li>

<li> <div>  Suppose the velocity of a particle is given by $\textbf{v}(t) = (3t,-2t^2)$. Find its position as a function of time if $\textbf{r}(0) = (1,0)$.  </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>

<div  id="answer2" class="answer">
Coming soon 
</div> </li>

</ol>
