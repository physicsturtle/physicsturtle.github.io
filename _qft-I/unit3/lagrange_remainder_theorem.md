---
layout: lesson
title: Lagrange Remainder Theorem 
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

In the last section, we considered the Taylor polynomial to $f(x)$ at $x=a$, the formula for which is 

$$T_n(x) = \sum_{k=0}^n \frac{(x-a)^k f^{(k)}(a)}{k!}$$

We said that this approximated $f(x)$, and thus wrote $f(x) \approx T_n(x)$. This means that there is some difference between the approximation $T$ and the original function $f$. We call this difference the *remainder*. 

<div class="definition">
<b>Definition:</b> The remainder $R_n$ of the $n$th degree Taylor polynomial is defined as 
$$R_n(x) = f(x) - T_n(x).$$
</div>

There is a theorem about the remainder which will allow us to make bounds on the error. This theorem is an existence theorem whose proof is not constructive. Thus, we will not be able to actually calculate this remainder. 

<div class="theorem">
<b>Theorem:</b> 
</div>

Consider approximating the function $f(x)$ about the point $x = a$. Suppose we have the $n$th degree polynomial $T_n$, and want to know the value 

