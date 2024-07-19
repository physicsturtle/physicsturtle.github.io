---
layout: lesson
title: Multivalued Functions
dept: math
course: complex-variables
unit: unit2
deptDisplay: Math
courseDisplay: Complex Variables
unitDisplay: Unit 2
---

### Introduction

There are many functions whose inverse function is multi-valued. For example, inverting any of the following functions (for complex $z$)

$$f(z) = z^2, \qquad f(z) = \sin z,\qquad f(z) = \cos z,\qquad f(z) = e^z$$

will produce multiple values. In the world of calculus of a real variable, all of these have mutivalued inverses except the exponential. In the calculus of complex variables, we have to recall the polar form of complex numbers $z = re^{i\theta}$. Notice that changing $\theta$ by $2\pi$ would produce the same value of $z$. Thus, if we take the logarithm of both sides, we get $\log z = \log r + i(\theta + 2\pi n)$, where $n\in \Z$. Thus $\log z$ can take multiple values. 

To visualize how these multivalued inverse mappings work, consider $w = f(z)$, where $f(z)$ is a single valued function. The multivalued inverse goes from the $w$ plane to the $z$ plane, and maps the same value of $z$ to different values of $w$.

(insert many to one inverse schematic here)

**Remark:** Strictly speaking, a *multivalued function* isn't a function at all! It is simply terminology that we use in complex analysis to describe the kinds of relations that we are studying in this section. 

### Logarithm Function
All multivalued function inverses in complex analysis can be related back to the logarithm function, so we study the logarithm first. Suppose we have the equation 
$$z = e^w;$$
we want to solve for $w$ in terms of $z$ (note that this is the opposite of the notation that we used in the introduction, where it was $w = e^z$). For a given $z = re^{i\theta}$, where $\theta = \Arg(z)$ (recall that $-\pi < \Arg(z) \leq \pi$), we want to write $w = u + iv$. The equation is thus 
$$r e^{i\theta} = e^{u + iv}.$$

This allows us to work entirely in terms of real numbers! If we take the magnitude of both sides, then we find that $r = e^u$. Thus, $u = \ln r$. We use $\ln$ here to mean the natural logarithm of real argument only. This is conventional in complex analysis; for the (multivalued) natural logarithm of a complex number, we use $\log$. For the imaginary part, we get $v = \theta + 2\pi n = \Arg(z) + 2\pi n$, where $n\in \Z$ is any integer. Putting these together, and recalling that $r = \|z\|$ and $\theta = \Arg(z)$, we have our expression for $w$:

$$w = u + iv = \ln|z| + i[\Arg(z) + 2\pi n].$$

<div class="definition">
<b>Definition:</b> Let $z\in\C$ be a complex number. Then, we define the <i>multivalued logarithm of $z$</i> to be
$$\log z = \ln|z| + i(\Arg(z) + 2\pi n).$$
</div>

This definition is equivalent to saying that 

$$\log z = \ln|z| + i\arg(z),$$

because $\arg z$ is multivalued. It is possible to define a single valued logarith by simply picking one value for its imaginary part. We call this value the *principal value*.

<div class="definition">
<b>Definition:</b> Let $z\in \C$ be a complex number. Then, we define the <i>principal value of the logarithm of $z$</i> to be 
$$\Log z = \ln |z| + i\Arg(z).$$
</div>

### Continuity of the Logarithm
We now examine the continuity of the logarithm. Since $\Log z$ is an actual function (because it is single valued), this is actually a valid question. If we consider any point on the negative real axis, or, the line $\theta = \pm \pi$. 

* If we consider $z = x + i\epsilon$ for $x < 0$ and and $\epsilon\to 0^+$, then $\log z \to \ln\|x\| + i\pi$.
* If we consider $z = x + i\epsilon$ for $x < 0$ and $\epsilon \to 0^-$, then $\log z \to \ln\|x\| - i\pi$. 

Thus the limits from opposite sides don't agree, so $\Log z$ is not continuous across the line $z = x$ for $x < 0$. 

