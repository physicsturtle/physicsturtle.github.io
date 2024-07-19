---
layout: lesson
title: Squeeze Theorem
dept: math
course: calculus-I
unit: unit2
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 2
---

### Introduction
What happens to the function

$$f(x) = \frac{\sin x}{x}$$

as $x\to\infty$? The function $\sin x$ is always between positive and negative 1, but the function $1/x$ shrinks to be smaller and smaller as $x$ gets big. Even though $\sin x$ oscillates and has no limit, we can in fact assign a limit to the combination $f(x) = \frac{\sin x}{x}$ due to a result which we will state here.

### Theorem

<div class="theorem">
<b>Theorem:</b> Suppose $g(x)\leq f(x) \leq h(x)$ in the neighbourhood of a real number $a$, but not necessarily at $a$ itself. If $g$ and $h$ satisfy 
$$\lim_{x\to a} g(x) = L,\qquad \lim_{x\to a} h(x) = L,$$
then 
$$\lim_{x\to a} f(x) = L$$
also. This result is commonly referred to as the <i>squeeze theorem</i> or the <i>sandwich theorem</i>.
</div>

This result has an intuitive geometric interpretation

(insert picture here)

### Examples

<div class="example">
<p><b>Example:</b> Evaluate the limit
$$\lim_{x\to 0} x\sin\left(\frac{1}{x}\right).$$
</p>

</div>


<div class="example">
<p><b>Example:</b> Evaluate the limit
$$\lim_{x\to 0} (e^{-x}-1)\cos^2\left(e^{1/x^2}\right).$$
</p>

</div>


<div class="example">
<p><b>Example:</b> Evaluate the limit
$$\lim_{x\to 0} \sqrt{x+x^3}\cos\left(\frac{1}{x^3}\right).$$
</p>

</div>
