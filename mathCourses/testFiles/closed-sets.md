---
layout: page
title: Closed Sets
course: test
unit: unit1
permalink: /test/closed-sets/
---

Let $(X,d)$ be a metric space, and $E\subset X$. Then $p$ is a limit point of $E$ if every neighbourhood of $p$ contains at least one point $q$ not equal to $p$ such that $q\in E$. 

Let $(X,d)$ be a metric space, and $E\subset X$. Then $E$ is closed if all limit points of $E$ are already in $E$.

Define $\overline{E} = E\cup E'$.

Theorems on closed sets:

Theorem: The set $\overline{E}$ is closed. 

Proof: Let $x$ be a limit point of $\overline{E}$. Then every neighbourhood of $x$ contains a point $y$ of $\overline{E}$. If this point $y$ is in $E$, then $x$ is a limit point of $E$, so $x\in E'\subset \overline{E}$. If $y\in E'$, then $y$ is a limit point of $E$, and so every ball around it contains a point of $E$. 
