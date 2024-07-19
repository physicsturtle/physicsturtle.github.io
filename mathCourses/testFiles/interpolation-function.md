---
layout: page
title: Interpolation from a Function
course: test
unit: unit1
permalink: /test/interpolation-function/
---

In the last section, we were interested in interpolating between data points. Sometimes, we might want to sample a smooth function $f$ on an interval, and then approximate it with an interpolating polynomial. One might wonder why we would want to approximate a function with a polynomial when we already have the exact function! There are uses for this, particularly in the context of numerical integration. 

Suppose we have smooth function $f$ defined on the interval $[a,b]$. We can sample $f$ at the points $x_0,x_1,\dots,x_n$ to get $f_i = f(x_i)$. 

Definition: A polynomial $p$ is said to *interpolate* $(x_0,y_0), (x_1,y_1), \dots, (x_n,y_n)$, if $p(x_i) = y_i$ for all $i = 0,\dots,n$. 

Now, how do we find such an interpolating polynomial? First, let's, let's define the *cardinal polynomials*. If we have $n+1$ distinct data points, then we define the cardinal polynomials to be 

$$L_{n,k}(x) = \frac{(x-x_0)(x-x_1)\cdots(x-x_{k-1})(x-x_{k+1})\cdots(x- x_n)}{(x_k-x_0)(x_k-x_1)\cdots(x_k-x_{k-1})(x_k-x_{k+1})\cdots(x_k- x_n)}.$$

These polynomials have the property that $L_{n,k}(x_i)$ is zero if $i \not= k$, and $1$ if $i = k$. Also observe that they are of degree $n$. This makes sense because an $n$th degree polynomial has $n+1$ degrees of freedom. We then construct the interpolating polynomial out of these cardinal polynomials by taking a linear combination:

$$p_n(x)= \sum_{k=0}^n f(x_k) L_{n,k}(x).$$



