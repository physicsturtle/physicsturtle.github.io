---
layout: page
title: potential-question
course: test
unit: unit1
permalink: /test/potential-question/
---

Consider a system with a spherical metal shell of radius $a$, and a spherical shell outside of it with inner radius $b$ and outer radius $c$. There is a potential difference of $V_0$ between the inner shell and outer shell. The potential is described by Laplace's equation

$$\nabla^2 V = 0$$

with boundary conditions $V(a) = $V_0$, and $V(b) = 0$. This is a radially symmetric system, so we rewrite this as 

$$\frac{1}{r^2}\frac{\partial}{\partial r}\left( r^2 \frac{\partial V}{\partial r}\right) = 0$$

Multiplying by $r^2$ and then integrating both sides gives us 

$$ r^2\frac{\partial V}{\partial r} = c_1$$

Now dividing by $r^2$ and integrating again, 

$$V = c_2 - \frac{c_1}{r}$$

If we plug in the boundary conditions, we get the final solution, which holds for $a < r < b$.

$$V(r) = \frac{V_0}{1-b/a}\left(1 - \frac{b}{r}\right)$$

Now, we can construct the full solution

$$V(r) = \begin{cases}
V_0 & 0 < r < a \\
\frac{V_0}{1-b/a}\left(1 - \frac{b}{r}\right) & a < r < b\\
0 & b < r < \infty
\end{cases}$$



