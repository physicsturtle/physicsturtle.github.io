---
layout: lesson
title: Free Electron Model
dept: physics
course: ssp
unit: unit4
deptDisplay: Physics
courseDisplay: Solid State Physics
unitDisplay: Unit 4
---

The free electron model assumes that none of the electrons interact with one another, nor with the underlying lattice structure. One may think that this is a gross oversimplification of a solid, but the model actually makes some reasonable predictions in certain systems, namely metals. Of all the metals, alkali metals and alkali earth metals are the metals which are better described by the free electron model. 

The Schrödinger equation for the free electron model is written by setting $V(x) \equiv 0$:

$$-\frac{\hbar^2}{2m}\nabla^2\psi(\x) = E\psi(\x).$$

There are various boundary conditions that one can pick for the equation. Suppose that the system is confined to a cube with side length $L$. Two options for boundary conditions, which give rise to the same physics, are periodic boundary conditions, and zero boundary conditions. We will choose periodic boundary conditions. Namely, 

$$\psi(x,y,z) = \psi(x+L,y,z), \qquad \psi(x,y,z) = \psi(x,y+L,z),\qquad \psi(x,y,z) = \psi(x,y,z+L)$$

This gives us the solutions 

$$\psi_\k(\x) = A e^{i\k\cdot\x} + B e^{-i\k\cdot\x},$$

where all the components of $\k$ are positive. We can rewrite this in an easier way if we  throw out the $e^{-ikx}$ solution. This can be done if we decide instead that $k$ can be either positive or negative. Thus, 

$$\psi_\k(\x) = A e^{i\k\cdot\x}$$

and we now find the value(s) of $\k$ by plugging in the boundary conditions. This gives us that 

$$\k = \left(frac{2n_1\pi}{L}, \frac{2n_2\pi}{L},\frac{2n_3\pi}{L}\right)$$

where $n_1, n_2, n_3$ are integers (can be positive or negative). We normalize by setting $A = 1/\sqrt{V}$, where $V = L^3$ is the volume of the box. 





