<div class="example">
<p><b>Example:</b> Calculate the following values of the logarithm:
<ol type="a">
<li> $\log(i)$ </li>
<li> $\log(-i + \sqrt{3})$ </li>
<li> $\Log(-2+2i)$ </li>
</ol> </p>
<b>Solution:</b>
<ol type="a">
<li> $\log(i)$ </li>
<li> $\log(-i + \sqrt{3})$ </li>
<li> $\Log(-2+2i)$ </li>
</ol>
</div> <br>

There are certain identities which hold for the multivalued logarithm $\log$ which do not hold for the single valued logarithm $\Log$, and vice versa. 

LOGARITHM IDENTITIES HERE WITH PROOFS


### Exponents
Suppose $\alpha\in\C$ and $z\in\C$ is a nonzero number. Then, we can consider the function $f(z) = z^\alpha$. 

<div class="definition">
<b>Definition:</b> Suppose $\alpha\in\C$ and $z\in\C$ is a nonzero number. Then, we define $z^\alpha$ to be the multivalued function
$$z^\alpha = e^{\alpha\log z} = e^{\alpha[\ln|z| + i\Arg(z) + 2\pi n]},\qquad n\in \Z.$$
</div> <br>

This definition can be further explored in certain subcases. 
1. Suppose $\alpha = \beta + \gamma i$. If $\beta$ and $\gamma$ are both rational numbers, then $z^\alpha$ is a finite set of numbers. 
2. If $\alpha = \beta + \gamma i$ and $\beta$ and $\gamma$ are both integers, then $z^\alpha$ is a single number.  
3. If $\alpha$ is purely real, then we can simplify the expression to be $z^\alpha = \|z\|^\alpha e^{i\alpha[\Arg z + 2\pi n]}$, so that $z^\alpha$ forms a set whose magnitude is always the same for every $n$, but whose phase rotates around the circle of radius $\|z\|^\alpha$.
4. If $\alpha = \beta i$ is purely imaginary, then we can simplify the expression to be $z^\alpha = \|z\|e^{-\beta[\Arg(z) + 2\pi n]}e^{i\beta\ln \|z\|}$, so that $z^\alpha$ forms a set whose phase is the same for every $n$, but whose magnitude is always on a ray of angle $\beta\ln\|z\|$. 

<div class="definition">
<b>Definition:</b> The <i>principal value</i> of $z^\alpha$ is defined to be 
$$z^\alpha = e^{\alpha\Log z} = e^{\alpha[\ln|z| + i\Arg(z)]}.$$
</div>

<div class="example">
<p><b>Example:</b> Find all values of $z$ satisfying $z^{2-i} = 3$. </p>
<b>Solution:</b> 

</div>

In our discussion of the logarithm and its multivalued nature, we defined the principal value as a particular one of these multiple values. We could have defined the principal value as a different one of the multiple values! This leads us to the definition of a *branch*. 

<div class="definition">
<b>Definition:</b> Let $f(z)$ be a multivalued function in a domain $D$. Then, $F(z)$ is said to be a <i>branch</i> of $f(z)$ if the following conditions hold:
<ul>
<li> $F(z)$ is single-valued in $D$ </li>
<li> $F(z)$ is continuous in $D$ </li>
<li> $F(z)$ is one of the values of $f(z)$ </li>
</ul>
</div>

<div class="definition">
<b>Definition:</b> Let $f(z)$ be a multivalued function. Then, $z_\*$ is said to be a <i>branch point</i> of $f$ if, for every circle enclosing $z_\*$, $f(z)$ changes discontinuously. 
</div>

To actually construct a branch of a function, we have to draw a curve going outward from the branch point, which allows us to ensure the branch is single valued. In order to get a thorough understanding of the topic, one needs to consider Riemann surfaces, which are outside the scope of the course. 

<div class="example">
<p><b>Example:</b> Let $f(z) = \log z$ be the multivalued logarithm. 

</div>


<div class="definition">
<b>Definition:</b> A <i>branch cut</i> of a multivalued function $f$ is a curve across which $f$ is discontinuous. 
</div>












































