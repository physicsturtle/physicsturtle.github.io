---
layout: lesson
title: Introductory Problems 
dept: physics
course: cm-III
unit: unit3
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 3
---

The general prescription for solving problems with the Euler-Lagrange equations is the following:

<ol>
<li> Write down the positions of all of the particles in terms of Cartesian coordinates
</li>
<li> If there are any constraints leading to a more sensible coordinate system, express the Cartesian coordinates in terms of these new coordinates. Otherwise, skip this step.
</li>
<li> Compute the velocities of all of the particles
</li>
<li> Write down the potential and kinetic energies, and thus the Lagrangian
</li>
<li> Compute the Euler-Lagrange equation for each of the variables. 
</li></ol>

<div class="example">
<b>Example:</b>
Derive the equation of motion for the simple harmonic oscillator by using the Lagrangian method.


<b>Solution:</b> The position of the simple harmonic oscillator is \(x\). There are no constraints on this system. The velocity of the particle is \(\dot{x}\). The kinetic energy is given by 

$$\begin{equation}
T = \frac{m\dot{x}^2}{2}
\end{equation}$$

and the potential energy is \(V = \frac{1}{2}kx^2\). Thus, the Lagrangian is 

$$\begin{align}
L ={}& T - V \\
={}& \frac{m\dot{x}^2}{2} - \frac{1}{2}kx^2
\end{align}$$

The Euler-Lagrange equations are given by 

$$\begin{equation}
\frac{\d}{\d t}\frac{\partial L}{\partial \dot{x}} = \frac{\partial L}{\partial x}
\end{equation}$$

The partial derivatives of the Lagrangian are given by 

$$\begin{equation}
\frac{\partial L}{\partial x} = -kx, \qquad \frac{\partial L}{\partial \dot{x}} = m\dot{x}
\end{equation}$$

Thus, plugging these in to the Euler-Lagrange equation, we find that 

$$\begin{equation}
\frac{\d}{\d t}(m\dot{x}) = -kx
\end{equation}$$

This simplifies to the differential equation for the simple harmonic oscillator, which we have seen before in previous courses:

$$\begin{equation}
m\ddot{x} + kx = 0
\end{equation}$$

If we define \(\omega = \sqrt{k/m}\), then we can write this as 

$$\begin{equation}
\ddot{x} + \omega^2 x = 0
\end{equation}$$

As expected, we obtain the same result as in the usual case, and the solution is 
$$\begin{equation}
x(t) = A\cos(\omega t + \phi)
\end{equation}$$

</div>

From this example, we have seen that the equations of motion derived from Newtonian mechanics are reproduced exactly with the Lagrangian approach. The true power of the method is not obvious until we look at some more examples. As the next level of complexity, let us derive the equation of motion of a simple pendulum by using the Lagrangian approach. 

<div class="example">
<b>Example:</b>
Derive the equation of motion of a simple pendulum by using the Lagrangian approach.

\noindent<b>Solution:</b> 



</div>

Let us now consider a system which is quite difficult to study within the Newtonian framework. This is the most common example to demonstrate the true power of the approach. This is the double pendulum. The double pendulum 



