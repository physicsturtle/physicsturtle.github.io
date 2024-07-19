---
layout: page
title: Bifurcations
course: test
unit: unit1
permalink: /test/bifurcations/
---

### Introduction
When one considers a system $\dot{x} = f(x)$, it is possible that there are some parameters in $f$. For example, in $f(x) = r - x^3 + x$, $r$ is a parameter. In a situation like this we change our notation and append an $r$: $\dot{x} = f(x,r)$. Depending on these parameters, the system could have different numbers of fixed points $x_\*$. A cubic like $r - x^3 + ax$ could have one, two, or three real roots, depending on the values of the coefficients. One can plot the set of roots as a function of $r$, which will be a few curves in the $r,x_\*$ plane. These curves may join up at a particular value of $r$, and when two of these curves join together, it is called a *bifurcation*. Our goal is to give examples of bifurcations and classify them. 

### Saddle Node Bifurcation
A *saddle node bifurcation*, also called a *fold bifurcation*, is characterised by having two distinct equilibrium points (i.e. solutions to $f(x) = 0$) for certain values of $r$, but as $r$ is varied, this becomes zero equilibrium points. An example of this is the equation $\dot{x} = x^2 - r$. Thus, $f(x,r) = x^2 - r$ has two solutions if $r > 0$, but no solutions if $r < 0$ (we are interested only in real solutions to $f(x,r) = 0$, recall). The solutions are, for nonnegative $r$, $x = \pm\sqrt{r}$. 

### Transcritical Bifurcation
A *transcritical bifurcation* is when there are multiple solutions to $f(x,r) = 0$, and as $r$ is varied, the number of fixed points does not change, but the stabilities of the fixed points do change. 

### Pitchfork Bifurcation
A *pitchfork bifurcation* is when there are already solutions, but solutions are added at a certain value of $r$. 






