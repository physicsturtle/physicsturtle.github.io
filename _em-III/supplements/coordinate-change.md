---
layout: lesson
title: CHANGE OF COORDINATES
course: calculus-III
unit: supplement
---

When I was first learning about different coordinate systems, I was never able to easily find a discussion on changing coordinates that was to my satisfaction. Here, I hope to remedy that situation for anybody who is learning about changing coordinates for their math or physics courses. This section is going to depart from the geometric arguments that we've used in the past to justify things like the volume element in spherical coordinates and such. Unfortunately, everything stems from the use of Cartesian coordinates and the definitions of gradient, divergence, and curl in terms of them. 

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






