---
layout: page
title: Gaussian Beams
course: test
unit: unit1
permalink: /test/gaussiean-beam/
---

In this section, we will derive the Gaussian beam formula for the paraxial approximation. In this optics course, we will deal with scalar waves, so the wave equation we want to solve is 
$$(\nabla^2 + k^2) E = 0$$

If we suppose this is propagating in the $z$ direction, we can rewrite this equation by using the substitution $E = e^{ikz}\psi$. Plugging this in, 

$$\nabla^2 + 2ik\nabla\psi\cdot\hat{z} = 0$$

In the paraxial approximation, we say that 

$$\frac{\partial^2\psi}{\partial x^2} + \frac{\partial^2\psi}{\partial y^2} \gg \frac{\partial^2\psi}{\partial z^2},$$

which leads to the approximate equation 

$$\frac{\partial^2\psi}{\partial x^2} + \frac{\partial^2\psi}{\partial y^2} + 2ik\frac{\partial\psi}{\partial z} = 0.$$

We will search for cylindrically symmetric solutions. Thus, we leave the $z$ coordinate alone and transform to polar coordinates in $x$ and $y$. 

$$\frac{\partial^2\psi}{\parital r^2} + \frac{1}{r} \frac{\partial\psi}{\partial r} + \frac{1}{r^2}\frac{\partial^2\psi}{\partial\varphi^2} + 2ik\frac{\partial\psi}{\partial z} = 0.$$

Since we seek a solution which is cylindrically symmetric, we set the term with the $\phi$ derivative equal to zero. Thus,

$$\frac{\partial^2\psi}{\parital r^2} + \frac{1}{r} \frac{\partial\psi}{\partial r} + 2ik\frac{\partial\psi}{\partial z} = 0.$$

(fill in the motivation why)

We then rewrite $\psi$ as 

$$\psi(r,z) = A(z)\exp\left(\frac{ikr^2}{2q(z)}\right)$$

The derivatives of $\psi$ can now be written in terms of derivatives of $A$ and $q$, 

$$\frac{\partial\psi}{\partial r} = \frac{Aikr}{q}\exp\left(\frac{ikr^2}{2q(z)}\right),\qquad \frac{\partial^2\psi}{\partial r^2} = A\left(\frac{ik}{q} - \frac{k^2 r^2}{q^2}\right)\exp\left(\frac{ikr^2}{2q(z)}\right),\qquad \frac{\partial\psi}{\partial z} = \left(A' - \frac{Aq'ikr^2}{2q^2}\right)\exp\left(\frac{ikr^2}{2q(z)}\right)$$

If we simplify all the terms, we end up with the equation

$$2ik\left(\frac{A}{q} + A'\right) + \frac{Ak^2 r^2}{q^2}(q' - 1) = 0$$

Since the first term is independent of $r$, both terms are independently equal to zero:

$$\frac{A}{q} + A' = 0,\qquad q' = 1.$$

Thus, $q = q_0 + (z-z_0)$. This is often written as (justification?)

$$\frac{1}{q} = \frac{1}{q_r} + \frac{i}{q_i}$$

This leads us the following representation for $\psi$:

$$\psi = A(z)\exp\left(\frac{ikr^2}{w}\left(\frac{1}{q_r} + \frac{i}{q_i}\right)\right) = A(z)\exp\left(\frac{-kr^2}{q_i} + \frac{ikr^2}{2q_r}\right)$$


