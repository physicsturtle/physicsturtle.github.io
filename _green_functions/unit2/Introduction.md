---
layout: lesson
title: Introduction 
dept: math
course: green_functions
unit: unit2
deptDisplay: Math
courseDisplay: Green functions
unitDisplay: Unit 2
---
As we have discussed in the introduction section, a Green function is essentially the inverse of a differential operator that allows one to find the solution to a differential equation for an arbitrary input. In the same way that we want to solve for the unknown \\(\x\\) in the equation

$$A\x = \boldsymbol{b}$$

where \\(A,\boldsymbol{b}\\) are given, we are often interested in solving problems like:

<ol>
<li> The function \(y(x)\) in the first order linear differential equation 
$$\begin{equation}
y'(x) + p(x)y(x) = q(x), \quad y(0) = y_0
\end{equation}$$
In this case, \(y\) could represent the heat in a room over time. 
</li>
<li> The function \(x(t)\) for \(m\ddot{x} + b\dot{x} + k\cdot{x} = F(t)\), which represents the oscillations of a mass on a spring subject to a damping force and also an external driver. We would want to determine a general solution for the equation for an arbitrary \(F\).
</li>
<li> The electrostatic potential \(\phi(\x)\) due to some charge distribution \(\rho(\x)\). In this case we would want to solve 

\(\)\nabla^2\phi(\x) = -\frac{\rho(\x)}{\epsilon_0}\(\)
</li></ol>

Some of these problems you have already solved before, including by determining the Green function, in previous courses. The goal of this section is to solve these problems again, but through the lens of the Green functions. 

