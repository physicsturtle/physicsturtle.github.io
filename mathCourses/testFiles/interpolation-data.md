---
layout: page
title: Interpolation
course: test
unit: unit1
permalink: /test/interpolation/
---

Suppose we have a set of data points $(x_0,y_0), (x_1,y_1), \dots, (x_n,y_n)$, and we are interested in interpolating it. There are various ways to interpolate such data. Here, we will look at using a polynomial over the entire interval $[x_0,x_n]$ to approximate the data at the points in between the given ones.

Definition: A polynomial $p$ is said to *interpolate* $(x_0,y_0), (x_1,y_1), \dots, (x_n,y_n)$, if $p(x_i) = y_i$ for all $i = 0,\dots,n$. 

Now, how do we find such an interpolating polynomial? First, let's, let's define the *cardinal polynomials*. If we have $n+1$ distinct data points, then we define the cardinal polynomials to be 

$$L_{n,k}(x) = \frac{(x-x_0)(x-x_1)\cdots(x-x_{k-1})(x-x_{k+1})\cdots(x- x_n)}{(x_k-x_0)(x_k-x_1)\cdots(x_k-x_{k-1})(x_k-x_{k+1})\cdots(x_k- x_n)}.$$

These polynomials have the property that $L_{n,k}(x_i)$ is zero if $i \not= k$, and $1$ if $i = k$. Also observe that they are of degree $n$. This makes sense because an $n$th degree polynomial has $n+1$ degrees of freedom. We then construct the interpolating polynomial out of these cardinal polynomials by taking a linear combination:

$$p_n(x)= \sum_{k=0}^n f(x_k) L_{n,k}(x).$$




