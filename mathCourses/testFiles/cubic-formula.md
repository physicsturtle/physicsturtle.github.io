---
layout: page
title: The Cubic Formula
course: test
unit: unit1
permalink: /test/cubic-formula
---

### Introduction
Here, we present a simple solution to the cubic equation. No knowledge of abstract algebra is assumed, but rather only introductory calculus and linear algebra.

Solving polynomial equations is a very old problem, and it was proven that polynomials of degree five or higher have no formula for their solution. It is well understood how to solve the equation 

$$ax^2+bx+c = 0$$ 

through the quadratic formula

$$x = \frac{-b\pm\sqrt{b^2-4ac}}{2a}.$$

It is possible to derive a formula that solves 

$$ax^3 + bx^2 + cx + d = 0,$$

but this time it is much more involved than completing the square. Here, we will derive the formula that solves general cubic equation. 

### Moving the Inflection point
Starting from 

$$ax^3 + bx^2 + cx + d = 0,$$

we can, without loss of generality, we can write the general cubic as 

$$ \begin{equation} \label{eq:generalCubic}
x^3 + Ax^2 + Bx + C = 0
\end{equation} $$

because, assuming that the leading coefficient is nonzero, we can divide through by it to obtain Equation $\eqref{eq:generalCubic}$. The trick to solving this is first getting rid of the $x^2$ term. If we make a shift so that the inflection point moves to zero, then it will help us solve the equation. 

First, defining $f(x) = x^3 + Ax^2 + Bx + C$, we calculate $f^{\prime\prime}(x) = 6x + 2A = 0$, so that the inflection point is found to be at $x = -A/3$. Thus making the change of variables $x = X - A/3$, we can rewrite the equation:

$$X^3 + \left(B - \frac{A^2}{3}\right)X + \left(\frac{2A^2}{27} - \frac{BA}{3} + C\right) = 0$$

Now, we define new coefficients so that we can rewrite it simply as 

$$X^3 -3\alpha X -2\beta = 0,$$

$$\alpha = -\frac{1}{3} \left(B - \frac{A^2}{3}\right),\qquad \beta = -\frac{1}{2}\left(\frac{2A^2}{27} - \frac{BA}{3} + C\right) $$

### A Clever Substitution
Now, we focus on the equation

$$X^3 = 3\alpha X + 2\beta.$$

If $X = s + t$, for some values of $s$ and $t$, then we transform the equation into 

$$s^3 + 3s^2t + 3st^2 + t^3 = 3\alpha(s+t) + 2\beta$$

If we can find $s$ and $t$ such that $s^3 + t^3 = 2\beta$ and $3s^2t + 3st^2 = 3\alpha(t+s)$, or, equivalently $st = \alpha$, then our job is done. If we solve this system of two equations 

$$\begin{cases}
s^3 + t^3 = 2\beta \\
st = \alpha
\end{cases}$$

then we get that 

$$s^3 = \beta\pm\sqrt{\beta^2 - \alpha^3}, \qquad t^3 = \beta \mp \sqrt{\beta^2 - \alpha^3}.$$

Pick the positive sign for $s^3$ and the negative sign for $t^3$, 

$$s^3 = \beta+\sqrt{\beta^2 - \alpha^3}, \qquad t^3 = \beta - \sqrt{\beta^2 - \alpha^3}.$$

### Some Complex Arithmetic

In order to continue, we rewrite $t^3$ and $s^3$ in terms of complex exponentials:

$$s^3 = |t|^3e^{i\phi_s},\qquad t^3 =  |t|^3 e^{i\phi_t}$$

whereby the magnitudes are

$$|s| = \left|\beta + \sqrt{\beta^2 - \alpha^3}\right|^{1/3},\qquad |t| = \left|\beta - \sqrt{\beta^2 - \alpha^3}\right|^{1/3}.$$

For the angles, there are two subcases:

<ol>
<li> if $\beta^2 - \alpha^3 > 0$, then the angles $\phi_s$ and $\phi_t$ are both zero. </li>
<li> if $\beta^2-\alpha^3 < 0$ we use the formula

$$\phi_s = \atan\left(\sqrt{\alpha^3-\beta^2},\beta\right),\qquad \phi_t = \atan\left(-\sqrt{\alpha^3-\beta^2},\beta\right).$$
This tells us that $\phi_s = -\phi_t$. Let us define $\phi_s = \phi$ for the following calculations. We also note that in this case $\beta^2 - \alpha^3 < 0$, we know that $\alpha > 0$. 
</li>
</ol>

Now, we take cube roots of each, ensuring that $st = \alpha$ is maintained; we already know that $\|s\| \|t\| = \alpha$, so we need the angles of $s$ and $t$ to add up to $2\pi$.

$$s = |s| z e^{i\phi/3}, \qquad t = |t|z^2 e^{-i\phi/3},$$

where $z = e^{2\pi i n/3}$ for $n = 0,1,2$, which means that $st = \|s\| \|t\| z^3$, and since $z$ is a cube root of unity, $z^3 = 1$ and $st = \alpha$. 

This gives us three solutions, each corresponding to a value of $z$:

$$X =  |s| ze^{i\phi/3} + |t| z^2e^{-i\phi/3}$$

In terms of the original variable $x$, the solution is

$$x = -\frac{A}{3} +  |s| z e^{i\phi/3} + |t| z^2 e^{-i\phi/3}$$

The last step is to rewrite the equation in terms of the original 

### Discussion
A cubic equation always has three roots, but some may be complex. It is possible for a cubic equation to have one, or three real roots; sometimes in the three real roots cases we can have a repeated root like $b$ in $(x-a)(x-b)^2 = 0$, but we consider this to be the three real roots case. Now, when do we have three real roots and when do we have one? 

In the case that 
