---
layout: page
title: Quadrature
course: test
unit: unit1
permalink: /test/quadrature/
---

The trapezoidal rule is one way to estimate the area under a curve. We calculate area under a curve by computing the integral of the curve over a certain region. However, not all functions are easily integrated. What we can do instead is use an interpolating polynomial for a curve as a proxy function, and then integrate that because polynomials are easily integrated. 

Suppose we are interested in calculating the area under the curve $f(x)$ from $a$ to $b$. We can divide the interval $[a,b]$ up into $n$ segments, defining $x_i = \frac{b-a}{n}i + a$, so that $x_0 = a$ and $x_n = b$. 

We can define the cardinal polynomials $L_{n,k}(x)$ for this particular partition (independent of $f$), and from this an interpolating polynomial 

$$p(x) = \sum_{k=0}^n f(x_k)L_{n,k}(x).$$

We want to approximate:

$$\begin{eqnarray}
\int_{x_0}^{x_n} f(x) dx &\approx& \int_{x_0}^{x_n} p_n(x) dx \\
&=& \int_{x_0}^{x_n} \sum_{k=0}^n f(x_k)L_{n,k}(x) dx \\
&=& \sum_{k=0}^n f(x_k) \int_{x_0}^{x_n} L_{n,k}(x) dx \\
&=& \sum_{k=0}^n f(x_k) w_k \\
\end{eqnarray}$$

whereby we define the *weights*

$$ w_k = \int_{x_0}^{x_n} L_{n,k}(x) dx $$

If we choose $n = 1$, then we have the trapezoidal rule, and if we have $n = 2$, then we have Simpson's rule. The trapezoidal rule is so named because the interpolation is then a line, which reduces our problem to calculating the area under a trapezoid. 

### Errors 

We can find the error in calculating the integral by using the formula for the error in the polynomial interpolation. 

$$\begin{eqnarray}
\left|\int_{x_0}^{x_n} f(x) - p(x) dx \right| &=& \left|\int_{x_0}^{x_n} dx\right|\\

\end{eqnarra}$$
