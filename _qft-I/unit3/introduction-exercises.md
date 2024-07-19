---
layout: lesson
title: Tangents and Velocity
dept: math
course: calculus-I
unit: unit2
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 2
---

### Introduction
To provide some motivation for the study of calculus, we begin with a classic example. Suppose we are given the position $x$ of a particle as a function of time. We have learned before that the average velocity $\bar{v}$ of the particle from $t_1$ to $t_2$ can be calculated with the formula

$$\bar{v} = \frac{x(t_2) - x(t_1)}{t_2 - t_1}.$$

But this does not answer what the velocity $v$ at a particle time $t_1$ is! Now, one could imagine taking $t_2$ closer and closer to $t_1$ so that the average velocity approaches the velocity at $t_1$. This can be drawn pictorially in the following figure, where we see *secant lines*, which go through two points on the curve, approaching the *tangent line* at the point $t_1$. 

(isnert figure here)

The slope of the tangent line at $t_1$ is what we call the velocity of the particle at time $t_1$; no mention of average is made anymore. This process of taking the points $t_1$ and $t_2$ closer and closer together is known as a limiting process, and it leads us to the idea of taking the limit of a difference quotient to find the velocity at a point $t$:

$$v(t) = \lim_{h\to 0} \frac{x(t+h) - x(t)}{h}.$$









