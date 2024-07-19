---
layout: lesson
title: L'Hopital's Rule
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---

### Introduction
We have encountered many limits so far in this course. For some of them, we could simply plug in the value and we would get the answer. For example, we can just plug $x = 2$ into the following:

$$\lim_{x\to 2} \sqrt{11x + 3} = 5.$$

We also encountered cases where we ran into trouble if we naïvely plugged in the value of $x$. Such cases lead to $\frac{0}{0}$, or $0\times\infty$. For example, the two limits

$$\lim_{x\to 0} \frac{\tan x}{x},\qquad \lim_{x\to 0} x\log x.$$

have problems upon plugging in $x = 0$. We have developed some strategies for evaluating limits that lead to $\frac{0}{0}$, for example multiplying by the conjugate in

$$\lim_{x\to 2}\frac{\sqrt{x^2 - 3} - 1}{x-1}.$$ 

Sometimes however, these strategies fail us and we need to try other methods. L'Hopital's rule is one such method. 


### Definition & Theorem
<div class="definition">
<b>Definition:</b> Consider the limit
$$\lim_{x\to a}\frac{f(a)}{g(a)}.$$
Each of the following are said to be <i>indeterminate forms</i>
<ul>
<li> $\lim_{x\to a} f(x) = 0$ and $\lim_{x\to a} g(x) = 0$. This is called a "$\frac{0}{0}$" form. </li>
<li> $\lim_{x\to a} f(x) = \pm\infty$ and $\lim_{x\to a} g(x) = \pm\infty$. This is called a "$\frac{\infty}{\infty}$" form. </li>
</ul>
</div> <br>

Note that this definition actually encompasses other cases if we do a little bit of work. For example, if we consider a form $0\times\infty$, then this is equivalent to the above cases, because one can think of this as "$\frac{0}{\frac{1}{\infty}} = \frac{0}{0}$".Thus we make this *into* an indeterminate form. Another example of a function which can turn into an indeterminate form is the exponential. Consider the limit

$$L = \lim_{x\to a} [f(x)]^{g(x)}$$

If we end up with a form of $1^\infty$ or $\infty^0$, then these are also indeterminate forms! This is so because we can take the logarithm of both sides to form

$$\log L = \lim_{x\to a}g(x)\log f(x).$$

In the case of $f(x)\to 1$ and $g(x)\to\infty$, we find that $\log f(x)\to 0$, so we have a $0\times\infty$ form. In the case $f(x)\to\infty$ and $g(x)\to 0$, then we find that $\log f(x)\to\infty$, so we again have a $0\times\infty$ form. Both of these can be changed into $\frac{0}{0}$ or $\frac{\infty}{\infty}$. 

<div class="theorem">
<b>Theorem:</b> (L'Hopital's Rule) Suppose the limit
$$\lim_{x\to a}\frac{f(x)}{g(x)}$$
is an indeterminate form. Then, the limit is equivalent to
$$\lim_{x\to a}\frac{f(x)}{g(x)} = \lim_{x\to a}\frac{f'(x)}{g'(x)}.$$
Note that the theorem holds also if $a = \pm\infty$. 
</div> <br>

Also note that if the resulting limit is again of the form $\frac{0}{0}$, we can continue applying L'Hopital's rule and get 

$$\lim_{x\to a}\frac{f'(x)}{g'(x)} = \lim_{x\to a}\frac{f''(x)}{g''(x)}.$$

SHOW PROOF HERE?

### Examples
Let's start with the examples that we started the section with, and then proceed to some more difficult ones. 

<div class="example">
<p><b>Example:</b> Evaluate the limit $$\lim_{x\to 0} \frac{\tan x}{x}$$
</p>
<b>Solution:</b>
</div> <br>


<div class="example">
<p><b>Example:</b> Evaluate the limit $$\lim_{x\to 0} x\log x.$$ </p>
<b>Solution:</b>

</div> <br>


<div class="example">
<p><b>Example:</b> Evaluate this limit with and without L'Hopital's rule 
$$\lim_{x\to 2}\frac{\sqrt{x^2 - 3} - 1}{x-1}.$$ </p>
<b>Example:</b> 

</div> <br>


<div class="example">
<p><b>Example:</b> Evaluate the limit 
$$\lim_{x\to 0} \frac{2\cos x - 2}{e^x - 1 - x}$$ </p>
<b>Example:</b> 


</div> <br>
