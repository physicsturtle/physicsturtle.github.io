---
layout: lesson
title: Equations of Planes
dept: math
course: calculus-III
unit: unit1
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 1
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

