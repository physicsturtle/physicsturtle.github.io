---
layout: lesson
title: Method of Characteristics
dept: math
course: pde-II
unit: unit1
deptDisplay: Math
courseDisplay: Partial Differential Equations II
unitDisplay: Unit 1
---

### Constant Coefficients

Consider the equation 

$$a u_x + b u_y = 0$$

where $a$ and $b$ are constants. We can rewrite this equation as 

$$(a,b)\cdot\nabla u = 0.$$

This means that the gradient of $u$ is orthogonal to the vector $(a,b)$. Recall that the direction of the gradient is the direction of greatest increase of a function. The direction perpendicular to the gradient is the direction along which the function is constant. What functions, when you plug in $(x,y) = \lambda(a,b)$, are depend only on $\lambda$? These functions are 

$$u(x,y) = f(bx - ay).$$

<div class="example">
<p><b>Example:</b> Solve the initial value problem 
$$\begin{cases}
2 u_t + 3 u_x = 0\\
u(x,0) = \sin x
\end{cases}$$
</p>
<b>Solution:</b> From before, we learned that $u(x,t) = f(2x-3t)$. Plugging in the initial condition, we have that $u(x,0) = f(2x) = \sin x$. Thus, $f(x) = \sin\left(\frac{x}{2}\right)$. Thus, 


$$u(x,y) = \sin\left(\frac{2x-3t}{2}\right).$$
</div>



<div class="example">
<p><b>Example:</b> Solve the following initial value problem. Hint: Use an integrating factor. 
$$\begin{cases}
u_x + u_t + 2u = 0\\
u(x,0) = \sin x
\end{cases}$$
</p>
<b>Solution:</b> Let's apply an integrating factor, which we could use on the $t$ derivative or the $x$ derivative. It doesn't matter. I will apply it on the $x$ derivative. 


</div>






### Variable Coefficients
Let's now consider the equation

$$a(x,y) u_x + b(x,y) u_y = c(x,y)$$

for the unknown $u$. Consider a curve $\r(s) = (x(s),y(s))$ in the plane. How does $u$ change along this curve? It changes according to the chain rule. 

$$\frac{du}{ds} = \frac{\partial u}{\partial x}\frac{dx}{ds} + \frac{\partial u}{\partial y}\frac{dy}{ds}.$$

If we call $a = dx/ds$ and $b = dy/ds$, we can write this as 

$$\frac{du}{ds} = a\frac{\partial u}{\partial x}+ b\frac{\partial u}{\partial y}.$$

If we match this with the original equation, then we see that 

$$\frac{dx}{ds} = a, \qquad \frac{dy}{ds} = b, \qquad \frac{du}{ds} = c.$$

We can eliminate $s$ by combining these equations 

$$\frac{dx}{a} = \frac{dy}{b} = \frac{du}{c}.$$

which are two coupled *ordinary differential equations*. 






