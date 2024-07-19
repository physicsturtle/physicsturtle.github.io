---
layout: page
title: Lie Groups
course: test
unit: unit1
permalink: /test/lie-group/
---

<div class="definition">
<b>Definition:</b> A <i>Lie group</i> (Lie is pronounced Lee, not Lai) is a set $G$ satisfying the following properties:
<ol type="i">
<li> $G$ is a group with group operation $*$ </li>
<li> $G$ is a smooth manifold (thus it is equipped with a topology and a smooth atlas) </li>
<li> The map $\mu : G\times G\to G$ defined by $\mu(g_1,g_2) = g_1 * g_2$ is smooth as a map from the product manifold $G\times G$ to $G$ </li>
<li> The map $i : G\to T$ defined by $i(g) = g^{-1}$ is smooth as a map from $G$ to $G$. </li>
</ol>
</div>

If the Lie group is also commutative, then it is called an Abelian Lie group. 

Now, we present some examples of Lie groups. 

1. If $G = \R^n$, and we consider it as a smooth manifold with identity as the only chard, then if the group operation is componentwise addition, it is a Lie group. Furthermore, it is a commutative Lie group. It is known as the "$n$-dimensional translation group".

2. The circle $\mathbb{S}^1$ is a commutative Lie group known as $U(1)$. The $U$ here stands for unitary, and the group operation is the multiplication of complex numbers.

3. If $G = \{A : \R^n \to \R^n | \det A \not= 0\} = GL(n,\R)$ is the general linear group, it is a Lie group with the group operation of matrix multiplication. It is noncommutative. 

4. The last example is the orthogonal group with respect to an inner product. This notion is likely unfamiliar to you, so we will present a couple definitions so that we can construct the group properly. 

Let $V$ be a $d$-dimensional vector space over $R$ equipped with a pseudo-inner product 
$$\left<\cdot,\cdot\right>: V\times V \to \R,$$
satisfying 
i. bilinearity
ii. symmetry
iii. non-degenerate

Note that we could require positive definiteness instead of non-degeneracy. 

Theorem: THere are (up to isomorphism) only as many pseudo inner products on $V$ as there are different signatures. 

If we define the set 
$$O(p,q) = \{\varphi : V\to V : \left<\varphi(v),\varphi(w) = (v,w)\}$$

then this is a subgroup of the general linear group $GL(p+q,\R)$. This Lie group is called the "orthogonal group with respect to the pseudo inner product $\left<\cdot,\cdot\right>$".

The Lorentz group from special relativity is $O(1,3)$ and $O(3,0)$ is the rotation group on $\R^3$. 


