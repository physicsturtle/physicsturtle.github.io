---
layout: lesson
title: CHANGE OF COORDINATES IN TENSOR NOTATIOn
course: calculus-III
unit: supplement
---

This page is a repeat on the one about change of coordinates, but this time it will be in the tensor notation. This makes all of the calculations much easier.

Let the cartesian coordinates be denoted by $x^1,x^2,x^3$. The gradient is then 

$$\nabla f = \frac{\partial f}{\partial x^1} \hat{\textbf{e}}_x^1 + \frac{\partial f}{\partial x^2} \hat{\textbf{e}}_x^2 + \frac{\partial f}{\partial x^3} \hat{\textbf{e}}_x^3 = \frac{\partial f}{\partial x^i} \hat{\textbf{e}}_x^i$$

Here we are going to discuss how to find formulas for gradient, divergence, curl, and laplacian in various coordinate systems, starting from their definitions in Cartesian. We will aim to provide intuition for this, and also will give formulas for the most common coordinate transformations, namely cylindrical and spherical. We will have other coordinate systems as exercises. 

In cartesian coordinates, the definition of the gradient of a function \\(f = f(x,y,z)\\) is 

\\[ \nabla f = \frac{\partial f}{\partial x} \hat{x} + \frac{\partial f}{\partial y}\hat{y} + \frac{\partial f}{\partial z}\hat{z} \\]

When we express this in terms of another coordinate system, we can't only change the derivative terms. We must also change the unit vectors, which is what makes this so difficult. Here we will outline a general procedure for calculating the gradient, divergence, curl, and laplacian of a function in any orthogonal curvilinear coordinate system. 


Suppose that we have two coordinate systems, \\(x,y,z\\), and \\(u,v,w\\). We also have the relationships between them, 

$$\left\{\begin{eqnarray}
x &=& x(u,v,w) \\
y &=& y(u,v,z) \\
z &=& z(u,v,w)
\end{eqnarray}\right.
$$

### Unit Vectors
Any point in 3D space can be described by the position vector $\textbf{r}$. This position vector is a geometric object and should be independent of coordinates. In cartesian coordinates, the unit vectors are 

$$\hat{\textbf{x}} = \frac{\partial \textbf{r}}{\partial x}\left/\left|\frac{\partial \textbf{r}}{\partial x}\right|\right. ,\quad \hat{\textbf{y}} = \frac{\partial \textbf{r}}{\partial y}\left/\left|\frac{\partial \textbf{r}}{\partial y}\right|\right. ,\quad \hat{\textbf{z}} = \frac{\partial \textbf{r}}{\partial z}\left/\left|\frac{\partial \textbf{r}}{\partial z}\right|\right.$$

In any other coordinate system, we then define 

$$\hat{\textbf{u}} = \frac{\partial \textbf{r}}{\partial u}\left/\left|\frac{\partial \textbf{r}}{\partial u}\right|\right. ,\quad \hat{\textbf{v}} = \frac{\partial \textbf{r}}{\partial v}\left/\left|\frac{\partial \textbf{r}}{\partial v}\right|\right. ,\quad \hat{\textbf{w}} = \frac{\partial \textbf{r}}{\partial w}\left/\left|\frac{\partial \textbf{r}}{\partial w}\right|\right.$$

which means that we can express each of the unit vectors in the new coordinate system in terms of the unit vectors of the cartesian unit vectors. We define the *scale factors* 

$$h_1 = \left|\frac{\partial r}{\partial u}\right|,\quad h_2 = \left|\frac{\partial r}{\partial v}\right|,\quad h_3 = \left|\frac{\partial r}{\partial w}\right|$$

### Gradient
Now that we have the scale factors and unit vectors, we can express the gradient in any coordinate system. 






