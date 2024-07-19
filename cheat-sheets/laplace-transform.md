---
layout: page
title: Laplace Transforms
permalink: /cheat-sheets/laplace-transform/
---

First, let's get some notation straight. We define the Heaviside function

$$ u(t) = \left\{
\begin{array}{cc}
0, & t<0 \\
1, & t > 0
\end{array}  \right.
$$

and then the shifted Heaviside function as \\(u(t-a) = u_a(t)\\).

The delta function \\(\delta(t)\\) can't be defined in the same way. That is, in terms of a piecewise expression. It does indeed have the value of 0 at every value of \\(t\\) except \\(t = 0\\). However, its value is not defined at \\(t = 0\\). It does have the property that 

$$\int_{-\infty}^\infty \delta(t) dt = \int_{-\epsilon}^\epsilon \delta(t) dt = 1$$

no matter how small \\(\epsilon\\) is, as long as it is positive. What this means is that the delta function has area 1, despite being zero everywhere except at \\(T = 0\\).

The definition of the Laplace Transform is 

$$ F(s) = \int_0^\infty f(t)e^{-st} dt$$


### Common Laplace Transforms

| \\(f(t)\\)|\\(F(s)\\)|
|:---:|:---:|
| \\(1\\) | \\(\frac{1}{s}\\)|

