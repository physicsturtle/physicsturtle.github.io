---
layout: lesson
title: Infinite Square Well
dept: physics
course: qm-I
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 2
---

Here, we solve one of the simplest quantum mechanics problems, mathematically speaking. Later we will come to the spin-$\frac{1}{2}$ system, which one may argue is simpler mathematically, but the infinite square well I find to be more intuitive. 

Consider an infinite square well, defined by the potential 

$$V(x) = \begin{cases}
0 & 0 < x < L \\
\infty & \text{otherwise}
\end{cases}.$$

This system should be thought of, classically, as a box of length $a$ whose walls are infinitely tall, so a ball which you throw up could never get out. What this means in quantum mechanics is that the wavefunction, whose squared magnitude represents the probability of a particle being at that point in space, is zero outside the box. That is, $\psi(0) = \psi(L) = 0$, and at all other points outside the box as well. 

The Schrödinger equation and boundary conditions are for this equation in the region of $0 < x < L$ is

$$\begin{cases}
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} = E\psi & 0 < x < L \\
\psi(0) = 0 & \psi(L) = 0
\end{cases}$$

To solve this boundary value problem, we rearrange this equation to get 

$$\psi'' + \frac{2mE}{\hbar^2}\psi = 0$$

This equation has well known solution of sines and cosines, which give 

$$\psi(x) = A\sin(kx) + B\cos(kx)$$

Applying the boundary conditions, we find that $B = 0$, $A$ arbitrary, and we need $\sin(kL) = 0$. 






