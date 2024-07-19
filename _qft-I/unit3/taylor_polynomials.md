---
layout: lesson
title: Taylor Polynomials
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

Suppose we have a function $f(x)$, and we are interested in approximating its value near $x = a$. A truly awful approximation would be $f(x)\approx f(a)$. This is an awful approximation because it works only at the value $x = a$. Everywhere else, the approximation, which is simply a horizontal line, isn't even close to the value of the actual function. 

(insert figure here)

A better approximation would be a straight line which not only passes through the point $(a,f(a))$, but also has the same slope as the original function at that point. This approximation is the linear approximation which we have discussed before:

$$f(x) \approx f(a) + (x-a)f'(a)\approx f(x).$$

(insert figure here)

One can see that this approximation not only passes through the curve at $(a,f(a))$, but also is pretty close to the curve in a small neighbourhood around $x=a$. 

The next best approximation would match the second derivative as well. This approximation is 

$$f(x) \approx f(a) + (x-a)f'(a) + \frac{(x-a)^2f''(a)}{2}.$$

Let's proceed to one order higher before generalizing this result. 

$$f(x) \approx f(a) + (x-a)f'(a) + \frac{(x-a)^2f''(a)}{2} + \frac{(x-a)^3f'''(a)}{6}.$$

The pattern here should be come clear. Rewriting it in the following form and recalling that $0! = 1$, 

$$f(x) \approx \frac{(x-a)^0 f(a)}{0!} + \frac{(x-a)^1f'(a)}{1!} + \frac{(x-a)^2f''(a)}{2} + \frac{(x-a)^3f'''(a)}{6}.$$

The formula for the $n$ Taylor polynomial to $f$ centred about $x-a$ is therefore

<div class="result">
<b>Result:</b> Suppose $f(x)$ is a function which is differentiable $n$ times at $x=a$. Then, its $n$th degree Taylor polynomial about $x = a$ is given by 
$$T_n(x) = \sum_{k=0}^n \frac{(x-a)^k f^{(k)}(a)}{k!}.$$
The higher $n$ is, the better $T$ approximates $f$. 
</div>

Now, let's proceed with some examples of calculating Taylor approximations to certain functions.

<div class="example">
<p><b>Example:</b> Calculate the 

</p> <b>Solution:</b>


</div>


<div class="example">
<p><b>Example:</b> Calculate the 

</p> <b>Solution:</b>


</div>


<div class="example">
<p><b>Example:</b> Calculate the 

</p> <b>Solution:</b>


</div>
