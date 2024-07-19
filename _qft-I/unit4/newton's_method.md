---
layout: lesson
title: Newton's Method
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---


### Introduction
In high school, we learned how to solve various algebraic equations. The most notable of which is the quadratic equation

$$ax^2 + bx + c = 0,$$

the solution to which was the quadratic formula

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}.$$

There are of course many equations which don't have simple solutions like that! For example, 

$$x^3 - 2x + 2 = 0$$

doesn't have a nice easy formula! One can use a computer to solve such equations, but, what does that computer actually do when it calculates the solution? One of the methods that one could program into a computer is called *Newton's method*, which is the topic of this section.

In this course, Newton's method has two uses: 
1. Providing approximate solutions to algebraic equations
2. Providing decimal expansions for numbers like $\sqrt{2}$

### The Method
Suppose we have the graph of $y = f(x)$, and we are looking for a solution of $f(x) = 0$. Let's make a guess of the solution, and call it $x_0$. Now, unless we were very very lucky, $f(x_0) \not= 0$. If it is a good guess however, then we can say that the tangent line to $f(x)$ at $x_0$ will intersect the $x$ axis at a point closer to the root than our original guess. Suppose it intersects at a point $x_1$. Now we apply the same procedure to $f(x_1)$. 

More systematically, we consider the tangent line about $x_n$:

$$L(x) = f(x_n) + (x-x_n)f'(x_n).$$

We then set $x_{n+1}$ to be the intersection of this line and the $x$ axis. Thus setting $L(x_{n+1}) = 0$, we find that 

$$0 = f(x_n) + (x_{n+1} - x_n)f'(x_n).$$

Now if we solve for $x_{n+1}$, we find

<div class="result">
<b>Newton's Method:</b>
To iteratively solve $f(x) = 0$, we make a guess $x_0$. We plug $x_0$ into the following formula to find $x_1$. Continue plugging into the following formula to get sucessively better approximations to the solution of $f(x) = 0$. 
$$x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}.$$
</div>


### Examples
<div class="example">
<p><b>Example:</b> Find an approximation to the solution of $x^2 = 2$ by using Newton's method with an initial guess of $x_0 =1$. Find the third approximation $x_3$.  </p>
<b>Solution:</b>

</div>

<div class="example">
<p><b>Example:</b> Find an approximation to the solution of $x^2 = 2$ by using Newton's method with an initial guess of $x_0 =1$. Find the third approximation $x_3$.  </p>
<b>Solution:</b>

</div>








