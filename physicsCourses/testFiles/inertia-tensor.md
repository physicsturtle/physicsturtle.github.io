---
layout: page
title: Inertia Tensor
course: test
unit: unit1
permalink: /test/inertia-tensor/
---

In physics, tensors are often introduced as matrices that transform vectors to vectors. Here, we will take that approach because it is the most physically intuitive. However, we want to be able to understand the inertia tensor in the more general tensor formulation that one would see in general relativity. That explanation will be postponed to another time.

### Review of Angular Velocity, Angular Momentum, Moment of Inertia

We start with angular velocity and angular momentum of a single particle. Suppose we have a particle moving in space, with its trajectory described by $\textbf{r}(t)$. Then, its velocity is $\frac{d\textbf{r}}{dt} = \textbf{v}(t)$. This velocity is independent of where the origin of coordinates is! Because, if we imagine shifting our origin, so that we are in a new coordinate system $\textbf{R}(t) = \textbf{r}(t) + \textbf{r}_0$, where $\textbf{r}_0$ is a constant shift, then we get $\frac{d\textbf{R}}{dt} = \frac{d\textbf{r}}{dt}$. Although the velocity is independent of position, the angular velocity is not! We define angular velocity to be the vector $\boldsymbol{\omega}(t) = \textbf{r}(t)\times\textbf{v}(t)/r^2$, where $r = \|\textbf{r}\|$. Clearly, $\boldsymbol{\omega}$ depends on $\textbf{r}$. To summarize, 

<div class="definition">
Definition: Suppose we have a point particle, and $\textbf{r}$ is its position vector with respect to the origin $O$. Let its velocity be $\textbf{v} = \frac{d\textbf{r}}{dt}$. Then, the <i> angular momentum of the particle with respect to $O$ </i> is
$$\boldsymbol \omega = \frac{\textbf{r}\times\textbf{v}}{r^2},$$
where $r = |\textbf{r}|$.
</div>

For a single particle, angular momtum is defined as $\textbf{L} = \textbf{r}\times\textbf{p}$. Although $\textbf{p} = m\textbf{v}$ does not depend on position, $\textbf{r}$ does, so we define:

<div class="definition">
Definition: Suppose we have a point particle, and $\textbf{r}$ is its position vector with respect to the origin $O$. Let its momentum be $\textbf{p} = m\textbf{v} = m\frac{d\textbf{r}}{dt}$. Then, the <i> angular momentum of the particle with respect to $O$</i> is 
$$\textbf{L} = \textbf{r}\times\textbf{p}.$$
</div>

At this point the idea of moment of inertia is quite simple, but we discuss it here because the nuances of the moment of inertia are better understood after having understood the single particle case. The moment of inertia of a point particle with respect to the origin $O$ is defined by 



Now, we proceed to angular velocity and angular momentum of a collection of $N$ point particles. For $N$ point particles, it is possible to define an angular momentum of the collection with respect to an origin $O$. This can actually be decomposed into two other quantities: The angular momentum of the centre of mass of the collection with respect to the origin, and the angular momentum of the collection witih respect to its centre of mass. 
<div class="definition">
Suppose there is a collection of $N$ point particles, whose positions are $\textbf{r}_1,\textbf{r}_2,\dots,\textbf{r}_N$ (all taken with respect to the same origin $O$),  and masses are $m_1,m_2,\dots,m_N$. The the total angular momentum of the system (with respect to $O$) is 
$$\textbf{L} = \sum_{i=1}^N \textbf{r}_i\times\textbf{p}_i$$
where $\textbf{p}_i = m_i\frac{d\textbf{r}_i}{dt}$ is the momentum of the $i$th particle. Simply replace the position vectors by the ones with respect to the centre of mass in order to find the angular momentum with respect to the centre of mass.
</div>

Now, we finally move on to rigid bodies. With rigid bodies, a very similar analysis to that of the collection of particles case occurs. This is because a rigid body can be thought of as a collection of very many very small particles.




### Introduction
If we have some rigid body rotating about its centre of mass, then its angular momentum with respect to its centre of mass, is $L = I\omega$, where $I$ is the moment of inertia with respect to the centre of mass, and $\omega$ is the angular velocity with respect to the centre of mass. 


### Exercises:
Given $\textbf{v} = \boldsymbol{\omega} \times\textbf{r}$, prove that 
$$\boldsymbol{\omega} = \frac{\textbf{r}\times\textbf{v}}{r^2}.$$



