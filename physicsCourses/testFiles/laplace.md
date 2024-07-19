---
layout: page
title: Laplace Equation
course: test
unit: unit1
permalink: /test/laplace/
---

Here we solve the Laplace equation $\nabla^2 u = 0$ in spherical coordinates. We will separate variables so that the radial part of the equation and angular part of equation so that we could solve the equation in either a bounded or unbounded spherically symmetric domain. 

$$\begin{equation}
\frac{1}{r^2}\frac{\partial}{\partial r}\left( r^2 \frac{\partial u}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial u}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2 u}{\partial\varphi^2}
\end{equation}$$

This equation can be solved by separation of variables, $u = R(r)Y(\theta,\varphi)$. We substitute this in and divide through by $RY$ and multiply by $r^2$:

$$\begin{equation}
\frac{1}{R}(r^2 R')' + \underbrace{\frac{1}{ Y\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial Y}{\partial\theta}\right) + \frac{1}{Y\sin^2\theta}\frac{\partial^2 Y}{\partial\varphi^2}}_{\ell(\ell + 1)} = 0
\end{equation}$$

Instead of setting a generic eigenvalue $\lambda$, we label it $\ell(\ell+1)$. This means that we are restricting the eigenvalue to be greater than or equal to $-1/4$, which is the minimum of $\ell(\ell+1)$. We will see that this clever choice will help us out later.

We now 











