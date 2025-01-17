---
layout: lesson
title: First order linear equations 
dept: math
course: green_functions
unit: unit2
deptDisplay: Math
courseDisplay: Green functions
unitDisplay: Unit 2
---
In a first course on ordinary differential equations, one of the early topics in the course is solving first order linear equations of the form 

$$\begin{equation}
y'(x) + p(x)y(x) = q(x), \quad y(0) = y_0
\end{equation}$$

As we have discussed in a first course, the way to solve this is by using an integrating factor. The integrating factor is \\(e^{\int p(x) \d x}\\), and if we multiply both sides by it we find 

$$\begin{align}
e^{\int_0^x p(x') \d x'} \frac{\d y}{\d x} + e^{\int_0^x p(x') \d x'} p(x) y(x) ={}& e^{\int_0^x p(x') \d x'} q(x) \\
\frac{\d}{\d x}(e^{\int_0^x p(x') \d x'}y(x)) ={}& e^{\int_0^x p(x') \d x'} q(x) \\
\int_0^x\left(\frac{\d}{\d x'}(e^{\int_0^{x'} p(x") \d x"}y(x'))\right) \d x' ={}& \int_0^x e^{\int_0^{x'} p(x") \d x"} q(x') \d x' \\
e^{\int_0^x p(x') \d x'} y(x) - y(0) ={}& \int_0^x e^{\int_0^{x'} p(x") \d x"} q(x') \d x' 
\end{align}$$

This allows us to find 

$$\begin{equation}
y(x) = y_0e^{-\int_0^x p(x') \d x'} + \int_0^x e^{\int_{x}^{x'} p(x") \d x"} q(x') \d x' 
\end{equation}$$

This tells us that the Green function for this system is 

$$\begin{equation}
G(x,x') = e^{\int_x^{x'} p(x") \d x"}
\end{equation}$$

and thus the solution can be written as 

$$\begin{equation}
y(x) = G(x,0)y_0 + \int_0^x G(x,x') q(x') \d x' 
\end{equation}$$

