---
layout: page
title: Direct Sum
course: test
unit: unit1
permalink: /test/direct-sum/
---

In this section, we will discuss the *direct sum* between two vector spaces.

<div class="definition">
<b>Definition:</b> Let $(V,+_V,\cdot_V)$ and $(W,+_W,\cdot_W)$ be vector spaces over the same field $F$. Then, we define the <i>direct sum</i> vector space by
$$V\oplus W = \{(v,w) | v\in V, w\in W\}.$$
Let $a,c\in V$, $b,d\in W$, and $\lambda \in F$. The sum operation $+: (V\oplus W) \times (V\oplus W) \to V\oplus W$ is defined by 

$$(a,b) + (c,d) = (a+c,b+d),$$
and the scalar multiplication $\cdot : F \times (V\oplus W) \to V\oplus W$ by 

$$\lambda(a,b) = (\lambda a, \lambda b).$$
</div>

Right now, we have not proven that this is a vector space, but rather just a set with some operations on it. The proof that it is a vector space is left to the exercises. 

### Operators

Now that we have a vector space, we can construct operators on the space. 
<div class="definition">
<b>Definition:</b> Let $A : V\to V$ and $B : W\to W$ be linear maps on on their respective vector spaces. Define the map
$$A\oplus B : V\oplus W\to V\oplus W$$
by 
$$(A\oplus B)(v,w) := (Av,Bw).$$
</div>


### Basis
How can we inherit a basis from the consitituent vector spaces to the direct sum space? Let $e_i$ be a basis for $V$, and $f_j$ be a basis for $W$. 

