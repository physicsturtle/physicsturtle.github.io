---
layout: page
title: Lie Algebra
course: test
unit: unit1
permalink: /test/lie-algebra/
---

<div class="definition">
<b>Definition:</b> Let $(G,*)$ be a Lie group. Then, for any $g\in G$, there exists a map 
$$\ell_g : G\to G$$ 
where 
$$\ell_g(h) = g*h$$
and this map is called <i>the left translation with respect to $g$</i>.
</div>

Note that $\ell_g$ is a bijection for any $g$, but it is not a homomorphism on $G$. It is however a diffeomorphism on $G$. 

Recall that we could extend the pull-back (defined for covectors at a point) to covector fields without problems. However, the push-forward of a vector cannot be extended to the push-forward of a vector field unless the underlying smooth map is a diffeomorphism. This is because, if the underlying map is not surjective, there may be points on the target manifold which don't get vectors! There may also be multiple points in the domain mapped to the same point in the target, and the target point can't have multiple vectors! 

Thus, since $\ell_g$ is a diffeomorphism, we can push-forward vector fields with respect to it! This is done in the following way. Let $X$ be a vector field on $G$. (So, $X\in \Gamma(TG)$ is a smooth section of the tangent bundle). Let $g\in G$. Then, the action of $\ell_{g*}$ on the vector field $X$ (evaluated at the point $gh$) is given by the push forward of the vector at the point $h\in G$. 

$$(\ell_{g*}(X))_{gh} = \ell_{g*}(X_h)$$

<div class="definition">
<b>Definition:</b> Let $(G,*)$ be a Lie group, and $X$ a vector field on $G$. Then, $X$ is said to be <i>left invariant</i> if, for all $g\in G$, 
$$\ell_{g*}X = X.$$
Note that this equation is a vector field equation. To properly check it, we would need to evaluate both sides at a point $h$ in $G$, which would be given by (for all $h\in G$)
$$\ell_{g*}(X_h) = X_{gh}.$$
This equality can be extended further and be written as a scalar equation if we act on an arbitrary function $f$ with both sides of the equation.
</div> <br>

<div class="definition">
<b>Definition:</b> The set of all left-invariant vector fields on a Lie group $G$ is denoted by $L(G)$. This set of vector fields is a sub-module of $\Gamma(TG)$. 
</div> <br>

<div class="definition">
<b>Definition:</b> An <i>abstract Lie algebra</i> is a vector space $(L,+,\cdot,[\cdot,\cdot])$ over the field $K$. $L$ is the set of vectors, $+$ is the vector-vector addition, and $\cdot$ is the field-vector multiplication. The bracket $[\cdot,\cdot]$ is called <i>an abstract Lie bracket</i> and must satisfy 
<ol type="i">
<li>bilinearity </li>
<li>antisymmetry</li>
<li>the Jacobi identity
$$[x,[y,z]] + [y,[x,z]] + [z,[x,y]] = 0$$
</li>
</ol>
</div> <br>

An example of a Lie algebra is 
$$L = \Gamma(TM)$$
which forms a $\R$ vector space , and the Lie bracket is the commutator of vector fields. 

Note that any $C^\infty(M)$ module is an $\R$ vector space. 

Theorem: $L(G)$ is a Lie subalgebra of $\Gamma(TG)$. 

<div class="theorem">
<b>Theorem:</b> Let $e$ be the identity in $G$. Then, $L(G)\sim T_eG$ ($L(G)$ is isomorphic as a vector space to $T_e G$). In words, the vectors in the tangent space $T_eG$ are mapped bijectively into left-invariant vector fields. We are getting an entire vector field out of each vector! 
</div><br>

<div class="proof">
<b>Proof:</b> In order to show that these two vector spaces (over $\R$) are isomorphic, we need to construct a linear bijection between the two. Let's call this isomorphism $j$. Define $j : T_eG \to L(G)$ by 
$j(X)_g = \ell_{g*}X$. In words, the vector $X\in T_eG$ gets mapped to an entire vector field. This vector field can be evaluated at any point in the manifold, and the vector that is produced at any point $g$ is the push-forward of the identity to $g$ under the left translation map $\ell_g$. (includ a picture!)

Now, we need to check linearity, injectivity, and surjectivity. 


</div><br>
















