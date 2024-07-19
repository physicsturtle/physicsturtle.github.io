---
layout: lesson
title: Projections
dept: math
course: calculus-III
unit: unit1
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 1
---

### Introduction

When we write a vector as $\textbf{v} = (1,2,3)$, we are saying that the $x$ component of $\textbf{v}$ is 1, and the $y$ component of $\textbf{v}$ is 2. Another way of saying this, is if we *project* $\textbf{v}$ onto the $x$ axis, we get 1, and if we project $\textbf{v}$ onto the $y$ axis we get 2. Intuitively, one can think of projecting onto the $x$ axis as shining a lamp in a direction perpendicular to the $x$ axis, and then looking at the shadow on the $x$ axis. See the figure 

(insert figure here)

We are interested in projecting 2D or 3D vectors onto any vector in space, not just the $x$, $y$, or $z$ axes. In this section, we will develop some formulas for how that could be done. Note that we will not cover projecting onto planes in this course. If you are interested in that, please see a course on linear algebra.





Suppose we have two vectors, are we are interested in finding the component of one onto the other. This is known as projecting one vector onto another. Geometrically, the process of projecting a vector is shown in the figure below

(insert figure here)

If we project $\textbf{a}$ onto $\textbf{b}$, then we write this as:

$$\text{proj}_\textbf{b}\textbf{a} = \frac{\textbf{a}\cdot\textbf{b}}{\textbf{b}\cdot\textbf{b}}\textbf{b}$$

A remark about this formula is that if we scale the vector onto which we're projecting, the magnitude of the projection does not change! This makes sense, because what we're really doing is projecting onto the direction defined by the vector we're projecting onto; the vector's length doesn't matter. 
