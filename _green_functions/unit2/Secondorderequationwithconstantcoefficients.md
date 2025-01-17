---
layout: lesson
title: Second order equation with constant coefficients 
dept: math
course: green_functions
unit: unit2
deptDisplay: Math
courseDisplay: Green functions
unitDisplay: Unit 2
---
Another example which you have probably seen before is the second order equation with constant coefficients. There are countless physical realizations of this equation, but the two most common are the damped harmonic oscillator, and the RLC circuit. For simplicity, let us work with the damped harmonic oscillator since the interpretation is easier. Newton's second law for this system is 

$$m\ddot{x} = -b\dot{x} - kx + F(t)$$

whereby \\(F(t)\\) is an external driving force. The system is subject to initial conditions \\(x(0) = x\_0\\) and \\(\dot{x}(0) = v\_0\\). How can we determine \\(x(t)\\) in terms of an integral over some <i>Green function</i>, and \\(F(t)\\)? Well, we can use the Laplace transform. We recall that the Laplace transform of a function \\(x(t)\\) is given by 

$$x(s) = \int_0^\infty e^{-st} x(t) \d t$$

Then, if we do this to both sides of the equation we find 

$$\begin{align}
ms^2 x(s) + bs x(s) + kx(s) - smx_0 - mv_0 - bx_0 = F(s)
\end{align}$$









