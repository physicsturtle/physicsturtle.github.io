---
layout: lesson
title: Forms
dept: math
unit: unit7
course: math-methods
deptDisplay: Math
unitDisplay: Unit 7
courseDisplay: Mathematical Methods in Physics
---

In this section, we will discuss differential forms. 

<div class="definition">
<b>Definition:</b> A differential $k$-form $\omega$ is a $(0,k)$ tensor field which satisfies the following property:

$$\omega(X_1,X_2,\dots,x_k) = \sgn(\sigma)\omega(X_{\sigma(1)}, X_{\sigma(2)},\dots,X_{\sigma(k)})$$
</div> <br>

It is possible to have a notion of differentiation on $k$-forms. We define this as the following.

<div class="definition">
<b>Definition:</b> Let $\omega$ be a differential $k$-form. Then, define the $k+1$-form $d\omega$ to be

$$\begin{align*}
d\omega(X_1,\dots,X_k,X_{k+1}) =& \sum_{i=1}^{k+1}(-1)^{i+1}X_i(\omega(X_1,\dots,X_{i-1},X_{i+1},\dots,X_k)) \\
&+ \sum_{i < j}\omega([X_i,X_j],X_1,\dots,X_{i-1},X_{i+1},\dots,X_{j-1},X_{j+1},\dots,X_n)
\end{align*}$$

where $[X_i,X_j]$ denotes the commutator of the vector fields $X_i$ and $X_j$. 
</div> <br>

We have not shown that $d\omega$ is actually well-defined! I claimed that $d\omega$ was a $k+1$ form. It is clearly a $C^\infty(M)$ multilinear function, but it is perhaps not clearly antisymmetric. The verification of this is left to the exercises. 










































