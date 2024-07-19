---
layout: page
title: Power Series Review
course: test
unit: unit1
permalink: /test/power-series-review/
---

### Introduction
The reader has likely not had contact with power series since introductory calculus. This unit is based entirely on power series, so in order to remind the reader, we review some key definitions and properties for working with power series. 

### Definitions
In this section, we review some definitions relating to power series, and their basic properties.

<div class = "definition">
Definition: Let $\{a_n\}_{n=0}^\infty$ be a sequence of real numbers. Then, we call
$$\sum_{n=0}^\infty a_n(x-a)^n$$ 
a <i> power series </i>. The series is said "to be centred about $a$"
</div>

It is possible that a power series does not converge if we add up terms that are too big! We need a notion of when a power series converges or diverges; the result will depend on which $x$ you plug in.

<div class = "definition">
Definition: A power series $\displaystyle{\sum_{n=0}^\infty a_n(x-x_0)^n}$ is said <i> to converge at $x$ </i> if the limit
$$\lim_{N\to\infty} \sum_{n=0}^N a_n(x-x_0)^n$$
exists for that particular value of $x$. If $x = x_0$, the series will always converge (because we will be adding up a bunch of zeros). 
</div>

Before we introduce an important test for convergence, we remind you of the definition of absolute convergence, which should be familiar from introductory calculus.

<div class = "definition">
Definition: A power series $\displaystyle{\sum_{n=0}^\infty a_n(x-x_0)^n}$ is said to <i> converge absolutely </i> at $x$, if 
$$\sum_{n=0}^N |a_n(x-x_0)^n|$$ 
converges.
</div>

In general, there are three possible cases for convergence:
1. The power series may converge only for a single value of $x$, that is, $x = x_0$. 
2. The power series may converge absolutely for values of $x$ within a certain *radius of convergence* of $x$, i.e. it may converge for $|x-x_0| < R$, or for $|x-x_0| > R$. It is possible for the series to converge or diverge for $|x-x_0| = R$. 
3. The series may converge absolutely for all values of $x$, $-\infty < x < \infty$. 

We now present a test for convergence which you have seen before in introductory calculus. It is called the ratio test and allows one to test for absolute convergence.

<div class="theorem">
Theorem (Ratio Test): Let $\sum a_n$ be a series.
<ul>
<li> If $\displaystyle{\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right| < 1}$, then the series converges absolutely </li>
<li> If $\displaystyle{\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right| > 1}$, then the series diverges </li>
<li> If $\displaystyle{\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right| = 1}$, then the test is indeterminate; the series may converge or diverge. </li>
</ul>
</div>

The ratio test has the disadvantage of being indeterminate if the limiting ratio of coefficients approaches 1. In these cases, it is necessary to use other tests for convergence, such as the comparison test, limit comparison test, integral test, and so on. We now show how to calculate the *radius of convergence* of a power series. 

#### Radius of Convergence


present the definition of *radius of convergence*, which we mentioned earlier. 

<div class = "definition">
Definition: The radius of convergence $R$ of a power series is 
</div>


Have exercises about finding the radius of convergence
