---
layout: page
title: Open Sets
course: test
unit: unit1
permalink: /test/open-sets/
---

Let $(X,d)$ be a metric space, and $E\subset X$. Then $p$ is an interior point of $E$ if there exists $r > 0$ such that $N_r(p)\subset E$. 

Let $(X,d)$ be a metric space, and $E\subset X$. Then $E$ is an *open set* if every point of $E$ is an interior point. 

Theorems on open sets:

Theorem: Every neighbourhood is an open set.

Proof: Consider a neighbourhood $E = N_r(p)$. Then let $q\in E.$ Since $q\in E$, $d(p,q) < r$. Since $d(p,q) < r$, there is a positive number $s$ such that $d(p,q) + s = r$. Then the ball $N_s(q)\subset N_r(p)$ because $x\in N_s(q)$ if $d(x,q) < s$, and $d(x,p) < d(x,q) + d(q,p) < s + r - s = r$, so $x\in N_r(p).$ 


Theorem: Let $(X,d)$ be a metric space. A set $E\subset X$ is open if and only if its complement is closed.

Proof: First, we show that $E^c$ is closed if $E$ is open. Since $E$ is open, every point $x\in E$ can be surrounded by a ball of some radius such that the entire ball lies in $E$. Let $y$ be a limit point of $E^c$. Then $\forall r > 0$, the ball of radius $r$ surrounding $y$ contains at least one point of $E^c$. Since this ball contains a point of $E^c$, the point $y$ cannot be an interior point of $E$. Because $y$ is not an interior point of $E$, it must then lie in $E^c$. Thus $E^c$ contains all of its limit points and is thus closed.

Now, we show that a subset $E$ is open if its complement is closed. Suppose $E^c$ is closed. Let $x\in E$. Then $x\not\in E^c$. Since $x\not\in E^c$, $x$ cannot be a limit point of $E^c$, because otherwise it would be in $E^c$. Since it is not a limit point of $E^c$, there exists a neighbourhood of it which contains no points of $E^c$. This means that the neighbourhood contains only points of $E$, so $x$ is an interior point. Thus all points of $E$ are interior points, so $E$ is open.


